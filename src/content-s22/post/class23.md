+++
date = "13 Apr 2022"
draft = false
title = "Class 23: Programmable Pharmacueticals"
slug = "class23"
+++

## Schedule

**Project Update: due Tuesday, 19 April, 4:59pm.** An update on how your project is going, any changes from your original plans, and summary of what progress you have been able to make. (A link to a form for submitting this will be posted on April 18.)

## Slides

Slides: [class23.pdf](https://www.dropbox.com/s/kgxqy4auzj92h7q/csbio-class23.pdf?dl=0)

## Causes of Death

There was a great question about what fraction of all deaths are
accounted for in the statistics I showed from [Our World In
Data](https://ourworldindata.org/causes-of-death). The source of most
of the data is the [Global Burden of Disease
Study](https://www.healthdata.org/gbd/2019) (mostly funded by the
Gates Foundation). My understanding is that the statistics do attempt
to assign a cause of death to every death, but are using a lot of
imputation to do it. According to [_Global burden of 369 diseases and
injuries in 204 countries and territories, 1990–2019: a systematic
analysis for the Global Burden of Disease Study
2019_](https://www.thelancet.com/journals/lancet/article/PIIS0140-6736(20)30925-9/fulltext),

> _Input data were extracted from censuses, household surveys, civil
registration and vital statistics, disease registries, health service
use, air pollution monitors, satellite imaging, disease notifications,
and other sources. Cause-specific death rates and cause fractions were
calculated using the Cause of Death Ensemble model and spatiotemporal
Gaussian process regression. Cause-specific deaths were adjusted to
match the total all-cause deaths calculated as part of the GBD
population, fertility, and mortality estimates._

They make many adjustments and corrections to the reported data to account for all sorts of biases in it (full details in this 1813 page [Appendix 1](https://www.thelancet.com/cms/10.1016/S0140-6736(20)30925-9/attachment/deb36c39-0e91-4057-9594-cc60654cf57f/mmc1.pdf), and [available source code](https://ghdx.healthdata.org/gbd-2019/code).
This should, of course, raise concerns about how closely the statistics used match the reality, but it is the best data we have.

For specific countries such as the US, there is more standard and
perhaps more carefully collected data. You can see the CDC form
doctors in the US fill our for cause of death: [_Instructions for
Completing the Cause-of-Death Section of the Death Certificate_](https://www.cdc.gov/nchs/data/dvs/blue_form.pdf). It does require
at least one cause of death to be filled in, and discourages use of
anything like "natural causes" as the cause of death:

> _The elderly decedent should have a clear and distinct etiological sequence for
cause of death, if possible. Terms such as senescence, infirmity, old
age, and advanced age have little value for public health or medical
research._

The "manner of death" includes Natural as an option (with the others
being Accident, Suicide, Homicide, Pending investigation, and "Could
not be determined".

If you're interested in exploring causes of death more, this is a
(morbidly) great site (based on the CDC data): [_How Will I
Die?_](https://www.lifecontingencies.com/question/3).

## Links

- Zhen Xie, Liliana Wroblewska, Laura Prochazka, Ron Weiss, Yaakov Benenson. [_Multi-Input RNAi-Based Logic Circuit for Identification of Specific Cancer Cells_](docs/xie-rna-logic-2011.pdf). Science, 2 September 2011.

Logic goes in vitro: https://www.nature.com/articles/nnano.2007.23.pdf

Advances in Applications of Molecular Logic Gates:
https://pubs.acs.org/doi/10.1021/acsomega.1c02912

- Dual MicroRNA-Triggered Drug Release System for Combined Chemotherapy and Gene Therapy with Logic Operation
https://pubs.acs.org/doi/10.1021/acsami.0c09494?ref=PDF


- Ana E. Jenike and Marc K. Halushka. [_miR-21: a non‐specific biomarker of all maladies_](https://biomarkerres.biomedcentral.com/track/pdf/10.1186/s40364-021-00272-1.pdf). Biomarker Research, 2021.