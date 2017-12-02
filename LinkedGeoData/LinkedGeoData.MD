
### Query to get neighborhoods
```sql
  Prefix lgdr:<http://linkedgeodata.org/triplify/>
  Prefix lgdo:<http://linkedgeodata.org/ontology/>
  select ?s ?neigh ?street ?lat ?long
  {
    ?s <http://linkedgeodata.org/ontology/addr%3Acity> "Rio de Janeiro" .
    ?s <http://linkedgeodata.org/ontology/addr%3Astreet> ?street .
    optional {
      ?s <http://linkedgeodata.org/ontology/addr%3Asuburb> ?neigh .
      ?s <http://www.w3.org/2003/01/geo/wgs84_pos#lat> ?lat .
      ?s <http://www.w3.org/2003/01/geo/wgs84_pos#long> ?long
    }
  }
  limit 1000
```
