FROM node:16-alpine as installer

WORKDIR /app

COPY package.json yarn.lock* ./
RUN yarn install --frozen-lockfile

FROM node:16-alpine

WORKDIR /app
COPY --from=installer /app/node_modules ./node_modules
COPY . .

ARG FRONTEND_ENV=dev
ENV VUE_APP_ENV=${FRONTEND_ENV}
ENV NODE_ENV=development
ENV HOST 0.0.0.0
ENV PORT 80

EXPOSE 80
EXPOSE 24678

CMD ["yarn", "dev"]
