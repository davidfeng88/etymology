public:: true

- {{query (page-property parts [])}}
  query-sort-by:: word
  query-table:: true
  query-sort-desc:: false
  query-properties:: [:parts :word :notes :直译 :tags]
- query-table:: true
  #+BEGIN_QUERY
  {:title [:h2 "Eu"]
   :query [:find (pull ?b [*])
           :where
           [?p :block/name "eu好"]
           [?b :block/refs ?p]]}
  #+END_QUERY