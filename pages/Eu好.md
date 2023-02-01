public:: true

- query-table:: true
  query-properties:: [:word :notes :直译 :tags]
  #+BEGIN_QUERY
  {:title [:h2 "Eu好"]
   :query [:find (pull ?b [*])
           :where
           [?p :block/name "eu好"]
           [?b :block/refs ?p]]}
  #+END_QUERY