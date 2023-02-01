- #+BEGIN_QUERY
  		  {:title [:h2 "Currently Reading"]
  		   :query [:find (pull ?b [*])
  		           :where
  		           [?b :block/properties ?props]
  		           [(get ?props :type) ?type]
  		           [(get ?props :status) ?st]
  		           [(= *#{"reading"} ?st)]]}*
  		  #+END_QUERY
-