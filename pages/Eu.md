- #+BEGIN_QUERY
  {:title [:h2 "My books"]
   :query [:find (pull ?b [*])
  :where
  [?b :block/properties ?p]
  [(get ?p :tags) ?t]
  [(= "[[eu]]" ?t)]]}
  #+END_QUERY
-