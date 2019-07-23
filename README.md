This script is processing changeset planet file.

Changeset file can be downloaded from [https://planet.osm.org/](https://planet.osm.org/)

In this case "Latest Weekly Changesets" file is needed. It is not huge and can be easily processed line by line.

It can be downloaded using `curl` from one of mirrors, for example
`curl -o changesets-190708.osm.bz2 https://ftp5.gwdg.de/pub/misc/openstreetmap/planet.openstreetmap.org/planet/2019/changesets-190708.osm.bz2`

The file should be unarchived.


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
