FROM node:24.13.0-alpine

RUN npm install -g pnpm

WORKDIR /frontend
# Copy package.json and pnpm-lock.yaml (if it exists)
COPY package.json pnpm-lock.yaml* ./
# Install dependencies using pnpm
RUN pnpm install

COPY . .

EXPOSE 5173

CMD ["pnpm","run", "dev", "--","--host"]
