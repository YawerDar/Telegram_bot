# Telegram_bot


python
import openai

# Set up OpenAI API credentials
openai.api_key = '6015349358:AAGmckgnTc3JTz3EDcgKpuzSYfn-SKTcbLY'

# Define a function to prompt the chatbot and get its response
def chat(prompt):
    response = openai.Completion.create(
        engine='text-davinci-003',
        prompt=prompt,
        max_tokens=100,
        temperature=0.6,
        n=1,
        stop=None,
        temperature=0.6,
        top_p=1,
        frequency_penalty=0,
        presence_penalty=0
    )
    return response.choices[0].text.strip()

# Start the chatbot conversation
print("Chatbot: Hello! How can I assist you today?")
while True:
    user_input = input("Globalvpn788_bot: ")
    if user_input.lower() == 'bye':
        print("Chatbot: Goodbye! Have a great day!")
        break
    prompt = f"User: {user_input}\nChatbot:"
    bot_response = chat(prompt)
    print(f"Chatbot: {bot_response}")

