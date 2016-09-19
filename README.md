# Eventex

Sistema de Eventos encomendado pela Morena.

[![Build Status](https://travis-ci.org/iesodias/eventex-wttd.svg?branch=master)](https://travis-ci.org/iesodias/eventex-wttd)
[![Code Health](https://landscape.io/github/iesodias/eventex-wttd/master/landscape.svg?style=flat)](https://landscape.io/github/iesodias/eventex-wttd/master)

## Como desenvolver?

1. Clone o repósitorio.
2. Crie um virtualenv com Python 3.5
3. Ative seu virtualenv.
4. Instale as dependecias
5. Configure a instância com o .env
6. Execute os testes.

```
git clone git@github.com:iesodias/eventex.git wttd
cd wttd
python -m venv .wttd
source .wttd/bin/activate
pip install c-r requirements-dev.txt
cp contrib/env-sample .env
python manage.py test

```


## Como fazer o deploy?

1. Crie uma instancia no heroku
2. Envie as configuracoes para o heroku
3. Define uma SECRETE_KEY segura para a instancia
4. Defina DEBUG=False
5. Configure o serviço de email
6. Envie o código para o heroku

```Console
Heroku create minhainstancia
heroku configu:push
heroku config:set SECRET_KEY='python contrib/secret_gen.py'
heroku config:set DEBUG=False
#configura o email
git push heroku master --force
```