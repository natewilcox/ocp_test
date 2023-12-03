
# Issue Description

We are currently experiencing an issue with a pod that runs the image natewilcox/node_server:1.0.4. The pod works as expected when run individually. However, when the same pod is included in a deployment, an error occurs.

## Error Message

The error message we receive is as follows:

```
node_server@1.0.0 start
> whoami && node src/index.js
1000660000
Server listening at http://localhost:8080
npm ERR! code EACCES
npm ERR! syscall mkdir
npm ERR! path /.npm
npm ERR! errno -13
npm ERR!
npm ERR! Your cache folder contains root-owned files, due to a bug in
npm ERR! previous versions of npm which has since been addressed.
npm ERR!
npm ERR! To permanently fix this problem, please run:
npm ERR!   sudo chown -R 1000660000:0 "/.npm"
npm ERR! Log files were not written due to an error writing to the directory: /.npm/_logs
npm ERR! You can rerun the command with `--loglevel=verbose` to see the logs in your terminal
```