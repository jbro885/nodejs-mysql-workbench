# NodeJS with MySQL Workbench

## Install

```
$ npm install mysql
```

For information about the previous 0.9.x releases, visit the v0.9 branch.

Sometimes I may also ask you to install the latest version from Github to check if a bugfix is working. In this case, please do:

```
$ npm install felixge/node-mysql
```

or

```
$ npm install node-mysql
```

## Usage

```
var mysql      = require('mysql');
var connection = mysql.createConnection({
  host     : 'localhost',
  user     : 'USER_NAME',
  password : 'PASSWORD',
  database : 'datatable',
  port     : '3306'
});

connection.connect();

connection.query('SELECT * from hist_stock', function(err, rows, fields) {
  if (err) throw err;

  console.log('The solution is: ', rows[0]);
});

connection.end();
```

## Note

Refer to `https://github.com/felixge/node-mysql`
