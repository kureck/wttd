# Eventex

Sistemas de eventos

## Como desenvolver?

1. Clone
2. virtualenv python3.5
3. ative virtualenv
4. instale dependências
5. configure instância com .env
6. execute testes

```console
git clone git@github.com:kureck/wttd.git wttd
cd wttd
python -m venv .wttd
source .wttd/bin/activate
pip install -r requirements.txt
cp contrib/env-sample .env
python manage.py test
```

## How to deploy

1. crie uma instância no heroku
2. envie config para heroku
3. defina uma SECRET_KEY segura para a instância
4. defina DEBUG=False
5. configure servico de email
6. envie código para heroku

```console
heroku create <minha instancia>
heroku config:push
heroku config:set SECRET_KEY=`python contrib/secret_gen.py`
heroku config:set DEBUG=False
# config email
git push heroku master --force
```