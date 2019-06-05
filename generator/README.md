
# generator-luna

[![License](https://img.shields.io/badge/license-Apache%202-4EB1BA.svg)](https://www.apache.org/licenses/LICENSE-2.0.html)


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
- [Nodejs Home](https://nodejs.org/en/）
``` 
npm -version
```
install package :you will install our generator globally
``` 
npm install -g generator-luna
```
make your project dir eg. windows
```  
cmd
mkdir myproject
```
copy the .jdl and run the command

copy the OBDML02-auth.jh file into your project directory
``` 
luna genform OBDML02-auth.jh --force
```
at last, run mvnw
``` 
mvnw
```
