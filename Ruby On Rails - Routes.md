Rountes are located in
<pre>
config/routes.rb
</pre>

Rails <b>resources</b> creates standard routes

$ <b>resources</b> <em>controller</em>  

<pre>
# config/routes.rb

<b>resources</b> :path
</pre>
creates the paths
<pre>
# $ rake routes

    Prefix Verb   URI Pattern                           Controller#Action
path_index GET    /path(.:format)                       path#index
           POST   /path(.:format)                       path#create
  new_path GET    /path/new(.:format)                   path#new
 edit_path GET    /path/:id/edit(.:format)              path#edit
      path GET    /path/:id(.:format)                   path#show
           PATCH  /path/:id(.:format)                   path#update
           PUT    /path/:id(.:format)                   path#update
           DELETE /path/:id(.:format)                   path#destroy
</pre>

adding
<pre>
resources :path
<b>get  'path/additional_path' => 'path#additional_path', as: 'another'</b>
</pre>

creates the paths
<pre>
    Prefix Verb   URI Pattern                           Controller#Action
path_index GET    /path(.:format)                       path#index
           POST   /path(.:format)                       path#create
  new_path GET    /path/new(.:format)                   path#new
 edit_path GET    /path/:id/edit(.:format)              path#edit
      path GET    /path/:id(.:format)                   path#show
           PATCH  /path/:id(.:format)                   path#update
           PUT    /path/:id(.:format)                   path#update
           DELETE /path/:id(.:format)                   path#destroy
   <b>another GET    /path/additional_path(.:format)       path#additional_path</b>
</pre>

the new path can be accessed using either
<pre>
<b>/path/additional_path  
another_path</b>
</pre>

and a method will need to be added to the controller
<pre>
# app/controllers/path_controller.rb

class PathController < ApplicationController
  <b>def additional_path
    ...
  end</b>
end
</pre>

###NOTE:paths are evaluated in the order the appear in routes.rb using the first occurance
