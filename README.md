# Influenza and Wikipedia Dataset

## Data Description

This dataset contains data which record ILI activity levels in several european conutries, starting from the 2006-2007 influenza season to the 2017-2018 one. It comprises also Wikipedia's pageviews and pagecounts data extracted for several
specific pages.

The directories are named in such way:
   * `wikipedia_{country}`: they contain the pageviews/pagecounts data for the selected Wikipedia's pages. The pageviews are divided by year and the pageviews/pagecounts are aggregated for each week. Each file contains the following columns:
      * `week`: a string composed by `year`-`week_number`;
      * Several other columns which are named as the Wikipedia's page monitored;
   * `{country}`: they contains the influenza incidence data for the specified country. The incidence information is divided for each influenza seasons (which spans over two years). The file are thus named `{year}_{year+1}.csv`.
   Each file contains the following columns:
      * `week`: a string composed by `year`-`week_number`;
      * `incidence`: the incidence of influenza cases over 100000 people in that speficic week;

Moreover, inside each `wikipedia_{country}` directory there is another layer of division (this division is present also inside the `{country}` directories, but it matters only for the Wikipedia's pageviews since for the incidence data the division was done only for improve the usability):
   * `complete`: contains the entire dataset, done by merging the pageviews and pagecounts data;
   * `pageviews`: contains only the data from the pageviews (they are available only from May 2015);
   * `pagecounts`: contains only the data from the pagecounts (it was the first method used to analyze traffic on
        Wikipedia's pages). The data here ranges from the 2007 to the 2016.

The only difference is the `USA` directory in which the incidence data are provided in one unique
file called `2007_2013.csv`. Moreover, for the USA, only the pagecounts data were extracted.

### Other Directories

The `keywords` directory contains the lists of Wikipedia's pages selected. Each file is named `keywords_{country}.csv`
and it contains a simple list of all pages monitored.

## License

The influenza incidence values where extracted from several sources. Italy's data comes
from the [InfluNet service](https://old.iss.it/site/RMI/influnet/Default.aspx). Influenza seasons of Belgium,
Austria and Netherlands were extracted from the [FluNet surveillance tool](https://extranet.who.int/sree/Reports?op=vs&path=/WHO_HQ_Reports/G5/PROD/EXT/Influenza%20Surveillance+Report+by+Country). Gemany's influenza seasons were extracted from the [Survstat](https://survstat.rki.de/Content/Query/Create.aspx) application of the Robert Koch Institute.
The pageviews dataset have been extracted from Wikipedia's dumps and they have the same
license (Creative Commons Attribution-Share-Alike 3.0).

## How to cite

## Questions?

For further infos [send us an email](mailto:giovanni.det@gmail.com,cristian.consonni@unitn.it).
