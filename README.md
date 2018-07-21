# typescript-example
example for typescript, with decorators (routing-controllers and sequelize)

## dependence

- [routing-controllers](https://github.com/typestack/routing-controllers)
- [sequelize](https://github.com/sequelize/sequelize)
- [sequelize-typescript](https://github.com/RobinBuschmann/sequelize-typescript)

## usage

```bash
> npm i
> brew service start mysql
> mysql -u root -p
# 请自行修改config/backend/local.js 中的user、password 以及以下的database
mysql> create database ts_test;
mysql> use ts_test;
mysql> CREATE TABLE `user_info_test` (   `uid` int(11) unsigned NOT NULL AUTO_INCREMENT,   `name` varchar(11) NOT NULL,   `age` int(3) DEFAULT '0',   `gender` int(1) NOT NULL,   PRIMARY KEY (`uid`) ) ENGINE=InnoDB DEFAULT CHARSET=utf8;

> npm run watch-ts
> npm run watch-node

> curl http://127.0.0.1:6666/add/Niko/1
> curl http://127.0.0.1:6666/add/Bellic/2

> curl http://127.0.0.1:6666/list/          # [{name: Niko, ...}, {name: Bellic, ...}]
> curl http://127.0.0.1:6666/list/filter/1  # [{name: Niko, ...}]
```