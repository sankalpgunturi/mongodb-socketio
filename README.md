# MongoDB == Socket.IO

## Integrating MongoDB Change Streams with Socket.IO

### How to run?

When implementing in macOS, open three terminals:

1. The first terminal should be running MongoDB Daemon with `dbpath` and `replicaSet`[^1] mentioned, something like this:

```
/Users/wolfe/mongodb/bin/mongod --port=27017 --dbpath=/Users/wolfe/mongodb-data --replSet rs0
```

2. The second terminal should be running Mongo[^2], something like this:

```
/Users/wolfe/mongodb/bin/mongo
```

3. The third terminal should run our Node.JS code[^3], like this:

```
node index.js
```

### References

[^1]: [MongoDB docs on replica set](https://www.mongodb.com/docs/manual/tutorial/convert-standalone-to-replica-set/)
[^2]: [StackOverflow guide in case of errors](https://stackoverflow.com/questions/70081140/mongodb-replica-set-cannot-use-non-local-read-concern-until-replica-set-is-fin)
[^3]: [MongoDB's tutorial on linking socket.IO](https://www.mongodb.com/developer/products/mongodb/mongo-socket-chat-example/)
