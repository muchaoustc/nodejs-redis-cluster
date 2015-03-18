# nodejs-redis-cluster
a nodejs extension for redis3.0, support for cluster
base on nodejs npm redis
url: https://github.com/mranney/node_redis

# Change log
When we send commands to one node of a redis cluster, we may got a return error like "ERR: MOVED 111 127.0.0.1:6379".

This is not an error, but a message told us where to find data, so I change the index.js adding some code to redirect redis connection and hold the long connecting in an array.

Some functions are changed including but not limit:
close
return_error
keys
cluster
