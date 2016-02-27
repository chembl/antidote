---
title: Open Science Prize Proposal
layout: post
author: mmmnow
permalink: /open-science-prize-proposal/
source-id: 1ks336AbZFJNqfBRmHpft5Ks8s8ZFgSNTFbDbVo3OT0E
published: true
---
# Antidote: An open platform for data-driven drug discovery applications

![image alt text]({{ site.url }}/public/pxkC3t6a973mMOBc8jINA_img_0.png)

**George Papadatos (****GP)****1****, Micha****l**** Nowotka (MN)****1****, Nathan Brown (NB)****2****, Greg Landrum (GL)****3**** and Patrick Walters (PW)****4**

**1**** ****EMBL-EBI**

**2**** The Institute of Cancer Research, London**

**3**** T5 Informatics and KNIME**

**4**** ****Vertex Pharmaceuticals**

**Deadline: 29th February 2016 11.59pm GMT**

## Proposal Requirements

* Case for support: word, pdf or html format

    * 15K characters (excluding spaces) ( i.e. 5 A4 pages roughly)

    * Brevity is strongly encouraged

* Case for support should:

    * Describe the proposed tool, technology or service;

    * Highlight how the proposed tool would utilise existing open content and data and advance the goals of Open Science;

    * Provide web links to any existing prototype or other online presence of the innovation;

    * Briefly describe their targets for developing the innovation if the team is successful in Phase I prize;

    * Outline if, how and under what license the outputs (including any computer code) would be made available to the wider public.

* **Optional**: letter of intent - DONE

* Links to prototype or other online presence

* Optional: Up to three pieces of media

    * videos, graphics, animations

## Executive Summary

**Vision: **we propose XX, an open source, state-of-the-art, end-to-end platform which enables the complete life cycle of data acquisition, curation, storage, mining, dissemination and reuse for chemoinformatics and drug discovery applications. Specifically, the resource combines *open* chemical, pharmacological and chemogenomics data and analogous in-house data with *open source* chemoinformatics and data science tools, and interactive demos, tutorials, documentation and use-cases to produce a free, end-to-end, accessible, and intuitive platform for data-driven drug discovery. We envisage that this will catalyse and facilitate i) academic and collaborative drug discovery; ii) teaching, learning and dissemination of data science applications for drug discovery to all levels of the scientific community; iii) reproducibility and sharing of research; iv) synergy between different institutions and domain experts; and v) accessibility for those from non-computational disciplines to adopt and employ computational methods.

**Implementation:** As an existing early-stage prototype, we will use myChEMBL, which was co-developed by members of our team at the EBI. myChEMBL is a virtual machine which hosts the ChEMBL database and a number of data analysis tools. We plan to heavily extend and scale-up myChEMBL by combining existing open data content, established open source chemoinformatics tools, data science and analytics technologies, as well as data curation and querying web platforms and applications built by members of our team. Importantly, the resulting platform will be modular, scalable and accessible via several deployment methods.

**Audience:** We envisage that XX will be a widely adopted platform in both academia and industry and among researchers of diverse backgrounds and experience, ranging from students to experts and from wet-lab scientists to computational ones. Particularly, we expect that XX will become indispensable to institutions with limited resources, such as academia, not-for-profit organisations, research institutes in developing economies, SMEs, CROs and biotechs.

## Description

XX will be an open and standalone environment that will support the drug discovery data life cycle, from data deposition and curation to data storage, mining and dissemination. Specifically, XX will allow users to:

* Query locally stored and hosted, high impact open data repositories, such as ChEMBL, SureChEMBL, and PubChem

* Optionally store and query additional open chemical and chemogenomics databases, such as ZINC and BindingDB or even subsets of virtual compound libraries, such as GDB17

* Standardise, curate and register compounds extracted from user-provided files or documents in a web-based platform

* Use web-based and graphical interfaces, such as IPython Notebooks, Kibana and KNIME for data analytics 

* Perform scientific computing and machine learning tasks, powered by the established Python scientific stack, which includes IPython, NumPy, scikit-learn, pandas, and seaborn

* Perform chemoinformatics tasks, powered by the RDKit open source cheminformatics library

* Reuse and learn with an unprecedented number of data science and drug discovery interactive IPython Notebooks tutorials, demos, examples and use cases, covering chemoinformatics, compound standardisation, data mining, machine learning, visualisation and drug discovery applications, such as virtual screening, target validation and lead optimisation.

![image alt text]({{ site.url }}/public/pxkC3t6a973mMOBc8jINA_img_1.png)

![image alt text]({{ site.url }}/public/pxkC3t6a973mMOBc8jINA_img_2.png)

In more detail, the proposed system architecture will consist of ten layers, listed below:

