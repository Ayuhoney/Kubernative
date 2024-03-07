FROM node AS builder
WORKDIR /myapp
COPY ./package*.json ./
RUN npm install
COPY . .

FROM node:alpine
WORKDIR /myapp
COPY --from=builder /myapp .
EXPOSE 3000
CMD ["npm", "start"]

