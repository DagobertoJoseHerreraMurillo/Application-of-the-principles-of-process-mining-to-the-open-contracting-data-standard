# Application-of-the-principles-of-process-mining-to-the-open-contracting-data-standard

##### Table of Contents  
[Introduction](#introduction)  

[Motivation](#motivation)

[OCDS](#OCDS)

[Contribution](#Contribution)

[Background](#Background)

[Prior Work](#PriorWork)

[Process model](#process)

[Data description](#data)

[Descriptive analyss](#descriptive)

[Graphs](#graphs)

[Impact](#impact)

[Conclusion](#conclusion)


<a name="introduction"/>
Introduction




Directorio de carga
C:\Users\Dagoberto\.Neo4jDesktop\neo4jDatabases\database-f0deac7c-28e7-4fc6-bc3c-0c4ef4bbd86e\installation-3.5.2\import

Guia sobre cómo abrir
https://medium.com/neo4j/neo4j-get-off-the-ground-in-30min-or-less-3a226a0d48b1
Guía sobre cómo cargar
https://neo4j.com/graphgist/importing-csv-files-with-cypher

#Create companies
LOAD CSV WITH HEADERS FROM "file:///companies.csv" AS row
CREATE (p:Company {id: (row.id), name: row.name})

#Create contracts
LOAD CSV WITH HEADERS FROM "file:///contracts.csv" AS row
CREATE (contract:Contract{id:(row.id)})

#Create constrains
CREATE CONSTRAINT ON (p:Company) ASSERT p.id IS UNIQUE
CREATE CONSTRAINT ON (contract:Contract) ASSERT contract.id IS UNIQUE

#Create relations
LOAD CSV WITH HEADERS FROM "file:///relations.csv" AS row
MATCH (company:Company { id:(row.company)}),(contract:Contract { id:(row.contract)})
CREATE (company)-[:PARTICIPATED]->(contract)


[Unsupervised fraud detection](#unsupervised)

[Association rules](#association)

    



#colusión
https://aristeguinoticias.com/1707/lomasdestacado/78-de-contratos-publicos-por-adjudicacion-directa-en-2017-por-licitacion-solo-12-cofece/
https://www.eleconomista.com.mx/empresas/Cofece-investiga-posible-colusion-en-mercado-de-higiene-20180504-0033.html


Referencias

#Estafa maestra
https://www.youtube.com/watch?v=aHMUs1cGypE&feature=youtu.be
ASF datos
http://www.asfdatos.gob.mx/

Agenda de Competencia para un ejercicio íntegro en las Contrataciones Públicas
https://www.cofece.mx/wp-content/uploads/2018/07/CPC-ContratacionesPublicas.pdf

Reporte de los datos relevantes de los contratos ingresados a CompraNet que iniciaron vigencia 2010-2019
https://sites.google.com/site/cnetuc/contrataciones
