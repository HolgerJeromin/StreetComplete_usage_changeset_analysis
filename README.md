This script is processing changeset planet file.

Changeset file can be downloaded from [https://planet.osm.org/](https://planet.osm.org/)

In this case "Latest Weekly Changesets" file is needed. It is not huge and can be easily processed line by line.

It can be downloaded using `curl` from one of [mirrors](https://wiki.openstreetmap.org/wiki/Planet.osm#Downloading), for example
`curl -o changesets-latest.osm.bz2 https://ftp.nluug.nl/maps/planet.openstreetmap.org/planet/changesets-latest.osm.bz2`

The file should be unarchived to allow processing, with something like `bzip2 -dk changesets-latest.osm.bz2`.

Data in the file looks like this

```
 <changeset id="71993917" created_at="2019-07-08T00:10:48Z" closed_at="2019-07-08T00:32:20Z" open="false" user="Jofe Graham-Jenkins" uid="9581609" min_lat="-21.0791870" min_lon="149.2141598" max_lat="-21.0791870" max_lon="149.2141598" num_changes="1" comments_count="0">
  <tag k="source" v="survey"/>
  <tag k="comment" v="Add opening hours"/>
  <tag k="created_by" v="StreetComplete 12.2"/>
  <tag k="StreetComplete:quest_type" v="AddOpeningHours"/>
 </changeset>
```

or

```
<changeset id="35" created_at="2005-05-24T16:49:34Z" closed_at="2005-05-24T19:28:22Z" open="false" user="Magne" uid="204" min_lat="62.6301994" min_lon="6.1912751" max_lat="63.4497032" max_lon="11.1394958" num_changes="303" comments_count="0"/>
```

for early changesets without tags.
