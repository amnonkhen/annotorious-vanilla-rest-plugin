# Annotorious Vanilla REST Plugin

The Vanilla REST Plugin is a basic plugin to store annotations on a REST-style HTTP endpoint. In general, you
will want to provide this server-side endpoint yourself, as part of your application, and persist the annotations
in your own database. However, the project also includes a simple storage server. (Consider it a "reference
implementation".)

In addition to storage, the plugin also augments the annotation popup in case the JSON returned from the server
includes 'username', 'user_avatar' and 'timestamp' fields.


## API

```
GET    /annotations?context={}
GET    /annotations?url={}
GET    /annotations/{id}
POST   /annotations
DELETE /annotations/{id}
UPDATE /annotations/{id}
```
