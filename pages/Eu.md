- #+BEGIN_QUERY
  {:title [:h2 "Eu"]
   :query [:find (pull ?b [*])
           :where
           [?p :block/name "project"]
           [?b :block/refs ?p]]}
  #+END_QUERY
-