FROM hayd/deno:alpine-0.32.0

EXPOSE 4000

WORKDIR /src

USER deno

COPY deps.ts .
RUN deno fetch deps.ts

ADD . .
RUN deno fetch main.ts

ENTRYPOINT ["deno", "run", "--allow-net", "main.ts"]
