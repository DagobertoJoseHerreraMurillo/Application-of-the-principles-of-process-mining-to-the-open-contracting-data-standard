# Application-of-the-principles-of-process-mining-to-the-open-contracting-data-standard

"This thesis is dedicated to all those who work for the cause of open government and open data. The revolution you are promoting will transform our world into a more democratic and just place for all".

##### Table of Contents  
[Introduction](#introduction)  

[Motivation](#motivation)

[Open Contracting Data Standard](#OCDS)

[Contribution](#Contribution)

[Background](#Background)

[Prior Work](#PriorWork)

[Process model](#process)

[Data description](#data)

[Descriptive analsys](#descriptive)

[Graphs](#graphs)

[Impact](#impact)

[Conclusion](#conclusion)




<a name="introduction"/><br/>
**Introduction**







<a name="motivation"/><br/>
**Motivation**

Governments are active protagonist of the data explosion that in recent years has radically modified the way we live. The Open Data movement seeks that governments and public authorities around the world to publish machine readable data under licenses that allow for unrestricted use, redistribution, modification, separation, compilation, propagation and application to any purpose without charge and without discrimination against any person or group (Open Knowledge Foundation).
Every year, governments devote gigantic amounts of money to public contracts, from papers and pencils to large infrastructure projects such as airports, roads, schools and hospitals. The size of public procurement represents approximately 12% of GDP in OECD countries (OECD, 2017). This significant volume of resources along with the complex interaction between public and private interests exposes the public contracting processes to multiple risks of waste, inefficiency, fraud, corruption, and uncompetitive practices throughout the whole procurement life-cycle.



<a name="OCDS"/><br/>
**Open Contracting Data Standard**

“Open contracting involves the full chain of government deal-making, from concessions of natural resources to procurement of goods, works, and services for citizens. It starts at the planning stage, and covers tenders, awarding, and implementation of all public contracts” (Open Contracting Partnership). 

Structured and standardized data about public contracting can help stakeholders to:

> *	deliver better value for money for governments,
> *	create fairer competition and a level playing field for business,
> *	drive higher-quality goods, works, and services for citizens,
> *	prevent fraud and corruption,
> *	promote smarter analysis and better solutions for public problems.

The access open to contracting data builds trust and allows to create mechanisms to ensure that the astronomical sums of money spent by governments each year translate into better goods, services, and infrastructure projects for the direct benefit of citizens.


<a name="data"/><br/>
**Data description**

The site datos.gob.mx publishes a dataset of 300,264 open contracting procedures of the Mexican federal public administration from January 2017 to date. The systems that feed this portal are managed by the Ministry of Public Administration and the Ministry of Finance and Public Credit. The published information is the responsibility of each public institution that reports it.


<a name="Contribution"/><br/>
**Contribution**

This thesis is to provide a mechanism for the detection of irregular behavior in contracts published under the standard of open public contracts. The idea is to develop a hybrid method that can combine the strengths of the process mining and some of the techniques of data mining that have traditionally been used in the prevention and detection of fraud.

<a name="Background"/><br/>
**Background**

<a name="PriorWork"/><br/>
**Prior Work**

<a name="process"/><br/>
**Process model**

<a name="descriptive"/><br/>
**Descriptive analsys**

<a name="impact"/><br/>
**Impact**

<a name="conclusion"/><br/>
**Conclusion**



























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
