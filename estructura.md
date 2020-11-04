<!--HEADERS--->
# my title
## title2
### title3
#### title 4
##### title h5
###### title 6

<!--PARRAFOS--->
*italic text*

**bold text**

~~tachado~~

<!--------------LISTAS--------->
<!--LISTA DESORDENADA-->
* item 1
    * subitem 1
    * subitem 2
* itme 2

<!--LISTA ORDENADA-->
1. ITEM 1
    * sub item 1
        * sub sub item 1
2. ITEM 2

<!------ENLACES---------------->
[GOOGLE](http://www.google.com)

[GOOGLE](http://www.google.com "custom title")

<!---LINEAS-->

---

<!------CITAS------------->
> this is a quote

<!-------------------INSERT CODE---------------------------->
<!--Linea codigo-->
` console.log("PRUEBA CODIGO"); `
<!------Bloque codigo------>
``` javascript
    const { connectionClass } = require('oracledb');
const oracledb = require('oracledb');
try{
    oracledb.initOracleClient({configDir: '/opt/oracle/instantclient_19_8'});
}
catch (err){
    console.error("PTM");
    console.error(error);
    process.exit(1);
}

database = {
    user: "system",
    password: "oracle",
    connectString: "192.168.1.9:4000/test"
}


async function Open(sql, binds, autoCommit) {
    let cnn = await oracledb.getConnection(database);
    cnn.execute();
    console.log("datbase connected")
    let result = await cnn.execute(sql, binds, { autoCommit });
    cnn.release();
    return result;
}

exports.Open = Open;
```

<!-----------------------TABLAS--------------------------->
|   Column 1    |  Column 2 |
|   -------     |   ------- |
|   dato 1      |   dato 2  |

<!-----------------------IMAGENES------------------------->
![code](data:image/jpeg;base64,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 "code")

<!--GITHUB MARKDOWN-->
* [ x ] Task 1
* [ x ] Task 1
* [  ] Task 1



