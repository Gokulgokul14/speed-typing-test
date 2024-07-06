# speed-typing-test
import time

# Function to calculate typing speed
def calculate_wpm(time_taken, num_words):
    return (num_words / time_taken) * 60

# Function to run the typing test
def typing_test():
    test_sentence = "The quick brown fox jumps over the lazy dog."
    num_words = len(test_sentence.split())

    print("Type the following sentence as quickly and accurately as possible:")
    print(f"\n{test_sentence}\n")

    input("Press Enter when you are ready to start...")

    start_time = time.time()
    typed_sentence = input("\nStart typing now:\n")
    end_time = time.time()

    time_taken = end_time - start_time

    if typed_sentence.strip() == test_sentence:
        wpm = calculate_wpm(time_taken, num_words)
        print(f"\nGreat job! Your typing speed is {wpm:.2f} words per minute.")
    else:
        print("\nOops! The sentence you typed does not match the given sentence.")

# Run the typing test
typing_test()
