```
ENTRYPOINT ["deno", "run", "--allow-net", "main.ts"]
```

Note: That the listen port (4000), must match with the EXPOSED port in the Dockerfile.


```sh
$ docker build -t edoo-api . && docker run -it --init -p 4000:4000 edoo-api
```
