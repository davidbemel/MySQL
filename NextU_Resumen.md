# Índices:
```
    CREATE TABLE [tabla] ([col 1] [tipo 1],....[col 2] [tipo 2],
    PRIMARY KEY ([campo_pk])KEY [key_name1] ([campos2]),
    ...KEY [key_name2] ([campos2]),)
```
Claves Foráneas:
```
    CREATE TABLE [tabla] ([col 1] [tipo 1],....[col 2] [tipo 2],
    PRIMARY KEY ([campo_pk])KEY [key_name1] ([campos2]),
    ...CONSTRAIN [nombre_fk1] FOREIGN KEY ([campo_origen1]) 
    REFERENCES [tabla destino1]([campo_destino1]),
    CONSTRAIN [nombre_fk2] FOREIGN KEY ([campo_origen2]) 
    REFERENCES [tabla destino2]([campo_destino2]))
```
    Left Join:
```
    SELECT * FROM [tabla_izquierda] LEFT JOIN [tabla_derecha] 
    ON [condición que une las tablas]
```
    Right Join:
```
    SELECT * FROM [tabla_izquierda] RIGHT JOIN [tabla_derecha] 
    ON [condición que une las tablas]
```    
    --------
    
    
        Triggers:
```
    CREATE TRIGGER [nombre_trigger] [AFTER|BEFORE] 
    [UPDATE|INSERT|DELETE] ON [nombre_tabla]
    FOR EACH ROW BEGIN …[cuerpo trigger]END
```
    Procedures:
```
    CREATE PROCEDURE [nombre_procedure] (parametros) 
    BEGIN …[cuerpo procedure]END
```    
#  DUMP
  
  Respaldo
  ```
  mysqldump -u [usuario] -p [base_de_datos] > [archivo.sql]
  ```
  Recuperando
  ```
   mysql -u [usuario] -p [base_de_datos_destino] < [archivo.sql]
```

# Monitoreo


 Veamos cómo se realizan las operaciones de monitoreo en MySQL.

    Número de Conexiones:
```
    mysql> SHOW STATUS WHERE `variable_name` = 'Threads_connected';
```
    Ver las conexiones activas:
```
    mysql> SHOW PROCESSLIST;
```
    Matar una conexión :
```
    mysql> KILL [conection_id];
```
