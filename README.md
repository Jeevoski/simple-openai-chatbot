# simple-openai-chatbot
A simple AI chatbot built with Python using the OpenAI API. It takes user input and generates smart, human-like responses. Ideal for beginners exploring AI integration. Just plug in your API key and start chatting! Clean, minimal codebase that’s easy to extend and customize.
import openai
openai.api_key=""
def chat_with_gpt(prompt):
    response = openai.ChatCompletion.create(
        model="gpt-3.5-turbo",
        messages=[{"role": "user", "content": prompt}]
    )
    return response.choices[0].message.content.strip()

if __name__ == "__main__":
    while True:
        user_input = input("You: ")
        if user_input.lower() in ["quit", "exit", "bye"]:
            break

        response = chat_with_gpt(user_input)
        print("Chatbot: ", response)
 
