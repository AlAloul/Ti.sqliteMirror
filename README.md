Usage
=====

```javascript
var DBModule = require('de.appwerft.sqlitemirror');
var Database = new (DBModule)({
    dbname : LOCALDBNAME,
    url : url,
    timeout : 10000,
});
Database.loadDB();
Database.addEventListener('load', function(_e) {
    // do something
});

```