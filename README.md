# Annotorious Vanilla REST Plugin

The Vanilla REST Plugin is a basic plugin to store annotations on a REST-style HTTP endpoint. In general, you
will want to provide this server-side endpoint yourself, as part of your application, and persist the annotations
in your own database.

## Usage
```javascript
// simple
anno.addPlugin('VanillaREST', {});

// specifying options
anno.addPlugin('VanillaREST', {
                'prefix':'/store',
                'urls': {
                    read: '/index',
                    create:  '/create',
                    update:  '/edit/:id',
                    destroy: '/delete/:id',
                    search:  '/search?query=*&limit=1000'
                },
                extraAnnotationData: {type: 'highlighted'}
            });
            
```

## Options

```
prefix                 url prefix. Default: 'store'
urls                   urls for each request. they will get appended to the prefix
extraAnnotationData    extra data that is added to annotation before it is sent with the create/update request.
loadFromSearch         Load annotations from search url rathern than read url. Default: false
```
