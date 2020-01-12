# Datasource CheatSheet

## HSQL Datasource

```js
this.datasources["hsqldb"] = {
    class: 'org.hsqldb.jdbcDriver'
    , connectionString: 'jdbc:hsqldb:file:#expandPath("/PATH/TO/FILE")#'
};
```

Can specify bundle name if you really want, but I'm not even sure what that does!

```js
this.datasources["hsqldb"] = {
    class: 'org.hsqldb.jdbcDriver'
    , bundleName: 'org.hsqldb.hsqldb'
    , bundleVersion: '2.4.0'
    , connectionString: 'jdbc:hsqldb:file:#expandPath("/PATH/TO/FILE")#'
};
```

## H2 Datasource

```js
this.datasources["h2"] = {
    class: 'org.h2.Driver'
    , bundleName: 'org.h2'
    , connectionString: 'jdbc:h2:#expandPath("/db/h2db")#;MODE=MySQL;'
};
```

Additional (optional) configuration settings:

```js
this.datasources["h2"] = {
    class: 'org.h2.Driver'
    , bundleName: 'org.h2'
    , bundleVersion: '1.3.172'
    , connectionString: 'jdbc:h2:#expandPath("/db/h2db")#;MODE=MySQL'
    
    // optional settings
    , connectionLimit:100 // default:-1
    , validate:false // default: false
};
```