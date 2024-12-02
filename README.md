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
liquibase init project
```

## Arch Diagram
![liquibase-arch](https://github.com/user-attachments/assets/c0c60d80-262d-4d01-be20-61080d112550)

## Useful Links

- https://docs.liquibase.com/commands/init/project.html