* The **data acquisition layer** is responsible for provisioning a local instance of a data source. The latter may be a public domain chemical or bioactivity database containing data extracted from the scientific literature (such as ChEMBL, PubChem and BindingDB), chemistry data extracted patent documents (SureChEMBL), large virtual compound libraries, such as GDB-17, or even user-provided chemistry data either from an internal database or automatically extracted from files or documents by text-mining.

* The data acquired by the first layer is then transferred to the **data persistency layer**, which is intended to store data by employing different storage technologies. Each of the storage engines used has different characteristics and advantages; for example, MongoDB is suited for storing a large amounts of homogenous data to quickly perform searching and filtering tasks, Neo4j allows mining data as relations between different entities, while relational databases such as Postgres are widely adopted by open content providers. 

* The purpose of the **data integration layer **is to provide a single coherent interface to query the data in the persistency layer and to ensure that all the data is synchronised across all the different storage engines. Such an interface can be provided using various data abstraction technologies. 

* The data stored in the persistency layer is constantly being checked by the number of automated processes from the **data validation layer**. The goal of this layer is to make sure that the underlying data meet certain criteria, for example that all compounds are standardised, textual data is checked for possible spelling errors using special dictionaries/ontologies, important references to external resources are valid and up to date.

* As there are still a number of issues that cannot be addressed by an automated process, the **curation interface layer** provides a user friendly, web-based interface which enable curators to check and fix issues flagged by the data validation layer.

* Once the data are appropriately curated and stored, they can be exposed in a number of ways. The **data querying layer** will provide data using different protocols, formats and dialects. Those include traditional Structured Query Language (SQL), Resource Description Framework Query (RDF) language for exploring predicate knowledge, Cypher language for relationship mining and REST architecture to support rapid web application development.

* Data exposed in the previous layer are then consumed by a number open platforms **data analytics frameworks layer**. Such platforms such as KNIME, Kibana and IPython Notebooks users to intuitively create complex scientific data processing pipelines and and efficiently mine the underlying data.

* The **scientific computing layer** provides the necessary scientific modules and libraries to perform the computation, chemoinformatics and visualisation tasks used in data processing pipelines defined in the previous layer. The tools will include RDKit, scikit-learn, numpy, scipy and seaborn.  

* The **data modelling layer** interprets results provided by the previous layer, in order to and perform tasks such as classification, regression, association rule learning, etc. Machine learning models, created by this layer can then be used to prioritise compounds, or predict targets for further investigation.

* Finally, the **deployment layer **encapsulates all above layers into a standalone, scalable container. The latter can then be deployed on multiple hardware platforms ranging from a Raspberry Pi to a standard desktop PC or Mac, or be hosted in a cloud infrastructure.

Critically, all output, including the source code and content will be provided under the open and permissive Apache and CC-BY-SA licenses, respectively. The project codebase and documentation will be hosted on GitHub.

## Advancement of Open Science and Impact

As a response to a current plethora of open chemical and chemogenomics resources, there has been a steep rise in the number of cutting-edge computing, (chemo)informatics, data curation and integration and data science resources and methodologies applied to the domain of drug discovery in the last 10 years. Nevertheless, these methodologies and tools have been developed and used in isolation; they are often opaque, undocumented or proprietary; moreover, they oftentimes depend on commercial software or infrastructure which renders them inaccessible to most academics and researchers in the drug discovery community; as an immediate result, reproducibility, dissemination, and thus progress, is hindered. Moreover, although a plethora of public domain drug discovery repositories exists, they are disparate and often not readily amenable to large-scale data integration and mining which can provide crucial novel insights. In addition to the fragmentation in tools and resources, wet lab scientists such as chemists and biologists are currently struggling to keep up with new technologies and the data deluge produced and published on a daily basis. 

We aim to bridge the information gap and democratise access to drug discovery data and data mining infrastructure and methodologies. Therefore, we propose XX, an open source, state-of-the-art, centralised, end-to-end platform which enables and supports the complete life cycle of data acquisition, curation, storage, mining, sharing and reuse for chemoinformatics and data-driven drug discovery applications. Furthermore, XX will provide access to an unprecedented number of web-based, user-friendly tutorials, demos and use-cases that highlight the multiple ways to interact and interrogate the underlying data for key steps in the drug discovery pipeline. Because the tutorials and demos themselves will also be open, they serve as good starting points for scientists who wish to build upon or extend the tools provided by XX.

We believe that XX will address the issues stated above by strictly adhering to the principles of Open Science, i.e. openness, transparency, reproducibility, accessibility and dissemination to all levels of the community. In more detail, XX has the following features by design:

* Completely free and open: XX effectively repackages widely adopted open data content and and open source tools and libraries, hosted on an open infrastructure with no dependencies on proprietary or commercial products. Therefore, XX removes the expensive licensing costs often associated with drug discovery data content and chemoinformatics software applications.

