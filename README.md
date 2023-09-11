# Create-a-simple-chatbot-that-can-respond-to-user-input-with-predefined-responses.
import nltk
from nltk.chat.util import Chat, reflections

pairs = [
    ["hi|hello|hey", ["Hello!", "Hi there!"]],
    ["how are you?", ["I'm a chatbot, so I don't have feelings, but thanks for asking!"]],
    ["what's your name?", ["I'm just a chatbot, so I don't have a name."]],
    ["bye|goodbye", ["Goodbye!", "See you later!"]],
]

chatbot = Chat(pairs, reflections)

def main():
    print("Hello! I'm a chatbot. Type 'bye' to exit.")
    while True:
        user_input = input("You: ")
        if user_input.lower() == 'bye':
            print("Chatbot: Goodbye!")
            break
        response = chatbot.respond(user_input)
        print(f"Chatbot: {response}")

if __name__ == "__main__":
    main()
