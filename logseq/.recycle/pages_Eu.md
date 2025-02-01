query-table:: true
#+BEGIN_QUERY
{:title [:h2 "Eu"]
 :query [:find (pull ?b [*])
         :where
         [?p :block/name "eu"]
         [?b :block/refs ?p]]}
#+END_QUERY

-