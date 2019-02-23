# Application-of-the-principles-of-process-mining-to-the-open-contracting-data-standard

##### Table of Contents  
[Introduction](#introduction)  

[Process model](#process)

[Data description](#data)

[Descriptive analyss](#descriptive)

[Graphs](#graphs)

Guia sobre cómo abrir
https://medium.com/neo4j/neo4j-get-off-the-ground-in-30min-or-less-3a226a0d48b1
Guía sobre cómo cargar
https://neo4j.com/graphgist/importing-csv-files-with-cypher

#Create companies
LOAD CSV WITH HEADERS FROM "file:///companies.csv" AS row
CREATE (p:Company {id: toInt(row.id), name: row.name})

#Create contracts
LOAD CSV WITH HEADERS FROM "file:///contracts.csv" AS row
CREATE (contract:Contract{id:toInt(row.id)})


[Unsupervised fraud detection](#unsupervised)

[Association rules](#association)

    
<a name="introduction"/>
##Introduction
