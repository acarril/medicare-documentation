title: Overview

# Overview

!!! note
    This documentation is ported from https://www.nber.org/medicare/public/Public.html

NBER researchers have a long history of working with Medicare claims and as a result the NBER has worked closely with CMS over the past 15 years to ensure the integrity, security, and confidentiality of the data.

It is important to note that a researcher is required to enter into a data use agreement (DUA) with CMS for each project and follow proper protocol for approval, use and destruction of the data after completion of a project. Data acquired for one project cannot be used for a different project unless a new DUA approval has been obtained. CMS is the sole authority for decisions on any DUA. Obtaining a DUA is an involved and time consuming process.

ResDAC is an excellent resource which CMS contracts to provide guidance to Medicare data users. They provide assistance ranging from answering specific questions, to giving Medicare seminars at no direct cost to the attendee. In addition the ResDAC website (http://www.resdac.umn.edu/) contains information regarding FAQ, Medicare data dictionaries and information on the DUA application process.

Completing a CMS application is often a time consuming process which may take several months. ResDAC reviews DUAs to ensure that they are complete before sending them to CMS. The ResDAC website has more information on the steps and materials needed to complete a DUA application [here](https://www.resdac.org/cms-data/request/research-identifiable-files).

It is important to note that this document was created specifically with the NBER collection in mind and is therefore extremely relevant to NBER researchers interested in understanding the NBER holdings. While this document provides information specific to the NBER's collection, the code and many parts of this document are still useful to a non-NBER researcher interested in understanding Medicare data extracts.

## Medicare code and documentation project

The remainder of this document deals with documenting idiosyncrasies of the Medicare claims data and walks through the extraction of a cohort using the associated code. From a programming perspective, the associated code begins by extracting harmonized Medicare claims data for a narrowly defined sample of Medicare-enrolled individuals who experienced the onset of a diagnosis (defined by one or more diagnosis/procedure codes). This documentation focuses on individuals diagnosed with an acute myocardial infarction (AMI), although users can create their own cohorts.

The extraction of claims must first harmonize inter-year differences in the files, while also (1) identifying the claims representing the start of an episode, commonly referred to as an index event (e.g. the hospital claim showing the individual was diagnosed with an AMI (2) having identified the index event, a window of all claims occurring `X` years before and after the index event are generated. As the code has evolved, the harmonization of the raw files has been separated from the extraction of the cohorts because it overly complicated the code. Currently the harmonization is done by generating a series of views.

The documentation is organized into 3 parts, where part I↓provides background on the Medicare program and highlights some of the characteristics of the data in Section 2↓. This section is a good reference, to be used as questions arise while working with the data. The following Part 3↓ is a good starting point for new users looking to start using the Medicare data and code. Section 4↓ provides help to users running and setting up the code. Section 5↓ walks through the creation of the AMI extract. The final Part III↓ describes the programs (Stata and SAS) which take the harmonized extracted claims files, and aggregate them to create cost, procedure and comorbidity information at the episode/index event level. The programs are included in the [attached zip file](https://www.nber.org/medicare/public/MedicareNBER.zip).

Before proceeding to the main text, a few caveats are in order. In general, users should be aware that while the goal of this project has been to create extracts in which variables are comparable across all years, there are likely cases where the same variable is coded differently in different years or where a variable's meaning or interpretation changes in subtle ways from one year to the next. It is advisable to develop some familiarity with the underlying fields in each year's data file before working with the extracts generated by these scripts.

## Version Updates

See [https://www.nber.org/medicare/public/Public-1.html#toc-Section-1.2](https://www.nber.org/medicare/public/Public-1.html#toc-Section-1.2)