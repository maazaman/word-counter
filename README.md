# word-counter
ef count_words(text):
    """Function to count the number of words in a given text."""
    # Split the text into words using whitespace as a delimiter
    words = text.split()
    return len(words)

def main():
    """Main function to handle user input and display the word count."""
    print("Welcome to the Word Counter Program!")
    
    while True:
        # Prompt user for input
        user_input = input("Enter a sentence or paragraph (or type 'exit' to quit): ")
        
        # Check if the user wants to exit
        if user_input.lower() == 'exit':
            print("Thank you for using the Word Counter. Goodbye!")
            break
        
        # Handle empty input
        if not user_input.strip():
            print("Error: Input cannot be empty. Please enter some text.")
            continue
        
        # Count words and display result
        word_count = count_words(user_input)
        print(f"Word Count: {word_count}\n")

if __name__ == "__main__":
    main()
