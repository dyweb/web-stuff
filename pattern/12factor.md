# 12 factor

- site: http://12factor.net/
- repo: https://github.com/heroku/12factor
- fork: https://github.com/dyweb/12factor

## CodeBase 

- site: http://12factor.net/codebase
- zh-cn: http://12factor.net/zh_cn/codebase

- A codebase is a repo in git, it has many deploys, production, staging, developer 1's local machine, dev2 etc
- Use libraries and dependency management tools to share code between codebase

## Dependency

- site: http://12factor.net/dependencies
- zh-cn: http://12factor.net/zh_cn/dependencies

- explicit dependency declaration 
- dependency isolation

DONT use system wide tool or lib, since they may not be installed on all machines or has wrong version. use vendored system tools.
(TODO: how to do that in php, have a curl binary inside vendor folder?)


## Config

－ site： http://12factor.net/config
－ zh-cn: http://12factor.net/zh_cn/config

- store config value in environment variables

DONT use language or framework specific config like `database.yml` `console.properties`. 

## Backing Services

- site: http://12factor.net/backing-services
- zh-cn: http://12factor.net/zh_cn/backing-services

- local and remote services are all attached resources through network. ie: Database in local server and Amazon. 

## Build release run

- site: http://12factor.net/build-release-run
- zh-cn: http://12factor.net/zh_cn/build-release-run

- separate build, release and run. 
- build, compile code, contact, compress etc. can be complex and show error messages to developer
- release, build + config
- run, launch app process against a selected release. should be simple.
- able to rollback ie: Capistrano 

## Processes

- site: http://12factor.net/processes
- zh-cn: http://12factor.net/zh_cn/processes

- stateless, persist in database or cache. 

## Port binding

- site: http://12factor.net/port-binding
- zh-cn: http://12factor.net/zh_cn/port-binding

- have a build in http server, can become a backing service

## Concurrency 

- site: http://12factor.net/concurrency
- zh-cn: http://12factor.net/zh_cn/concurrency

- use process to scale out
- processes share nothing
- use process managers to manage, such as upstart, foreman

## Disposability

－ site: http://12factor.net/disposability
- zh-cn: 