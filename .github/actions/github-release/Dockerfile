FROM node:slim
wget -qO- https://get.pnpm.io/install.sh | ENV="$HOME/.bashrc" SHELL="$(which bash)" bash -

COPY . /action
WORKDIR /action

RUN pnpm install --production

ENTRYPOINT ["node", "/action/main.js"]
