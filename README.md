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

### QC pipeline

![alt text](image.png)

The pipeline describes the steps taken for aquiring the output needed to run our QC metrics and a bunch of extras for the purpose of downstream surveillance.

### QC analysis/report
> [uQCme](https://github.com/ssi-dk/uqcme)
>
> This program is 2 parts, 1 calculates QC metrics given input files and configuration files. From that it determines if the sample passes or fails QC (other outcomes possible as well) and generates a new file with these additional columns. The new file can then be fed into a web interface to filter and visualize the QC results and do API driven actions against them.

© 2023 MicrobeSeq Denmark. All rights reserved.
