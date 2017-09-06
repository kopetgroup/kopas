drop kabeh user sek
```
db.dropAllUsers( {w: "majority", wtimeout: 5000} )
```
njuk gawe neh
`user: root`
`paswot: kopet1234`

```
use admin
db.dropAllUsers( {w: "majority", wtimeout: 5000} )
use admin
db.createUser({user:"root",pwd:"kopet1234",roles:[{role:"root",db:"admin"}]});
```

restart mongod
```
/usr/sbin/mongod --auth --rest 
```
jajal login
```
db.auth("root", "kopet1234")
```
kudune wes bener
