#Hashes, Symbols

As we have seen, arrays can be defined to contain
	many items of the same type

```ruby 
my_array = ['zero','one','two','three','four']
```


we can access one of these items by its index in the arrays

```ruby 
puts my_array[2] #outpus 'two' 
```


we can also use the index to SET a value in the arrays

```ruby 
my_array[2] = 'TWO'
puts my_array[2] #outpus 2
```


We can even have arrays containing many different
  data types. Here well create a 'wizard' object

```ruby
my_wizard = ['Gandalf the Grey', 10000, 'Middle Earth', 'You Shall Not Pass', true, 'Balrogs']
```


Now this is all ok, if you remembered or noted somewhere that:
```ruby
my_wizard[0] #is name,
my_wizard[1] #is age,
my_wizard[2] #is location,
my_wizard[3] #is famous quote,
my_wizard[4] #is whether or not our wizard is epic, and
my_wizard[5] #is weaknesses
```

##But...
### we begin to see some shortcomings (at least with our wizard example). 

1. There is no evident association between the index of the array and the information it contains.
2. If we are storing diverse information, there is no key that identifies what each piece of information represents.
3. As a product of the first shortcoming, it is very difficult and time-inneficient to fetch or update information if we don't already know where it is. For example, looking up "Gandalf the Grey" by famous quotes might consist of something like:

```ruby
# assume all_wizards is a collection of wizards like the one we defined above
all_wizards.each do |wizard|	#iterates over each of our wizards
	wizard.each do |information| #iterates over single wizard info
		if information == 'You Shall Not Pass'
			return wizard
		end
	end
end
```

##What ever could we use?

#Hashes

A hash is a ruby data structure that allows us to pair keys with values. Before any further explaination, take a look at how it's done:

```ruby
my_wizard = {
    name: 'Gandalf the Grey',
    age: 10000,
    location: 'Middle Earth',
    famous_quote: 'You Shal Not Pass',
    epic: true,
    weaknesses: 'Balrogs',
}
```
