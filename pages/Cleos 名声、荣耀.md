public:: true

- query-sort-by:: word
  query-table:: false
  query-sort-desc:: false
  query-properties:: [:word :直译 :tags :page :block]
  #+BEGIN_QUERY
  {:title [:h2 "Cleos"]
   :query [:find (pull ?b [*])
           :where
           [?p :block/name "cleos 名声、荣誉"]
           [?b :block/refs ?p]]}
  #+END_QUERY