v1.1.6
使用方法


# generator-luna

[![License](https://img.shields.io/badge/license-Apache%202-4EB1BA.svg)](https://www.apache.org/licenses/LICENSE-2.0.html)


### Luna generator Goals
 * Provide best performance in server side and android client
 * Provide simple toJSONString() and parseObject() methods to convert Java objects to JSON and vice-versa
 * Allow pre-existing unmodifiable objects to be converted to and from JSON
 * Extensive support of Java Generics
 * Allow custom representations for objects
 * Support arbitrarily complex objects (with deep inheritance hierarchies and extensive use of generic types)


## Documentation

- [Documentation Home](https://github.com/alibaba/fastjson/wiki)
- [Contributing Code](https://github.com/nschaffner/fastjson/blob/master/CONTRIBUTING.md)
- [Frequently Asked Questions](https://github.com/alibaba/fastjson/wiki/%E5%B8%B8%E8%A7%81%E9%97%AE%E9%A2%98)

## Usage

``` first of all you need to install nodejs  
- [Nodejs Home](https://nodejs.org/en/）
```

``` install package :you will install our generator globally
npm install -g generator-luna
```

``` make your project dir eg. windows 
cmd
mkdir myproject
```

``` copy the .jdl and run the command
cp the OBDML02-auth.jh file into your project directory
luna genform OBDML02-auth.jh --force
```

``` at last, run mvnw
mvnw
```
