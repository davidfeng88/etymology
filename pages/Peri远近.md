public:: true

- query-table:: true
  query-properties:: [:word :notes :直译 :tags]
  #+BEGIN_QUERY
  {:title [:h2 "Peri"]
   :query [:find (pull ?b [*])
           :where
           [?p :block/name "peri远近"]
           [?b :block/refs ?p]]}
  #+END_QUERY