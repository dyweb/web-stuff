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