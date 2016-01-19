# DBpedia Utils

This small Python module contains a set of utility functions to work with DBpedia data. It works with Python 2.7 and 3.4.

You require the following modules: `regex`, `bz2file`.

Basically, the important function is `iter_entities_from`. It works like this:

```
for entity in iter_entities_from('instance_types_en.nt.bz2'):
    if 'http://dbpedia.org/ontology/Person' in entity['22-rdf-syntax-ns#type']:
        print(entity['resource'])
```

This snippet would print the DBpedia URI of all entities that are of class __Person__ in the file
`instance_types_en.nt.bz2`. Each entity is a dictionary where the resource key is the DBpedia URI
and the other keys correspond to the attributes present in the file being read.

That's all folks! :)

