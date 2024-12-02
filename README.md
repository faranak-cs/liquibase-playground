# liquibase-playground

Liquibase playground

## Commands

1. Install Liquibase

```
brew install liquibase
```

2. Copy `examples` directory to different directory

```
cp -rf libexec/examples ~/YOUR_PATH
```

3. Run H2 database

```
liquibase init start-h2
```

4. Deploy all new changes

Go to `/examples/sql` directory first and run following command:

```
liquibase update
```

- Create new Liquibase project files

```
liquibae init project
```
