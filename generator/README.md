
# generator-luna

[![License](https://img.shields.io/badge/license-Apache%202-4EB1BA.svg)](https://www.apache.org/licenses/LICENSE-2.0.html)
v1.1.6

### Luna generator Goals
 * Provide a framework for healthcare software architecture
 * Provide a notion about continual development
 * One small step towards Luna's mission


## Documentation

- [Jhipster Home](https://www.jhipster.tech/)
- [Demo Site](https://luna.lian-med.com/)
- [More notions](https://github.com/alibaba/fastjson/wiki/%E5%B8%B8%E8%A7%81%E9%97%AE%E9%A2%98)

## Usage
v1.1.6
first of all you need to install nodejs  

- [Nodejs Home](https://nodejs.org/en/)
``` 
npm -version
```
install package :you need to install our generator globally
``` 
npm install -g generator-luna
```
make your project dir eg. windows
```  
cmd
mkdir myproject
```
copy the .jdl and run the command
``` 
copy the OBDML02-auth.jh file into your project directory
the modifiable fields are as follows,please keey others remain
baseName GenLuna,
packageName com.lianmed.gen,
serverPort 8082,
``` 
``` 
luna genform OBDML02-auth.jh --force
```
modify the database config,maybe you need to create a new empty databse
```
src\main\resources\config\application-dev.yml
 datasource:
        type: com.zaxxer.hikari.HikariDataSource
        url: jdbc:mysql://localhost:3306/GenL1?useUnicode=true&characterEncoding=utf8&useSSL=false&useLegacyDatetimeCode=false&serverTimezone=UTC
        username: root
        password: root
```
at last, run mvnw
``` 
mvnw
```
