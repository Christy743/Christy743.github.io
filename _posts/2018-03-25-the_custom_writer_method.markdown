---
layout: post
title:      "The Custom Writer Method "
date:       2018-03-26 01:45:45 +0000
permalink:  the_custom_writer_method
---


I was a little confused. Well, maybe a lot confused on the requirement in the Rails Portfolio Project for the custom writer. I did have to reach out on one of the 1:1’s with a tech coach. After reading, researching and talking with the tech coach, I think I have a handle on this writer method. Remember in earlier lessons and labs of the reader method and writer method? 

In the code below, the first method is to return @dog and the second method is to set @dog to an argument:

```
		def dog 
		    @dog  	# return @dog
		end 

		def dog=(dog)
		    @dog = dog 	# set @dog
		end

```

Remember that the first method is a ‘reader’ or ‘getter’ and the second method is a ‘writer’ or ‘setter’.  The above code is explicitly written and there are the implicit methods of attr_accessor, attr_reader and attr_writer that is written in the model. 

In my Rails Portfolio Project of ["Knitting Patterns"](https://github.com/Christy743/knitting_patterns_rails),  I decided to make a custom writer method for my_favorite.  I nested the attribute of my_favorite into the pattern view form so that the user could type in their favorite yarn.  Below is my custom writer code:

```
	def  favorite_patterns_attributes=(favorite_pattern_attributes)
       	  favorite_pattern_attributes.values.each do |favorite_pattern_attribute|
     	     if favorite_pattern_attributes[:my_favorite].present?
                  favorite_pattern = FavoritePattern.find_or_create_by(my_favorite: favorite_pattern_attributes[:my_favorite])		 	  self.favorite_patterns.build(my_favorite: my_favorite)
             end
          end
        end
```

And my view form for making a new pattern:

```
<%= form_for @pattern do |f| %>
     <%= f.label :name, "Type in Your Pattern Name" %><br />
       <%= f.text_field :name, class: "form-control" %>
       <br />
       <%= f.label :needles, "Knitting Needles:" %><br />
       <%= f.text_field :needles, class: "form-control" %>
       <br />
       <%= f.label :yarn %><br />
       <%= f.text_field :yarn, class: "form-control" %>
       <br />
       <%= f.label :weight, "Yarn Weight; for example; sport, fingering, lace:" %><br />
       <%= f.text_field :weight, class: "form-control" %>
       <br />
       <%= f.label :quantity, "Yarn quantity:" %><br />
       <%= f.number_field :quantity, class: "form-control"%>
       <br />
       <%= f.label :materials, "Any other materials to complete the project:" %><br></br>
       <%= f.text_area :materials, class: "form-control" %><br />
       <br />
       <%= f.label :content, "Pattern Directions" %><br />
       <%= f.text_area :content, class: "form-control" %>
       <br />
       <%= hidden_field_tag :authenticity_token, form_authenticity_token %>

      <h4>What is your favorite yarn?</h4>
           <%= f.fields_for :favorite_patterns, @pattern.favorite_patterns.build do |ff| %>
           <%= ff.text_field :my_favorite %>
      <% end %><br />

    <%= f.submit class: "btn btn-primary" %>
<% end %>

```

So the very last part of my form is asking “What is your favorite yarn?”

This part is nested in my pattern form and has the attribute ‘my_favorite’ and will look at the custom writer method in my ‘Pattern’ model. This writer method has more going on in it than just setting ‘favorite_patterns_attributes’ to an argument, such as finding or creating the favorite_patterns[:my_favorite] attribute.

Hope this helps a bit with your project!
