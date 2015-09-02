Usage
=====

Usecase: a sqlite Db is on server and will moved to app.

```javascript
var DBModule = require('de.appwerft.sqlitemirror');
var Database = new (DBModule)({
    dbname : LOCALDBNAME,
    url : url,
    timeout : 10000,
});
Database.loadDB();
Database.addEventListener('load', function(_e) {
    // do something with local DB
});

```

The module uses Etag-mechanism. If the database is not modified, then data will transfer. 