* Accessibility, ease of use and versatility: Due to the availability of interactive, web and GUI-based tools, XX will require no prior programming knowledge or experience. It also removes the often cumbersome technical burden to configure, update and maintain the data content or software libraries. However, XX will also provide a programmatic interface to facilitate integration with other systems.  

* Learning: XX will provide a versatile platform for learning chemical and biological data mining and chemoinformatics in an intuitive and straightforward way. The combination of data with relevant preinstalled and preconfigured tools along with the availability of interactive, user-friendly web and GUI-based tutorials will effectively lower the 'activation barrier' for learning. This will make XX an attractive platform to new audiences, including students, young researchers, and amateur and senior scientists alike. 

* Training: Featuring a plethora of web-based, interactive tutorials, demos and use cases out of the box, XX will be an invaluable platform for educators and trainers to host, reuse and further develop engaging training material on the use of widely popular tools and methods in the field of chemoinformatics and data-driven drug discovery.

* Application development and reuse: It is anticipated that XX will become the open source gold-standard among chemoinformatics platforms. The data and source code will be available for all XX applications and IPython Notebooks, so aspiring developers and researchers can easily reuse data, demos and code for novel data-driven drug discovery applications, thus improving the quality of open resources. 

* Reproducibility and sharing: XX offers an all-in-one platform where that all the data, and libraries are transparently standardised, repackaged and preconfigured. Novel chemoinformatics workflows, data mining algorithms and machine learning models can be developed and validated in-house and then seamlessly deployed, reproduced and repurposed in a different instance of XX run by a collaborator.

* Synergy: the existence of cutting-edge and innovative informatics and data science technologies in XX, coupled with several deployment options available will open the field to different domain experts, such as the machine learning or information retrieval communities, thus allowing a novel knowledge osmosis among them. This in turn will increase the chemoinformatics impact and visibility in community projects and challenges such as the DREAM challenges.

In particular, we anticipate the XX will have a critical impact in the following sectors and audiences:

* Academic drug discovery: Academic drug discovery is expanding rapidly in terms of number of students, researchers and research output and yet it is quite limited in data and informatics resources and support compared to its industrial counterpart. XX will provide a centralised resource for compound registration, curation, storage and bioactivity mining, thus minimising duplication of effort and allowing all researchers access to the same standardised tools, methods and data; this is certainly lacking from many academic departments at the moment. A large number of experiments and steps typically involved in the contemporary drug discovery pipeline, such as target validation, virtual screening, library, mode-of-action deconvolution, novelty detection, activity and property modelling, lead optimisation and adverse drug reaction prediction will be seamlessly supported and showcased using the extant content, tools and tutorials of XX. Furthermore, the availability of web-based, transparent and user-friendly tutorials, demos and use-cases that highlight the multiple ways to interact and interrogate the underlying data in the context of drug discovery. The impact of XX will become even more evident in drug discovery projects led by research institutes in emerging economies, wherein the budget for informatics and data analysis resources is effectively non-existent.

* Neglected tropical disease (NTD) community and charity organisations: The increase in the amount of funding against NTDs worldwide has lead to a surge in the number of NTD drug discovery projects and non-profit organisations and initiatives such as the Open Source Malaria (OSM) consortium and the Medicines for Malaria Venture (MMV) with many collaborators and groups around the earth. For example, OSM has been very productive in synthesising and testing new antimalarial lead compounds; XX would be an indispensable tool to them for compound curation and integration with other sources, along with chemoinformatics analyses. Both OSM and MMV will be given access to evaluate and test the XX platform.

* SMEs and CROs. SMEs and CROs typically operate in collaboration or partnership with other organisations and thus could directly benefit from a robust, cloud-based platform in order to register, manage and share compounds and analysis outcomes with partners and peers.

## Innovation and Originality

There have been few attempts in the community to package open infrastructure along with software libraries and tools. For example, BioLinux is a virtual machine based on the Ubuntu operating system which packages a large number of command-line and GUI-based tools and can serve as a workstation for running bioinformatics-related applications and tasks. BioLinux was pioneering work; however it is a collection of diverse tools, without tutorials or use cases on their effective usage. Furthermore, there is no focus on drug discovery or open data, while information on current maintenance and support is not clear. On the other hand, BioClipse is a free, plugin-based workbench based on the Eclipse environment which supports chemoinformatics and drug discovery tasks. Similar to BioLinux, there is no focus on access and reuse of open data or provision of integrated use cases, while active development has ceased for several years.

Compared to these existing solutions, the innovation and originality in XX lies in the following key features:

* Seamless integration of open and widely established data and informatics tools, along with tutorials and real-world data mining and drug discovery use-cases

