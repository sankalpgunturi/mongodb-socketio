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

### Screenshots of execution

1. Connect to `localhost:27017` on [MongoDB Compass](https://www.mongodb.com/products/compass).

2. Create a Database, and name it `chat`. Also create a collection in that database, and name it `messages`:

![Newly_Created_DB](/assets/Newly_Created_DB.png)

3. Follow `How to run?` from above, and add data into the collection:

![Insert_first_Message](/assets/Insert_first_Message.png)

4. Check out the browser with `localhost:3000`:

![Check_out_browser](/assets/Check_out_browser.png)

5. Update message in DB:

![Update_first_Message](/assets/Update_first_Message.png)

6. Check out the browser again:

![Check_out_update_Messages](/assets/Check_out_update_Messages.png)

### References

[^1]: [MongoDB docs on replica set](https://www.mongodb.com/docs/manual/tutorial/convert-standalone-to-replica-set/)
[^2]: [StackOverflow guide in case of errors](https://stackoverflow.com/questions/70081140/mongodb-replica-set-cannot-use-non-local-read-concern-until-replica-set-is-fin)
[^3]: [MongoDB's tutorial on linking socket.IO](https://www.mongodb.com/developer/products/mongodb/mongo-socket-chat-example/)
