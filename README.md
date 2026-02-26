# 🧬🇩🇰 MicrobeSeq Denmark (also known as SSI-Seq)

![MicrobeSeq Logo](./assets/images/MicrobeSeq_logo_dk.png)

Welcome to the official landing page for the MicrobeSeq Denmark project. This is the central hub for all repositories related to our research and development.

Apologies but this page is still in the works so details aren't available yet but will be made aviable here in the future!

SSI-Seq is supported by co-funding from the European Union’s EU4Health programme under Grant Agreement Nr 101111879. Views and opinions expressed do not necessarily reflect those of the European Union or HaDEA. Neither the European Union nor the granting authority can be held responsible for them.

## [Lab protocols](https://www.protocols.io/researchers/sekventeringsenheden-sb/publications)


>[Fast Track - Nanopore - SSI](dx.doi.org/10.17504/protocols.io.e6nvwd3n2lmk/v1) 
> 
> Protocol for the 'fast track' sequencing flow at the Sequencing Core Facility at Statens Serum Institut (SSI). This method utilises the MagLEAD system for DNA extraction and cleaning followed by the Nanopore sequencing platform for library prep. (Kit: SQK-RBK114-96) and sequencing (GridION w. flow cell type: FLO-MIN114). Both isolates and cleaned up DNA can be used as input material. 
Note, this protocol is in Danish. (🇩🇰) 

> [Bakterial WGS - SSI](dx.doi.org/10.17504/protocols.io.5qpvo3r7bv4o/v1) 
> 
> Method used at Sequencing Core Facility - Statens Serum Institut for sequencing of bacterial isolates. 
This protocol is specified for high-throughput sequencing of 96 isolates (sometimes less depending on the number of  isolates with large genomes). Furthermore, the genomes are sequenced on the Illumina sequencing platform using a MiSeq and the MiSeq 500-cycle v2 kit. Note, this protocol is in Danish. (🇩🇰) 

> [Covid sekventering - SSI](dx.doi.org/10.17504/protocols.io.j8nlkwqw6l5r/v1)
> 
> Method used at Statens Serum Institut for detection and sequencing of SARS-CoV-2 from saliva tests. 
This protocol is specified for high-throughput sequencing of 384 samples - 376 positive SARS-CoV-2 samples + 8 control samples divided into four 96-well PCR plates. Furthermore, the samples are sequenced on the Illumina sequencing platform using a NextSeq 550. Note, this protocol is in Danish. (🇩🇰) 

This list is not exhaustive.

## Software

### Sample processing

> uSymph
> 
> A custom database, API end points, job runners, and a web interface for chaining automation workflows to process tasks related to WGS surveillance.

> [Landing Zones](https://github.com/ssi-dk/landingzones)
>
> Our lab machines are on a different network from our data hub, and our analysis system. We user this to enable data transfers between our multiple servers while ensuring that all connections are tracked through a central file.

### Notification system

> [ssi_pingme](https://github.com/ssi-dk/ssi_pingme)
>
> A simple library intended for use with an API, to provide a common interface for sending notifications to users. The library supports multiple notification channels (e.g. email, webhook (slack/teams)) utilizing adaptive cards for messages.

### QC pipeline

![alt text](image.png)

The Bifrost QC pipeline is our standardized “front-door” workflow for bacterial whole‑genome sequencing data: it takes raw paired‑end reads and produces a clear, comparable quality summary that helps confirm a sample is usable before deeper, species‑specific analyses. In one run it performs core checks that matter for surveillance and routine genomics—cleaning and summarizing read quality, verifying that the data matches the expected organism (and flagging likely contamination or mix‑ups), generating a draft assembly, and then assessing assembly completeness and consistency. It also adds lightweight “sanity checks” that are informative across organisms, such as counting ambiguous sites and producing basic typing signals that support downstream interpretation.

Just as importantly, the pipeline collects all outputs into a single, structured report (along with the underlying per‑step reports), so results are easy to review, share, and compare across projects and time. Because it relies on widely used, well‑established analysis components (e.g., read QC, taxonomic classification, assembly and assembly metrics, MLST/rMLST typing, AMR marker screening, and plasmid marker screening) and produces consistent tabular outputs, other groups can run the same workflow to generate QC and characterization results that are directly comparable to SSI/Bifrost datasets—supporting harmonized analyses, benchmarking, and collaborative surveillance.

### QC analysis/report
> [uQCme](https://github.com/ssi-dk/uqcme)
>
> This program is 2 parts, 1 calculates QC metrics given input files and configuration files. From that it determines if the sample passes or fails QC (other outcomes possible as well) and generates a new file with these additional columns. The new file can then be fed into a web interface to filter and visualize the QC results and do API driven actions against them.

© 2023 MicrobeSeq Denmark. All rights reserved.

### Species specific pipelines
> [SSI Analysis utility](https://github.com/ssi-dk/ssi_analysis_utility)
>
> SSI Analysis Utility is Statens Serum Institute’s modular, reproducible pipeline for bacterial isolate characterization, developed as part of the MicrobeSeq Denmark project to support standardized genome-sequencing analysis in national surveillance. In practice, it provides a consistent way to convert sequencing data into comparable characterization outputs—such as antimicrobial resistance profiling, strain/sequence typing, and detection of virulence-associated markers—using a transparent, scalable workflow that can be applied across many samples.  ￼
>
> A key feature is that the pipeline is species-specific: the same framework runs tailored analysis “recipes” for priority pathogens including C. difficile, E. faecalis, E. faecium, E. coli, K. pneumoniae, N. meningitidis, S. aureus and S. enterica. Each organism is analysed with the most appropriate modules (for example, dedicated support for C. difficile toxin/repeat-focused characterization, meningococcal fine typing, S. aureus spa typing, and Salmonella serotyping). At the same time, SSI Analysis Utility is designed so results remain consistent and reproducible because the underlying tools and curated reference databases are managed in controlled, versioned setups—making it straightforward for other laboratories to adopt the same software and generate outputs that are directly comparable to SSI/MicrobeSeq Denmark datasets for downstream analysis and surveillance.