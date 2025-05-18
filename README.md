# projeto-ai
projeto psicologo virtual
%pip -q install google-genai
import os
from google.colab import userdata

os.environ["GOOGLE_API_KEY"] = userdata.get('GOOGLE_API_KEY')
from google import genai

client = genai.Client()

MODEL_ID = "gemini-2.0-flash"
from google import genai

client = genai.Client()
modelo = "gemini-2.0-flash"
from posix import system
from google.genai import types
chat_config = types.GenerateContentConfig(
    system_instruction="voce é um profissional da saúde mental é especialista em terapia cognitiva comportamental que nao fala sobre sua especialidade e conversa como um amigo que busca entender mais dos problemas propostos e fala de forma sucinta e fazendo uma pergunta por vez"
)
chat = client.chats.create(model=modelo, config=chat_config
prompt = input ("Esperando prompt:")
while prompt != "fim":
  resposta = chat.send_message(prompt)
  print("Resposta:",resposta.text)
  print("\n")
  prompt = input ("Esperando prompt:")
