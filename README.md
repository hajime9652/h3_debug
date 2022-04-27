
## unjs/h3 debugging repo
first you build and run the container.
```
docker-compose up -d --build
```

then access to `localhost:8899`, you can get this error.
```
h3_debug-frontend-1  | yarn run v1.22.18
h3_debug-frontend-1  | $ node .output/server/index.mjs
h3_debug-frontend-1  | Listening on http://0.0.0.0:80/
h3_debug-frontend-1  | file:///app/.output/server/chunks/nitro/server.mjs:109
h3_debug-frontend-1  | const hasReqHeader = (req, header, includes) => req.headers[header] && req.headers[header].toLowerCase().includes(includes);
h3_debug-frontend-1  |                                                            ^
h3_debug-frontend-1  | 
h3_debug-frontend-1  | TypeError: Cannot read properties of undefined (reading 'accept')
h3_debug-frontend-1  |     at hasReqHeader (file:///app/.output/server/chunks/nitro/server.mjs:109:60)
h3_debug-frontend-1  |     at Object.handleError [as onError] (file:///app/.output/server/chunks/nitro/server.mjs:111:25)
h3_debug-frontend-1  |     at nodeHandler (file:///app/.output/server/node_modules/h3/dist/index.mjs:370:23)
h3_debug-frontend-1  |     at processTicksAndRejections (node:internal/process/task_queues:96:5)
h3_debug-frontend-1  | error Command failed with exit code 1.
h3_debug-frontend-1  | info Visit https://yarnpkg.com/en/docs/cli/run for documentation about this command.
```