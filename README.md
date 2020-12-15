om chatterbot import ChatBot
from chatterbot.trainers import ListTrainer

bot = Chatbot("My Bot")

convo=[
    'Hello',
    'Hi there!',
    'How are you doing?',
    'I am doing great.',
    'That is good to hear',
    'Thank you.',
    'welcome.'
]





trainer = ListTrainer(bot)

# now training the bot with the help of trainer

trainer.train(convo)

#answer=bot.get_response("what is your name")
#print(answer)

print("Talk to bot")
while True:
    query=input()
    if query == 'exit' :
        break
    answer = bot.get_response(query)
    print("bot : ", answer)
    
