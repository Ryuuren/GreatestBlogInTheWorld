# Dev notes

Basic blog

## Tech Stack

| Tech | Desc |
| --- | --- |
| Hosting | Vercel |
| Backend | Node, Express, Cors |
| Frontend | TypeScript, React, NextJS |
| Database | PostgreSQL |
| Styling | Tailwind |

## Features

- user access: create own blog post, edit own blog post, delete own blog post
- user access levels: member, admin

## Considerations

| Backend | Notes |
| --- | --- |
| Authentication | JWT or Google OAuth |
| Authorisation | Role-based access control (RBAC) |
| Error handling | try...catch (my python brain is twitching rn - Jess) |
| Error logging | logger for errors so we can identify issues more easily |
| Db | Rollbacks to maintain data integrety |
| Db schema | Tables: Users, Posts, Comments, Categories/Tags |
| Db table relationships | 1 post : 1 user(?) 1 user : many posts |
| DB indexing | userid |
| Db naming convention | user_id or userid or id |
| Db security | [PostgreSQL here](https://www.crunchydata.com/blog/preventing-sql-injection-attacks-in-postgresql) |
| Database auditing | [PostgreSQL Auditing Extention (PGAudit)](https://www.pgaudit.org/) |
| SQL injection & XSS | Paramatise SQL statements; sanitise all inputs for things like `DROP TABLE` `DELETE FROM` `DELECT * FROM` `--` `;` ([stackoverflow convo with other stuff](https://stackoverflow.com/questions/58174695/prevent-sql-injection-with-nodejs-and-postgres)) |
| API | RESTful (CRUD), HTTP methods (GET, PUT, POST, DELETE, PATCH(?)) |
| API | Middleware to handle authorisation |
| Security | hash and salt passwords; HTTPS; input validation and sanitisation |

| Frontend | Notes |
| --- | --- |
| Authentication | JWT or [Google OAuth with nodejs](https://github.com/googleapis/google-api-nodejs-client) |
| Authorisation | [Role-based access control (RBAC)](https://auth0.com/docs/manage-users/access-control/rbac) |
| React state management | Redux(?) |
| React navigation | React router (blog list > detailed view > edit form) |
| Validation of forms | regex, js ...? |
|  |  |