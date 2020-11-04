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
![code](descarga.jfif "code")

<!--GITHUB MARKDOWN-->
* [X] Task 1
* [X] Task 1
* [ ] Task 1



