ARG NODE_VERSION=22

FROM node:${NODE_VERSION}-slim AS base

ENV PNPM_HOME="/pnpm"
ENV PATH="$PNPM_HOME:$PATH"
RUN corepack enable

FROM base AS prod

WORKDIR /app
COPY package.json /app
COPY pnpm-lock.yaml /app
RUN pnpm install --prod --frozen-lockfile

COPY . /app

FROM base
WORKDIR /app
COPY --from=prod /app/node_modules /app/node_modules
COPY --from=prod /app /app

EXPOSE 3000

CMD [ "node", "index.js"]