# Define a function called 'count_words' that takes one argument 'text'
def count_words(text):
    
# Initialize a variable 'word_count' to keep track of the number of words
   word_count = 0
    
 # Initialize a flag variable 'in_word' to track whether we're currently inside a word
   in_word = False

 # Iterate through each character 'char' in the input 'text'
  for char in text:
        
 # Check if the current character is a whitespace character (space, tab, newline, etc.)
   if char.isspace():
            
 # If it's a whitespace character, set 'in_word' to False to indicate we're no longer inside a word
   in_word = False
        
 # Check if we're not currently inside a word and the current character is not whitespace
   elif not in_word:
            
 # If we're not inside a word and the current character is not whitespace, increment 'word_count' by 1
  word_count += 1
            
 # Set 'in_word' to True to indicate we're now inside a word
  in_word = True

 # Return the total word count
 return word_count

# Prompt the user to enter a sentence or paragraph
text = input("Enter a sentence or paragraph: ")

# Call the 'count_words' function with the user's input and print the result
print("Word count:", count_words(text))
