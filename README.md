# Liquibase Intregation

Liquibase playground

## Getting Started

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

## Local setup

- Create new Liquibase project files

```
liquibase init project
```

- Run PostgreSQL container

```
docker run -d --name pgtest -p 5432:5432 -e POSTGRES_PASSWORD=admin123 pgvector/pgvector:pg16
```

- Deploy changes

```
liquibase update
```

- Output

![Output](https://github.com/user-attachments/assets/610d3af9-731c-4313-868f-14a1b80a4287)

## Maven setup
- Add dependencies in `pom.xml`
- Set `liquibase.properties`
- Add following files under `/src/main/resources`
  - `db.changelog.xml` as main liquibase file
  - `db.changelog-0.0.1.xml` being referenced in `db.changelog.xml`
  - `/sql/db.schema_v1.sql` being referenced in `db.changelog-0.0.1.xml`

## Arch Diagram

![liquibase-arch](https://github.com/user-attachments/assets/c0c60d80-262d-4d01-be20-61080d112550)

## Dir Structure

![liquibase-dir-structure](https://github.com/user-attachments/assets/333c6a9a-a082-4513-99ab-925a27aa7a0c)

## Useful Links

- https://docs.liquibase.com/commands/init/project.html
