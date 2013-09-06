RDF for CLIPS parser/serializer
===============================

Own CLIPS-suitable format's parser and serializer for Sesame's Rio.

This format is based on NTriples.
Therefore, we used Aduna's NTriples serializer and parser as a baseline.
Most of the credit goes for them.

Regarding our format:
 
 * A RDF triple in our CLIPS format must have the following shape: (. subject predicate object )
  * The subject's, predicate's and object's serialization is the same as in NTriples.
  * The URIs can be shortened using prefixes which are hidden to CLIPS in the CLP serialization.
    * This means that we must retain this correspondences to extend the URIs after CLIPS reasoning.
    * In other words, in our format we hide the namespace's values, so CLIPS doesn't know them.
 * This format is used in conjuntion with some RDFS and OWL rules also provided in this project.
