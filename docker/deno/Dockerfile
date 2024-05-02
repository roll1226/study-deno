FROM denoland/deno:alpine

WORKDIR /src

RUN apk update
RUN apk add curl zip unzip
RUN deno install -qAf --unstable https://deno.land/x/denon/denon.ts

ENV PATH="/root/.deno/bin:$PATH"

COPY . .

EXPOSE 8000

CMD ["denon", "run", "-A", "main.ts"]
