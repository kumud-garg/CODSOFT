import re
from datetime import datetime

def chatbot_response(user_input):
    user_input = user_input.lower()

    if user_input in ["hi", "hello", "hey"]:
        return "Hello! How can I help you?"

    elif re.search(r"\bhow are you\b", user_input):
        return "I'm doing well. How can I assist you?"

    elif "your name" in user_input:
        return "I am a simple rule-based chatbot."

    elif "time" in user_input:
        return "Current time is " + datetime.now().strftime("%H:%M:%S")

    elif "date" in user_input:
        return "Today's date is " + datetime.now().strftime("%Y-%m-%d")

    elif re.search(r"\b(help|what can you do)\b", user_input):
        return "I can respond to greetings, time, date, and simple questions."

    elif re.search(r"\b(bye|exit|quit)\b", user_input):
        return "Goodbye! Have a nice day."

    else:
        return "Sorry, I don't understand that."

print("Chatbot: Hello! Type 'bye' to exit.")

while True:
    user_input = input("You: ")
    response = chatbot_response(user_input)
    print("Chatbot:", response)

    if re.search(r"\b(bye|exit|quit)\b", user_input.lower()):
        break
