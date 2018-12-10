# Data Description

This directory contains data which record ILI activity levels in Italy, starting from the 2006-2007 season to the 2015-2016 one.  
The data are taken from two different sources, Influnet and Influweb. All these information are available
online as convenient PDF files that can be freely downloaded.
[Tabula](http://tabula.technology) software was used to extract data tables from the aforementioned PDF files.

There are also the Wikipedia data used to train and validate the model. The `wikipedia` directory contains the page views
of the 470 feature (Wikipedia's pages) used and the `wikipedia_random` directory contains the data of the random
Wikipedia's pages used to validate our model and confirm our hypothesis.

The `keywords` directory contains the lists of Wikipedia's pages selected.

## Influnet
Influnet (http://www.iss.it/iflu/) is an Italian epidemiological surveillance program which monitors ILI activity on a nation-wide
basis by using data provided by sentinel physicians. The data are published weekly, in the form of bulletins, that
can be viewed by visiting the Italian Department of Health website (http://www.salute.gov.it/portale/influenza/homeInfluenza.jsp).

## Influweb
Influweb (https://www.influweb.it/) is an epidemiological surveillance program, which is part of a larger European organization
called InfluenzaNet (http://www.influenzanet.eu/). In contrast with the traditional system of sentinel networks of mainly primary
care physicians, Influeweb obtains its data directly from the population. Any resident of a country in which InfluenzaNet is
implemented can register to the program. The participants are asked to monitor their health and report any symptoms they have
experienced since their last visit.

The data provided here were taken from the official Italian Influweb website (https://www.influweb.it/it/dati/)
and from the Influnet archives (http://www.iss.it/flue/index.php?id=138&tipo=13&lang=1).

## Data format

#### Influnet
Each row gives these information:
* **Settimana**: year and week in which the data were recorded;
* **Totale Medici**: total number of sentinel physicians who reported patients with ILI symptoms;
* **Totale Casi**: total number of ILI cases on that week;
* **Totale Assistiti**: total number of patients who were monitored by the sentinel physicians on that week;
* **Incidenza Totale**: total incidence of ILI cases on that week;

#### Influweb
Each row gives these information:
* **yearweek**: year and week in which the data were recorded;
* **incidence**: total incidence of ILI cases on that week;

### Wikipedia
Each row consists of data regarding all the feauture for a specific week. cd