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
- #+BEGIN_QUERY
  {:title "All pages have a *programming* tag"
   :query [:find ?name
         :in $ ?tag
         :where
         [?t :block/name ?tag]
         [?p :block/tags ?t]
         [?p :block/name ?name]]
   :inputs ["eu好"]}
  #+END_QUERY