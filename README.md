# Roll call results of vote events during plenary sessions of municipal assemblies in Czech Republic

## How to cite

GREGOR, Kamil (2015). "Roll call results of vote events during plenary sessions of municipal assemblies in Czech Republic" [https://github.com/kamilgregor1/czech_municipal_assemblies_roll_call_votes].

## Data availability

Municipalities are included depending on <a href = "http://blog.openingparliament.org/post/108553329888/surveying-parliamentary-data-openness-in-6300"><strong>data availability</strong></a>. Data from the Municipal Assembly of Prague (<em>Zastupitelstvo hlavního města Prahy</em>) were scraped by <a href = "https://github.com/michalskop/datapackages"><strong>Michal Škop</strong></a> and are updated irregularly.

Most municipalities included here have started to record and/or publish roll call results of plenary vote events only recently. If roll call results are available, it usually means that results of all or almost all vote events are recorded by names of individual voters. In almost all municipalities, votes of all voters are recorded (not just those that were present during voting).

## Data specification

The <a href = "http://popoloproject.com/"><strong>Popolo</strong></a> data standard is used. Data on each municipality is split into subdirectories by electoral terms. Each term contains CSV files on party groups, vote events and votes in a given term. If more information than just voters' names is available, it also contains a CSV file on voters. Types of information available in each municipality vary. See an <a href = "https://github.com/kamilgregor1/czech_municipal_assemblies_roll_call_votes/blob/master/data_specification.csv"><strong>overview</strong></a> of variables in the CSV files and examples of their values.

In most municipalities, there are some vote events that are included in the <code>vote_events</code> dataset but not in the <code>votes</code> dataset or vice versa due to errors, missing data or changes in HTML structure on the official websites of the municipalities. This usually does not amount to more than 5 % of all vote events.

## Data updates

In case of several larger municipalities that publish roll call results in the HTML format, there are live scrapers of the official municipal websites that run every Monday. In other cases, the data is manually copied from minutes from the plenary sessions. This data is updated irregularly.

## Miscellaneous information

In almost all municipalities, there are the following voting options:

<ul>
<li><em>Pro / Ano</em> - In favour / Yea
<li><em>Proti / Ne</em> - Against / Nay
<li><em>Zdržel se</em> - Abstained
<li><em>Nehlasoval</em> - Not voted (e.i. was present but did not indicate any of the options above)
<li><em>Nepřítomen</em> - Absent
</ul>

The quorum is almost always calculated out of all voters in the assembly (not just those present). This means that abstention, not voting and even absenting is <em>de facto</em> identical to voting against.

In some municipalities, voters are organized in formal party groups (<em>zastupitelský klub</em>). In most cases, however, voters' affiliations to political parties are not formally reflected in the assembly. A variable <code>group:id</code> usually indicates a political party that proposed a given voter as a candidate in municipal elections (<em>navrhující strana</em>) or a political party that the voter is a member of (<em>stranická příslušnost</em>). This is not identical to a name of a candidate list.

Substantive meaning of variables <code>vote_events:motion:title</code>, <code>vote_events:motion:number</code> and <code>vote_events:title</code> varies among municipalities depending on how information on voting is published. One motion can for example correspond to a single item of the agenda of a plenary session or to one proposal (project / dossier). In both situations, there could be multiple vote events related to the same motion. In all municipalities, the variable <code>vote_events:title</code> is only used if it always refers to information that is unique to individual vote events.

## Author

Created by <a href = "https://twitter.com/kamilgregor"><strong>Kamil Gregor</strong></a> (with <a href = "http://kohovolit.eu/en/"><strong>KohoVolit.eu</strong></a> and <a href = "http://www.muni.cz/"><strong>Masaryk University</strong></a>) in the <em>Otevírání výsledků hlasování na obecních zastupitelstvech</em> (Opening up voting results in municipal assemblies) project supported by the <a href = "http://www.osf.cz"><strong>Open Society Fund Prague</strong></a>. 

## License

<a href = "http://creativecommons.org/licenses/by/4.0"><strong>Creative Commons BY 4.0</strong></a>.
