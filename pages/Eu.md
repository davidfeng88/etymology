- #+BEGIN_QUERY
  		  {:title [:h2 "Currently Reading"]
  		   :query [:find (pull ?b [*])
  		           :where
  		           [?b :block/properties ?props]
  		           [(get ?props :type) ?type]
  		           [(get ?props :status) ?st]
  		           [(= *#{"reading"} ?st)]]}
  		  #+END_QUERY
- #+BEGIN_QUERY
  {:query [:find (pull ?b [*])
           :in $ ?s
           :where
           [?b :block/original-name ?n]
           [(clojure.string/starts-with? ?n ?s)]]
   :inputs [ "task.myName." ]
   }
  *#+END_QUERY*
-