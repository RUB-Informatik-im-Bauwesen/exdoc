Markdown documentation created by [pyLODE](http://github.com/rdflib/pyLODE) 2.4

# Extension for document types for the ISO 21597 ICDD Part 1 Container ontology [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.5903118.svg)](https://doi.org/10.5281/zenodo.5903118) 

## Metadata
* **IRI**
  * `https://w3id.org/exdoc`
* **Publisher(s)**
  * [Lehrstuhl Informatik im Bauwesen](http://www.inf.bi.rub.de)
* **Creators(s)**
  * [Philipp Hagedorn](https://orcid.org/0000-0002-6249-243X)
    [[ORCID]](https://orcid.org/0000-0002-6249-243X)
    (<philipp.hagedorn-n6v@rub.de></a>) of [Ruhr University Bochum](https://www.inf.bi.ruhr-uni-bochum.de/iib/lehrstuhl/mitarbeiter/philipp_hagedorn.html.en)
* **Modified**
  * 2022-08-02
* **Issued**
  * 2021-05-08
* **Version Information**
  * v0.4
* **License &amp; Rights**
  * [https://creativecommons.org/licenses/by/4.0/](https://creativecommons.org/licenses/by/4.0/)
  * &copy; 2022 by Chair of Computing in Engineering, Ruhr University Bochum
* **Source**
  * [https://github.com/RUB-Informatik-im-Bauwesen/exdoc](https://github.com/RUB-Informatik-im-Bauwesen/exdoc)
* **Ontology RDF**
  * RDF ([https://rub-informatik-im-bauwesen.github.io/exdoc/ExtendedDocument.ttl](turtle))
  * RDF ([https://rub-informatik-im-bauwesen.github.io/exdoc/ExtendedDocument.rdf](RDF/XML))
  * RDF ([https://rub-informatik-im-bauwesen.github.io/exdoc/ExtendedDocument.nt](N-Triples))
  * RDF ([https://rub-informatik-im-bauwesen.github.io/exdoc/ExtendedDocument.jsonld](JSON-LD))

## Description
<p>This ontology provides an extension for document types for the <a href="https://www.iso.org/standard/74389.html">ISO 21597 ICDD Part 1</a>  Container ontology <code>ct: &lt;</code><a href="https://standards.iso.org/iso/21597/-1/ed-1/en/Container.rdf">https://standards.iso.org/iso/21597/-1/ed-1/en/Container#</a><code>&gt;</code>.</p>
<p>The preferred namespace prefix is <code>exdoc</code> for the namespace IRI <a href="https://w3id.org/exdoc">https://w3id.org/exdoc</a>.  </p>
<p>It includes the <a href="#ExternalDatabase">ExternalDatabase</a> class as a subclass of the <code>ct:ExternalDocument</code>. This class can be used to provide information and connection details from an existing relational database, e.g., to retrieve data from DB and convert it into payload triples using R2RML mappings (see <a href="https://www.w3.org/TR/r2rml/">W3C R2RML Recommendation</a>). When working with databases in ICDD container, be sure you do not store credentials for the database in the connection string but in a secure credentials store. </p>
<p>It also includes the <a href="#PayloadProxy">PayloadProxy</a> class as a subclass of the <code>ct:ExternalDocument</code> class for registering payload triples from the "payload triples" folder. Instances of these classes can be used to define link elements for RDF-based data in ICDD containers.</p>

## History Note:
<p>v0.4: adding <code>PayloadProxy</code> class</p>
<p>v0.3: adding <code>databaseMapping</code> reference</p>
<p>v0.2: adding <code>databaseType</code> and <code>databaseQueryLanguage</code></p>
<p>v0.1: initial ontology</p>

## Namespaces
* **default (:)**
  * `https://w3id.org/exdoc#`
* **dc**
  * `http://purl.org/dc/terms/`
* **exdoc**
  * `https://w3id.org/exdoc#`
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
