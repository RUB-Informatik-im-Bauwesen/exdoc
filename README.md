Markdown documentation created by [pyLODE](http://github.com/rdflib/pyLODE) 2.4

# Extension for document types for the ISO 21597 ICDD Part 1 Container ontology [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.5903118.svg)](https://doi.org/10.5281/zenodo.5903118) 

## Metadata
* **IRI**
  * `https://icdd.vm.rub.de/ontology/icdd/ExtendedDocument`
* **Publisher(s)**
  * [Chair of Computing in Engineering, Ruhr University Bochum](https://www.inf.bi.rub.de)
* **Creators(s)**
  * [Philipp Hagedorn](https://orcid.org/0000-0002-6249-243X)
    [[ORCID]](https://orcid.org/0000-0002-6249-243X)
    (<philipp.hagedorn-n6v@rub.de></a>) of [Ruhr University Bochum](https://www.inf.bi.ruhr-uni-bochum.de/iib/lehrstuhl/mitarbeiter/philipp_hagedorn.html.en)
* **Modified**
  * 2021-12-13
* **Issued**
  * 2021-05-08
* **Version Information**
  * v0.3
* **License**
  * [https://creativecommons.org/licenses/by/4.0/](https://creativecommons.org/licenses/by/4.0/)
* **Ontology RDF**
  * RDF ([ExtendedDocument.ttl](turtle))
  * RDF ([ExtendedDocument.rdf](RDF/XML))
* **Code Repository**
  * [https://github.com/RUB-Informatik-im-Bauwesen/exdoc](https://github.com/RUB-Informatik-im-Bauwesen/exdoc)
### Description
<p>This ontology provides an extension for document types for the <a href="https://www.iso.org/standard/74389.html">ISO 21597 ICDD Part 1</a>  Container ontology <code>ct: &lt;</code><a href="https://standards.iso.org/iso/21597/-1/ed-1/en/Container.rdf">https://standards.iso.org/iso/21597/-1/ed-1/en/Container#</a><code>&gt;</code>.</p>
<p>The preferred namespace prefix is <code>exdoc</code> for the namespace IRI <a href="https://icdd.vm.rub.de/ontology/icdd/ExtendedDocument">https://icdd.vm.rub.de/ontology/icdd/ExtendedDocument</a>.  It includes the <a href="#ExternalDatabase">ExternalDatabase</a> class as a subclass of the ct:ExternalDocument.</p>
<p>This class can be used to provide information and connection details from an existing relational database, e.g., to retrieve data from DB and convert it into payload triples using R2RML mappings (see <a href="https://www.w3.org/TR/r2rml/">W3C R2RML Recommendation</a>). When working with databases in ICDD container, be sure you do not store credentials for the database in the connection string but in a secure credentials store. </p>

### History Note:
<p>v0.3: adding <code>databaseMapping</code> reference</p>
<p>v0.2: adding <code>databaseType</code> and <code>databaseQueryLanguage</code></p>
<p>v0.1: initial ontology</p>

## Table of Contents
1. [Classes](#classes)
1. [Object Properties](#objectproperties)
1. [Datatype Properties](#datatypeproperties)
1. [Namespaces](#namespaces)
1. [Legend](#legend)


## Classes
[External Database](#ExternalDatabase),
### External Database
Property | Value
--- | ---
IRI | `https://icdd.vm.rub.de/ontology/icdd/ExtendedDocument#ExternalDatabase`
Description | <p>This class is a proxy document referencing to an external data source with a connection string. An optional mapping file can be stored within the container as a <code>ct:Document</code>. The  referenced document must be formatted according to the <a href="https://www.w3.org/TR/r2rml/">W3C R2RML Recommendation</a>. When working with databases in ICDD container, be sure you do not store credentials for the database in the connection string but in a secure credentials store.</p>
Super-classes |[ct:ExternalDocument](https://standards.iso.org/iso/21597/-1/ed-1/en/Container#ExternalDocument) (c)<br />
Restrictions |[exdoc:databaseType](databasetype) (dp) **exactly** 1<br />[exdoc:databaseMapping](databasemapping) (op) **max** 1<br />[exdoc:databaseName](databasename) (dp) **exactly** 1<br />[exdoc:databaseConnectionString](connectionstring) (dp) **exactly** 1<br />[exdoc:databaseQueryLanguage](querylanguage) (dp) **exactly** 1<br />
In domain of |[exdoc:databaseName](databasename) (dp)<br />[exdoc:databaseMapping](databasemapping) (op)<br />[exdoc:databaseConnectionString](connectionstring) (dp)<br />[exdoc:databaseType](databasetype) (dp)<br />

## Object Properties
[database mapping](#databasemapping),
[](databasemapping)
### database mapping
Property | Value
--- | ---
IRI | `https://icdd.vm.rub.de/ontology/icdd/ExtendedDocument#databaseMapping`
Description | The reference to a mapping file, which allows for the generation of structured RDF-based data from the specified database. This file also needs to be specified within the respective container.
Domain(s) |[exdoc:ExternalDatabase](ExternalDatabase) (c)<br />
Range(s) |[ct:Document](https://standards.iso.org/iso/21597/-1/ed-1/en/Container#Document) (c)<br />

## Datatype Properties
[connection string](#connectionstring),
[database name](#databasename),
[query language](#querylanguage),
[database type](#databasetype),
[](connectionstring)
### connection string
Property | Value
--- | ---
IRI | `https://icdd.vm.rub.de/ontology/icdd/ExtendedDocument#databaseConnectionString`
Description | A database connection string is a string that specifies information about a data source and the means of connecting to it from an ICDD. It can be passed to an underlying driver or provider in order to initiate the connection. Warning: The connection string holds sensitive information.
Example | ````Server=myServerAddress;Database=myDataBase;Trusted_Connection=True;`<br />```
Domain(s) |[exdoc:ExternalDatabase](ExternalDatabase) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](databasename)
### database name
Property | Value
--- | ---
IRI | `https://icdd.vm.rub.de/ontology/icdd/ExtendedDocument#databaseName`
Description | The database name is used to adress the correct mapping from the mapping file to a certain database within the connection string.
Super-properties |[ct:name](https://standards.iso.org/iso/21597/-1/ed-1/en/Container#name)<br />
Domain(s) |[exdoc:ExternalDatabase](ExternalDatabase) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](querylanguage)
### query language
Property | Value
--- | ---
IRI | `https://icdd.vm.rub.de/ontology/icdd/ExtendedDocument#databaseQueryLanguage`
Description | The query language, which can be used to retrieve information from the specified database.
Example | ````SQL, XQuery`<br />```
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](databasetype)
### database type
Property | Value
--- | ---
IRI | `https://icdd.vm.rub.de/ontology/icdd/ExtendedDocument#databaseType`
Description | The type of database that is specified, e.g. MySQL, NoSQL, and others.
Example | ````MSSQL, MySQL, NoSQL`<br />```
Domain(s) |[exdoc:ExternalDatabase](ExternalDatabase) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />

## Named Individuals
## Namespaces
* **default (:)**
  * `https://icdd.vm.rub.de/ontology/icdd/ExtendedDocument#`
* **ct**
  * `https://standards.iso.org/iso/21597/-1/ed-1/en/Container#`
* **dc**
  * `http://purl.org/dc/terms/`
* **exdoc**
  * `https://icdd.vm.rub.de/ontology/icdd/ExtendedDocument#`
* **foaf**
  * `http://xmlns.com/foaf/0.1/`
* **owl**
  * `http://www.w3.org/2002/07/owl#`
* **prov**
  * `http://www.w3.org/ns/prov#`
* **rdf**
  * `http://www.w3.org/1999/02/22-rdf-syntax-ns#`
* **rdfs**
  * `http://www.w3.org/2000/01/rdf-schema#`
* **sdo**
  * `https://schema.org/`
* **skos**
  * `http://www.w3.org/2004/02/skos/core#`
* **vann**
  * `http://purl.org/vocab/vann/`
* **voaf**
  * `http://purl.org/vocommons/voaf#`
* **xml**
  * `http://www.w3.org/XML/1998/namespace`
* **xsd**
  * `http://www.w3.org/2001/XMLSchema#`

## Legend
* Classes: c
* Object Properties: op
* Functional Properties: fp
* Data Properties: dp
* Annotation Properties: dp
* Properties: p
* Named Individuals: ni
