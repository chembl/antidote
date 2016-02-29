---
title: Open Science Prize Proposal
layout: post
author: mmmnow
permalink: /open-science-prize-proposal/
source-id: 1ks336AbZFJNqfBRmHpft5Ks8s8ZFgSNTFbDbVo3OT0E
published: true
---
# Antidote: An open platform for chemoinformatics and data-driven drug discovery applications

![image alt text]({{ site.url }}/public/pxkC3t6a973mMOBc8jINA_img_0.png)

[http://chembl.github.io/antidote/](http://chembl.github.io/antidote/)

## Executive Summary

**Vision:** we propose [Antidote](http://chembl.github.io/antidote/), an open source, state-of-the-art, end-to-end platform which enables the complete life cycle of compound data acquisition, curation, storage, querying, mining, dissemination and reuse for chemoinformatics and drug discovery applications. Specifically, Antidote combines *open* chemical, pharmacological and chemogenomics data and analogous in-house data with *open source* chemoinformatics and data science and mining tools, along with interactive demos, tutorials, documentation and drug discovery use-cases in a *free*, *accessible* and *intuitive* platform. We envisage that this will catalyse and facilitate i) academic drug discovery *via* easy access to standardised infrastructure, data and use-cases; ii) accessibility and dissemination of modern informatics and computational applications for data-driven drug discovery to all levels of the scientific community; iii) interactive teaching and learning of chemoinformatics and data mining concepts and applications; iv) reproducibility and sharing of research methodologies and outcomes; and v) synergy and collaborations between different institutions and domain experts outside drug discovery.

**Implementation:** As an existing early-stage prototype, we use [myChEMBL](http://www.mdpi.com/2078-1547/5/2/334/htm), which was co-developed by members of our team at the EBI. myChEMBL is a virtual machine which hosts the [ChEMBL](https://www.ebi.ac.uk/chembl/) database and a number of data analysis tools. We plan to heavily extend and scale-up myChEMBL by combining existing open data content, open source data mining and analytics technologies, as well as user-friendly data curation and querying web platforms and applications built by members of our team. Importantly, the resulting platform will be modular, scalable and accessible via several deployment methods. 

**Audience:** We envisage that Antidote will become a widely adopted data analysis and reuse platform among researchers of diverse backgrounds and experience, ranging from students to experts and from wet-lab scientists to computational ones. Particularly, we expect that Antidote will become indispensable to institutions with limited resources, such as academia, not-for-profit organisations, and research institutes in developing economies.

## Description

[Antidote](http://chembl.github.io/antidote/) will be an open and standalone environment that will support the chemical compound data lifecycle, from acquisition, curation, storage, querying, mining, dissemination and reuse for chemoinformatics and data-driven drug discovery applications. Specifically, Antidote will allow users to:

* Access, query and reuse locally stored instances of established and impactful chemistry, pharmacology and chemogenomics open data repositories, such as [ChEMBL](https://www.ebi.ac.uk/chembl/), [SureChEMBL](https://www.surechembl.org/) and [PubChem](https://pubchem.ncbi.nlm.nih.gov/), which contain data extracted from the primary scientific and patent literature and depositions

* Optionally integrate and query additional open repositories of chemical structures and biological activities, such as [ZINC](http://zinc.docking.org/) and [BindingDB](https://www.bindingdb.org/), or even subsets of virtual compound libraries, such as [GDB-17](http://www.gdb.unibe.ch/gdb/home.html#gdb)

* Load, standardise, curate, validate and store compounds extracted from user-provided files or documents via a user-friendly, web-based compound curation interface (Figure 2)

* Leverage established web and graphical interface platforms, such as [Jupyter Notebooks](http://jupyter.org/), [Kibana](https://www.elastic.co/products/kibana) and [KNIME](https://www.knime.org/). These allow users to intuitively create and easily share complex scientific data processing pipelines and efficiently query and mine the underlying compound data and their measured and calculated properties, metadata and provenance

* Develop interactive scientific computing and machine learning applications, such as regression, classification and clustering, powered by the established Python scientific stack, which includes [IPython](http://ipython.org/), [NumPy](http://www.numpy.org/), [scikit-learn](http://scikit-learn.org/), [pandas](http://pandas.pydata.org/) and [seaborn](http://stanford.edu/~mwaskom/software/seaborn/)

* Perform chemoinformatics tasks, such as compound standardisation, fast chemistry searches and molecular property calculation, powered by the [RDKit](http://www.rdkit.org/) open source cheminformatics library

* Reuse data and methods based on a large number of interactive [Jupyter Notebooks](http://jupyter.org/) and [KNIME](https://www.knime.org/) tutorials, demos, examples and use-cases, covering chemoinformatics, data mining, machine learning, visualisation and data-intensive drug discovery applications, such as virtual screening and structure-activity relationship mining.

* Enable self-guided, interactive learning and teaching of data mining concepts and applications in drug discovery using a large number of heavily documented and interactive [Jupyter Notebooks](http://jupyter.org/) and [KNIME](https://www.knime.org/) tutorials, demos, examples and use-cases.

Antidote will be packaged and deployed in a number of ways in order to be accessible according to different user specifications and settings. Such deployments will include a virtual machine based on [Ubuntu](http://www.ubuntu.com/) or [CentOS](https://www.centos.org/) operating systems and hosted on a standard laptop with [VirtualBox](https://www.virtualbox.org/), [QEMU](http://wiki.qemu.org/Main_Page) or a lightweight [Docker](https://www.docker.com/) container or even on a remote cloud-based infrastructure, such as [OpenShift](https://www.openshift.com/) and [AWS](https://aws.amazon.com/), managed by [Vagrant](https://www.vagrantup.com/). 

The functionality listed above will be enabled by the proposed system architecture, depicted in Figure 1. 

![image alt text]({{ site.url }}/public/pxkC3t6a973mMOBc8jINA_img_1.png)

Figure 1. The proposed modular system architecture for Antidote featuring data resources and technologies for each component. 

![image alt text]({{ site.url }}/public/pxkC3t6a973mMOBc8jINA_img_2.png)

Figure 2. The Curation Interface prototype.

Critically, all output, including the source code and content will be provided under the open and permissive [Apache](http://www.apache.org/licenses/LICENSE-2.0)[ 2.0](http://www.apache.org/licenses/LICENSE-2.0) and [CC-BY-SA](https://creativecommons.org/licenses/by-sa/4.0/)[ 4.0](https://creativecommons.org/licenses/by-sa/4.0/) licenses, respectively. The project's web page, codebase and documentation will be hosted as a public repository on [GitHub](https://github.com/).

## Advancement of Open Science and Impact

As a response to a current plethora of open chemical and chemogenomics repositories, there has been a steep rise in the number of cutting-edge computing, (chemo)informatics, data curation and integration, and data science methodologies applied to the domain of drug discovery in the last 10 years. Nevertheless, these methodologies and tools have been developed and used in isolation; they are often opaque, undocumented or proprietary; moreover, they oftentimes depend on commercial software or infrastructure which renders them inaccessible to most academics and researchers in the drug discovery community; as an immediate result, reproducibility, dissemination, and thus scientific progress, is hindered. Moreover, despite the large number of public domain chemistry and bioactivity data repositories, they are disparate and often not readily amenable to large-scale data integration and mining which can provide crucial insights. In addition to the fragmentation of tools and resources, lab scientists such as chemists and biologists are currently struggling to keep up with new technologies and the data deluge produced and published on a daily basis. 

We aim to bridge the information gap and democratise access to open drug discovery data coupled with data mining infrastructure and methodologies. Therefore, we propose **Antidote**, an open source, state-of-the-art, standardised, end-to-end platform which enables and supports the complete life cycle of compound data acquisition, curation, storage, querying, mining, sharing and reuse for chemoinformatics and data-driven drug discovery applications. Furthermore, Antidote will provide access to an unprecedented number of web-based, user-friendly tutorials, demos and use-cases that highlight the multiple ways to interact and interrogate the underlying data for key steps in the drug discovery pipeline. As the tutorials and demos themselves will also be open, they serve as ideal starting points for scientists and researchers who wish to build upon or extend the tools provided.

We believe that Antidote will address the issues stated above by strictly adhering to the principles of Open Science, i.e. openness, transparency, reproducibility, accessibility and dissemination to all levels of the community. In more detail, Antidote has the following features by design:

* Completely free and open: Antidote effectively integrates and repackages widely adopted open data content and open source tools and libraries, hosted on an open infrastructure with no dependencies on proprietary or commercial products. Therefore, it removes the expensive licensing costs often associated with drug discovery data content and chemoinformatics software applications.

* Reproducibility and sharing: Antidote offers a platform where all the data and tools are transparently standardised, repackaged and preconfigured. Novel chemoinformatics workflows, data mining algorithms and machine learning models can be developed and validated by a user and then seamlessly deployed, reproduced and repurposed in a different instance of Antidote run by a collaborator or a member of the community.

* Accessibility, ease of use and versatility: Due to the availability of interactive, web and GUI-based tools, Antidote will require no prior programming knowledge or experience. It also removes the often cumbersome technical burden to configure, update and maintain the data content or software libraries. 

* Learning, teaching and training: Antidote will provide a novel platform for learning chemical and biological data mining and chemoinformatics in an intuitive and straightforward way. The combination of data with relevant preinstalled and preconfigured tools along with the availability of interactive, user-friendly web and GUI-based tutorials will smoothen the learning curve. This will make Antidote an attractive platform to new audiences, including high school students, undergraduates, early-stage researchers and senior scientists alike. For the same reasons, Antidote will be an invaluable platform for educators and trainers to host, reuse and further develop engaging training material on the use of widely popular tools and methods in the field of chemoinformatics and data-driven drug discovery.

* Application development and reuse: It is anticipated that Antidote will become the open source gold-standard among open chemoinformatics platforms. The data and source code will be available for all applications and tutorials, so aspiring developers and researchers can easily reuse data, demos and code for novel data-driven drug discovery applications. 

* Synergy: Antidote will attract experts outside the chemoinformatics and drug discovery domain, such as the machine learning and information retrieval communities, and will encourage collaborative projects and novel, interdisciplinary applications.

Furthermore, we anticipate that Antidote will have a critical impact in the following sectors and audiences:

* Academic drug discovery: Academic drug discovery is expanding rapidly in terms of number of students, researchers and research output and yet it is quite limited in data and informatics resources and support compared to its industrial counterpart. Antidote will provide a centralised resource for compound standardisation, curation, storage and biological activity mining, thus minimising duplication of effort and allowing all researchers access to the same standardised tools, methods and data; this is certainly lacking from many academic departments at the moment. A large number of experiments and steps typically involved in the contemporary drug discovery pipeline, such as target prioritisation and prediction, virtual screening, library design, biological activity modelling and lead optimisation will be seamlessly supported and showcased using the content, tools and tutorials of Antidote. Furthermore, the availability of web-based and user-friendly tutorials, demos and use-cases that highlight the multiple ways to interact and interrogate the underlying data in the context of drug discovery. The impact of Antidote will become even more evident in drug discovery projects led by research institutes in emerging economies, with limited access to specialised resources.

* Neglected tropical disease (NTD) community and charity organisations: The increase in the amount of funding against NTDs worldwide has lead to a surge in the number of NTD drug discovery projects and non-profit organisations and initiatives such as the Open Source Malaria ([OSM](http://opensourcemalaria.org/)) consortium and the Medicines for Malaria Venture ([MMV](http://www.mmv.org/)) with many collaborators and groups around the globe. For such organisations, Antidote is expected to be an indispensable tool for compound curation and integration with other sources, along with chemoinformatics analyses. 

* SMEs and CROs. SMEs and CROs typically operate in collaboration or partnership with not-for-profit and academic organisations and thus could directly benefit from a robust, cloud-based platform in order to standardise, manage and share compounds and analysis outcomes with their partners and peers.

## Innovation and Originality

There have been few attempts in the community to package open infrastructure along with software libraries and tools. For example, [BioLinux](http://environmentalomics.org/bio-linux/) is a virtual machine based on the Ubuntu operating system which packages a large number of command-line and GUI-based tools and can serve as a workstation for running bioinformatics-related applications and tasks. BioLinux was pioneering piece of work; however, it is merely a collection of diverse tools, without tutorials or use-cases on their effective usage. Furthermore, there is no focus on drug discovery or open data, while information on current maintenance and support is not clear. On the other hand, [BioClipse](http://www.bioclipse.net/) is a free, plugin-based workbench based on the Eclipse environment, which supports chemoinformatics and drug discovery tasks. Similar to BioLinux, there is no focus on access and reuse of open data or provision of integrated use-cases, while active development has ceased for several years.

Compared to these existing solutions, the innovation and originality in Antidote lies in the following four key features:

* Seamless integration of open chemistry and pharmacology data with open source informatics and data analysis tools

* Tutorials and real-world data mining and drug discovery use-cases, in a graphical and user-friendly environment

* Intuitive, web-based interfaces for the curation, validation, integration and querying of user-provided chemical structures

* Different ways to access and utilise the platform, for different user specifications and experience levels, as opposed to an 'one-size-fits-all' approach

## Technological viability and resource feasibility

Antidote will be based on myChEMBL as an existing, working prototype. myChEMBL is a virtual machine which hosts the ChEMBL database and a number of data analysis tools. It has been a very successful proof-of-concept for the viability and success of the seamless integration of open, widely established and robust technologies, tools and platforms, such as [PostgreSQL](http://www.postgresql.org/), [Python](https://www.python.org/), [Django](https://www.djangoproject.com/), [RDKit](http://www.rdkit.org/), [KNIME](https://www.knime.org/) and [IPython Notebooks](http://ipython.org/notebook.html).

During the six months of Phase I and the transition to Antidote, we plan to implement the system architecture according to Figure 1 and therefore extend and scale-up myChEMBL's scope for international adoption in the following five steps:

1. Add further existing open data content, such as the [SureChEMBL](https://www.surechembl.org/) chemistry annotations extracted from patent documents, and further develop the backend algorithms to provide real-time search performance on the increased volume of data.

2. Add and test new web-based interfaces for compound curation and standardisation which we have already developed in-house.

3. Introduce cutting-edge data analytics technologies, such as [Neo4j](http://neo4j.com/) and [Elastic Search](https://www.elastic.co/products/elasticsearch) for querying the existing data resources in novel ways.

4. Complement the above with new [Jupyter Notebooks](http://jupyter.org/) and [KNIME](https://www.knime.org/) tutorials, and data-driven drug discovery examples and use-cases, such as *de novo* compound design, bioisosteric replacement mining and structure-activity relationship analysis.

5. Introduce new deployment options to increase the accessibility and scalability of Antidote by adding support for cloud and cluster deployments, as well as [Docker](https://www.docker.com/) containerisation.

Moreover, during Phase I we are planning to engage the community as much as possible in the following ways:

1. Host the development project as a public GitHub repository.

2. Provide regular updates on progress via blog posts and social media.

3. Organise and participate in outreach activities, webinars and conference presentations.

4. Prepare and submit a publication in an open-access peer-reviewed journal, such as [NAR Database](http://nar.oxfordjournals.org/).

5. Make Antidote available to the community for testing and feedback at the end of Phase I.

Crucially, our team has many years of first-hand expertise and experience in the science, informatics and web technologies that will be employed during Phase I and has already developed working prototypes and proofs-of-concept for several of them. Furthermore, we have substantial experience with open chemogenomics data repositories, data curation, web application development, and chemoinformatics methods both in an academic and an industrial drug discovery setting. GP and MN ([EMBL-EBI](http://www.ebi.ac.uk/), UK) are responsible for the data integration and technical development of highly impactful open data repositories, such as [ChEMBL](https://www.ebi.ac.uk/chembl/) and [SureChEMBL](https://www.surechembl.org/), as well as rich web-based platforms and services, such as the ChEMBL [web services](https://www.ebi.ac.uk/chembl/api/data/docs), [Beaker](https://www.ebi.ac.uk/chembl/api/utils/docs) and the Curation Interface, which we plan to integrate to Antidote. NB ([ICR](http://www.icr.ac.uk/), UK) currently leads a computational medicinal chemistry group that supports academic drug discovery and has had demonstrable impact in drug design projects leading to a number of preclinical candidates and first-in-man clinical trials. GL ([T5 Informatics](http://www.t5informatics.com/) and [KNIME](https://www.knime.org/), Switzerland) is the main developer of the [RDKit](http://www.rdkit.org/) chemoinformatics toolkit and has extensive expertise in chemical informatics, machine learning, and data integration in an industrial setting. Finally, PW ([Vertex](http://www.vrtx.com/), US) currently leads a research informatics team to support drug discovery and has extensive expertise in chemoinformatics and machine learning.

With regard to the allocation of tasks and responsibilities, the main code development and project management will be coordinated and overseen by GP and MN at the EBI, in consultation with NB, GL and PW. GL will ensure that RDKit provides the high-performance algorithms to support the core chemoinformatics requirements of Antidote. NB, GL and PW will contribute to and test new tutorials, use-cases and bespoke chemoinformatics software; furthermore, they will extensively test Antidote during the stages of development. Finally, NB, GL and PW will provide feedback and advice during the deployment of the system in different environments and settings. All contributors will be involved in outreach activities and publications outputs.

The estimated budget breakdown for Phase I is listed below:

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


