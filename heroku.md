# Heroku

↑ **Parent:** [Platform as a service](platform-as-a-service.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Heroku)

This feels good.

One problem though is that Heroku is very opinionated, a likely like other PaaSes. So if you are trying something that is slightly off the mos common use case, you might be fucked.

Another problem with Heroku is that it is extremely difficult to debug a build that is broken on Heroku but not locally. We needed a way to be able to drop into a shell in the middle of build in case of failure. Otherwise it is impossible.

Deployment:
```
git push heroku HEAD:master
```

View [stdout](standard-output.md) logs:
```
heroku logs --tail
```

[PostgreSQL](postgresql.md) database, it seems to be delegated to [AWS](amazon-web-services.md). How to browse database: [https://stackoverflow.com/questions/20410873/how-can-i-browse-my-heroku-database](https://stackoverflow.com/questions/20410873/how-can-i-browse-my-heroku-database)
```
heroku pg:psql
```

Drop and recreate database:
```
heroku pg:reset --confirm <app-name>
```
All tables are destroyed.

Restart app:
```
heroku restart
```

**Table of contents**

- [Send free emails from Heroku](send-free-emails-from-heroku.md)

## ↑ Ancestors (10)

1. [Platform as a service](platform-as-a-service.md)
2. [Type of cloud computing](type-of-cloud-computing.md)
3. [Cloud computing](cloud-computing.md)
4. [Computer form factor](computer-form-factor.md)
5. [Computer hardware](computer-hardware-split.md)
6. [Computer](computer-split.md)
7. [Information technology](information-technology.md)
8. [Area of technology](area-of-technology.md)
9. [Technology](technology-split.md)
10. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (6)

- [Express.js](express-js.md)
- [FeathersJS](feathersjs.md)
- [feathersjs/feathers-chat](feathersjs-feathers-chat.md)
- [Shakacode/react\_on\_rails](shakacode-react-on-rails.md)
- [Cirosantilli.com content uploaded to ourbigbook.com/cirosantilli](sponsor/updates/6/cirosantilli-com-content-uploaded-to-ourbigbook-com-cirosantilli.md)
- [The Math Genome Project](the-math-genome-project.md)
