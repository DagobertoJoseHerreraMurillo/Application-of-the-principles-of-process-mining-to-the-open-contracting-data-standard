# Application-of-the-principles-of-process-mining-to-the-open-contracting-data-standard

"This thesis is dedicated to all those who work for the cause of open government and open data. The revolution you are promoting will transform our world into a more democratic and just place for all".

##### Table of Contents  
[Introduction](#introduction)  

[Motivation](#motivation)

[Open Contracting Data Standard](#OCDS)

[Contribution](#Contribution)

[Background](#Background)


Presentar resultados de aplicación de data mining a detección de fraude, luego lo mismo con process mining y finalmente los esfuerzos por combinarlos.

[Prior Work](#PriorWork)

[Process mining](#mining)


Presentar desarrollo de meetodología

[Research questions](#question)

[Process model](#process)


Caso de México

[Data description](#data)

[Event logs](#eventLogs)

[Descriptive analsys](#descriptive)

[Graphs](#graphs)

[Impact](#impact)

[Conclusion](#conclusion)

Conclusión Aplicación al Standard y aplicación a México

Sección de recomendaciones y trabajos futuros

[References](#references)




<a name="introduction"/><br/>
**Introduction**
4 pages






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


<a name="contribution"/><br/>
**Contribution**
Fortalezas y debilidades de Data Mining y Process Mining y proponer híbrido



<a name="data"/><br/>
**Data description**

The site datos.gob.mx publishes a dataset of 300,264 open contracting procedures of the Mexican federal public administration from January 2017 to date. The systems that feed this portal are managed by the Ministry of Public Administration and the Ministry of Finance and Public Credit. The published information is the responsibility of each public institution that reports it.

<a name="eventLogs"/><br/>
**Event logs**

Chapter 4
Getting the Data

CORREGIR PORQUE ESTÁ COPIADO
The information produced by the various processes is saved in event logs. In order to use this data for process mining, it needs to be modeled into a usable format. The aspect that is most relevant in this thesis is transformation. Current ERP use big relational tables, linking different tables by using keys. For process mining however, and especially aspects beyond process discovery, it is important to have a complete view on the dataset. Therefore it is important to make sure that all required information concerning the process is combined into the event log; this is called flattening of data.


<a name="Contribution"/><br/>
**Contribution**

This thesis is to provide a mechanism for the detection of irregular behavior in contracts published under the standard of open public contracts. The idea is to develop a hybrid method that can combine the strengths of the process mining and some of the techniques of data mining that have traditionally been used in the prevention and detection of fraud.

<a name="Background"/><br/>
**Background**

<a name="PriorWork"/><br/>
**Prior Work**

<a name="mining"/><br/>
**Process mining**

"Process mining is a relative young research discipline that sits between machine learning and data mining on the one hand and process modeling and analysis on the other hand. The idea of process mining is to discover, monitor and improve real processes (i.e., not assumed processes) by extracting knowledge from event logs readily available in today’s systems" (van der Aalst, 2016, p.31).

There is a clear association between conformance checking and fraud detection, especially when fraud is conceptualized as a deviation from normal operating procedures and processes (Stoop & Oezer, 2012).

<a name="question"/><br/>
**Research questions**

How can process mining be effectively combined with other data mining techniques for the detection and prevention of threats of corruption, collusion, or anti-competitive practices in public contracting processes?

This main question can be split into the following sub-questions:

What are the main indicators or red flags that suggest the presence of any irregularity in a public contracting process?

Which functional techniques of process mining can be used in the detection of which red flags in public procurement processes and what are their benefits?

In what characteristics do the conventional techniques of data mining used in the detection of fraud resemble the functional techniques of process mining and what are the possibilities of integration of both approaches in the detection of which red flags in public procurement processes?

How could a hybrid model (process mining + data mining) be used to detect red flags in public procurement processes in accordance with the characteristics of the Open Contracting Data Standard?

<a name="process"/><br/>
**Process model**


Business similarities between suppliers: Common addresses, personnel, phone numbers






<a name="descriptive"/><br/>
**Descriptive analsys**

<a name="impact"/><br/>
**Impact**

<a name="conclusion"/><br/>
**Conclusion**

<a name="references"/><br/>
**References**

Stoop, J., & Oezer, T. (2012). Process Mining and Fraud Detection.
