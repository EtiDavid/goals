# ---------- Stage 1: Build React ----------
FROM node AS builder

WORKDIR /app

COPY package.json .
RUN npm install

COPY . .

# ✔ Build-time env var (frontend)
ENV REACT_APP_API_URL=http://goalslb-618720737.eu-north-1.elb.amazonaws.com

RUN npm run build


# ---------- Stage 2: Serve Static Files ----------
FROM nginx:stable-alpine

# ❗ Important — fix path slashes
COPY --from=builder /app/build /usr/share/nginx/html

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]
