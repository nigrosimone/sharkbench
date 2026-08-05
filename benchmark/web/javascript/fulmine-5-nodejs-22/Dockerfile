# trixie: µWebSockets.js ships glibc binaries needing GLIBC >= 2.38 (no Alpine, no bookworm),
# and it is installed from GitHub, so git is needed
FROM node:22-trixie-slim

RUN apt-get update && apt-get install -y --no-install-recommends git ca-certificates && rm -rf /var/lib/apt/lists/*

WORKDIR /app
COPY . .

RUN npm install

EXPOSE 3000
CMD ["node", "main.js"]
