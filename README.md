# SQLite-Python
#David Sanchez
#Ficha: 2502640

# UPDATE 
""" Para actualizar los datos existentes en una tabla, primero se especifica la tabla donde desea actualizar luego UPDATE para actualizar y para cambiar el valor de una columna se utuliza SET. """

    """ UPDATE table
    SET column_1 = new_value_1,
        column_2 = new_value_2; """

# estructura de la base de datos .schema
""" En algunos casos los comandos SQL aparecen para poder crear cada uno de los objetos de las bases de datos main y temp. Esto significa que mostrará las declaraciones de crear para una o varias mesas. """

    """ .schema [name_table] """

# date and time functions
""" date(time-value, modifier, modifier, ...)
time(time-value, modifier, modifier, ...) 
estos toman forma de un argumento de fecha y hora; todas las funciones de fecha y hora acceden a valores de tiempo en cualquiera de los formatos de tiempo anteriores. """

    """ Formato que devuelve la función date(): AAAA-MM-DD. 
    Formato que devuelve la función time(): HH:MM:SS. """

# primary key constraint
""" Una llave primaria es un grupo de columnas que se utiliza para identificar la unicidad de las filas de una tabla. Cada tabla tiene una y sólo una clave principal. """

    """ CREATE TABLE table_name(
    column_1 INTEGER NOT NULL PRIMARY KEY); """

# not null constraint
""" Es una restricción se usa para indicar que la columna no permitirá almacenar valores NULL lo que hace sea una restricción llenar el campo o arrojará error. """

    """ CREATE TABLE tablename
    (column1 INTEGER,
    column2 TEXT NOT NULL,
    column3 TEXT NOT NULL); """

# unique constraint
""" UNIQUE es la restricción que garantiza que todos los valores de una columna o un grupo de columnas sean distintos entre sí o únicos. """

    """ CREATE TABLE table_name(
        column_name type UNIQUE); """

# default constraint
""" DEFAULT se usa para definir valores predeterminados para una columna. """

    """ CREATE TABLE tablename
    (colum1 INTEGER PRIMARY KEY,
    column2 TEXT NOT NULL,
    column3 INTEGER DEFAULT defaultvalue); """

# check constraint
""" CKECK tiene como función verificar valores cada vez ue se insertan o actualizan dentro de una columna, si los valores no cumplen con los criterios definidos SQLite emitirá una violación de restricción y anulará la declaración. """

    """ CREATE TABLE table_name(
        column_name data_type CHECK(expression)); """

# alter table
""" ALTER TABLE en SQLite permite: se puede renombrar; se puede cambiar el nombre de una columna; se le puede agregar una columna; o se puede quitar una columna de él. """

    """ ALTER TABLE tablename
    (ADD FOREING KEY (DATO),
    REFERENCES tablename(othertablename)); """

# delete, drop
""" DROP nos sirve para eliminar una tabla y borrarla por completo. Y el DELETE nos sirve para borrar los datos que están dentro de la tabla """

""" DROP TABLE tablename;
DELETE * FROM datoname; """

# backup, restore
""" BACKUP copia el contenido de una base de datos en otra, sobrescribiendo el contenido de la base de datos de destino. Es útil para crear copias de seguridad de bases de datos o para copiar bases de datos. RESTORE es lo contrario de BACKUP y lo que hace es que realiza una copia de bajo nivel de un archivo de base de datos en una base de datos abierta o adjunta; este comando se usa con frecuencia para llenar una base de datos en memoria activa desde un archivo de base de datos """

""" /*Base de datos existente (BACKUP)*/
<?php
// $conn is a connection to an already opened sqlite3 database

$backup = new SQLite3('backup.sqlite');
$conn->backup($backup);
?>

/*(RESTORE)*/
.restaurar [ database_name]filename """
