#Usa a imagem alpine com python 3.9
FROM python:3.9-alpine

#Muda o Diretorio padrão de uso
WORKDIR /myapp

#copia o arquivo com os requerimentos necessários para rodar a aplicação
COPY requirements.txt ./


#Instala compilador C, as dependencias, e remove o que não for mais necessário apos a instalação
RUN pip install --no-cache-dir -r requirements.txt


COPY . .

EXPOSE 8000

CMD [ "python3.9", "manage.py", "runserver", "0.0.0.0:8000"] 