* Intuitive, web-based interfaces based on modern technologies for ease of use

* Different ways to access and utilise the platform, for different user specifications, as opposed to an 'one-size-fits-all' approach

## Technological viability and resource feasibility

XX will be based on myChEMBL as an existing, working prototype. myChEMBL is a virtual machine which hosts the ChEMBL database and a number of data analysis tools and has been a successful proof-of-concept for the viability and success of the seamless integration of open, widely established and robust technologies, tools and platforms, such as PostgreSQL, Python, Django, RDKit, KNIME and IPython Notebooks.

During the six months of Phase I, we plan to extend and broaden the scope of myChEMBL with the following five steps:

1. Add further existing open data content, such as  the SureChEMBL database of patent chemistry, and further develop the backend algorithms to provide real-time search performance on the increased volume of data

2. Add and test new web-based interfaces for data curation and standardisation which we have developed in-house

3. Introduce cutting-edge data mining and analytics technologies, such as Neo4j and Elastic Search for the existing data resources

4. Complement the above with new IPython Notebook and KNIME tutorials, and data-driven drug discovery examples and use cases

5. Introduce new deployment options of XX by adding cloud-based support and Docker containerisation

Crucially, our team has significant first-hand expertise and experience in the science, technologies, web interfaces and resources that will be employed during Phase I and has already developed working prototypes and proofs-of-concept for several of them. 

Moreover, during Phase I we are planning to engage the community as much as possible in the following ways:

1. Host the project as a GitHub repository

2. Provide regular updates on progress via blog posts and social media

3. Organise and participate in outreach activities, webinars and conference presentations

4. Prepare and submit a publication in an open-access peer-reviewed journal, such as NAR Database

5. Make XX available to the community for testing and feedback at the end of Phase I

Our team has collaborators in three different countries, each providing their unique expertise and access to resources to this project. Overall, we have substantial experience with open chemogenomics data, web applications, open chemoinformatics tools and data science and informatics applications both in an academic and an industrial drug discovery setting. GP and MN (EMBL-EBI, UK) are responsible for the data integration and further development of highly impactful open data repositories, such as ChEMBL and SureChEMBL, as well as web-based platforms and chemoinformatics tools such as Beaker and the Curation Interface which we plan to integrate to XX. NB (ICR, UK) currently leads a computational medicinal chemistry group that supports academic drug discovery and has had major contributions in chemoinformatics research and has had demonstrable impact in drug design projects leading to a number of preclinical candidates and first-in-man clinical trials. GL (T5 Informatics and KNIME, Switzerland) is the main developer of the RDKit chemoinformatics toolkit and has extensive expertise in chemical informatics, machine learning, and data integration in an industrial setting. Finally, PW (Vertex, US) currently leads a research informatics team to support drug discovery and also has extended expertise in chemoinformatics and machine learning.

With regard to the allocation of tasks and responsibilities, the main code development and project management will take place at the EMBL-EBI by GP and MN, in consultation with GL and PW. GL will ensure that the RDKit core provides the high-performance algorithms to support the core chemoinformatics requirements of XX. GL and PW will develop and test new tutorials, use cases and bespoke chemoinformatics software; furthermore, they will extensively test XX during the stages of development. Finally, GL and PW will provide feedback and modifications during the deployment of the system in different environments and settings. All contributors will be involved in outreach activities and publications outputs.

The estimated budget for Phase I is listed below:

<table>
  <tr>
    <td>Category</td>
    <td>Cost Estimate</td>
  </tr>
  <tr>
    <td>Salary costs for software development</td>
    <td>$50,000.00</td>
  </tr>
  <tr>
    <td>Project management costs</td>
    <td>$12,000.00</td>
  </tr>
  <tr>
    <td>Research student stipends</td>
    <td>$5,000.00</td>
  </tr>
  <tr>
    <td>Infrastructure and maintenance</td>
    <td>$5,000.00</td>
  </tr>
  <tr>
    <td>Outreach and travel costs</td>
    <td>$5,000.00</td>
  </tr>
  <tr>
    <td>Publication costs</td>
    <td>$1,000.00</td>
  </tr>
  <tr>
    <td>Meeting costs</td>
    <td>$2,000.00</td>
  </tr>
  <tr>
    <td>Total:</td>
    <td>$80,000.00</td>
  </tr>
</table>


**Another way of depicting the architecture**

This is done as a sketch first, to see if it resonates with you.

![image alt text]({{ site.url }}/public/pxkC3t6a973mMOBc8jINA_img_3.png)

This is more compact than how we currently have the thing drawn, but conveys much the same information. Individual technologies can be called out (with logos… I think those are great) next to/under the relevant pieces of the diagram.

