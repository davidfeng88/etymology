-
- query-sort-by:: word
  query-table:: true
  query-sort-desc:: false
  query-properties:: [:word :直译 :tags :page]
  #+BEGIN_QUERY
  {:title [:h2 "Cleos"]
   :query [:find (pull ?b [*])
           :where
           [?p :block/name "cleos 名声、荣耀"]
           [?b :block/refs ?p]]}
  #+END_QUERY
- {{query [[Cleos 名声、荣耀]]}}
  query-table:: true
  query-properties:: [:word :notes :直译 :tags :block]