
## Poetry command

1) [Оф сайт с командами](https://python-poetry.org/)
2) [Документация подробная](https://python-poetry.org/docs/basic-usage/)


- `poetry new project` - инициализация проекта, если вы делаете не по текущему шаблону
- `poetry add fastapi` - добавить зависимость в toml
- `poetry install` - установить зависимость
- `poetry upgrade` - обновить все зависимости

###  Подключение в Pycharm интерпретатора poetry 
- Полная инструкция в jetbrains [Документации](https://www.jetbrains.com/help/pycharm/poetry.html#poetry-env)
- В случае неудачи писать за помощью к [@mob1ss](https://t.me/mob1ss)

### Для тех, кто работает в Других редакторах VisualSt и тд.
- install `python -m venv myenv`
- activate `source myenv/bin/activate` || `myenv\Scripts\activate`
- install `pip install poetry`
- Run `poetry install`

### Пример poetry DockerFile для API
```angular2html
FROM python:3.10-slim

WORKDIR /app

COPY . .

RUN pip install poetry && \
    poetry config virtualenvs.create false && \
    poetry install --no-interaction --no-ansi

COPY stargate /app/stargate

CMD ["uvicorn", "stargate.main:app", "--host", "0.0.0.0", "--port", "5002"]

```

## Ruff command
1) [Документация](https://docs.astral.sh/ruff)
- `ruff check --fix .` - проверить на ошибки и сразу пофиксить текущею директорию 
- Для перехода к определенной ошибки, `ctrl + лкм`

## Loguru tutorial
1) [Документация](https://pypi.org/project/loguru/)

`from loguru import logger`
- `logger.info("mess")` - вместо обычного print
- `logger.debug("mess")` - в случае дебагов
- `logger.success("mess")` - в успешного вывода или принта (транслируется зеленым)
- `logger.error("mess")` - в ошибок в except (транслируется красным)

## RabbitMQ
- [Репозиторий](https://github.com/Data-Acquisition/RabbitMq-Python) и UseCases для использования
- [Видео о том, что это такое](https://www.youtube.com/watch?v=WoPfMjy3UqA)

## Docker
- [Репозиторий](https://github.com/Data-Acquisition/Dokcer_Pattern) и примеры по сборкам проектам
- [Общий материал для ознакомления](https://sky.pro/media/chto-takoe-kontejnerizacziya-i-kak-ispolzovat-docker-s-python/)
- [Средне-углубленный материал](https://apipython.ru/rukovodstvo-po-ispolzovaniyu-modulya-python-dlya-raboty-s-docker-kontejnerami/)
- [Технически углубленный материал](https://tproger.ru/articles/dockerize-python-sozdajom-obraz-docker-iz-prilozhenija-na-python)
- [Видео-гайд по Docker c понятным объяснением](https://www.youtube.com/watch?v=eAXjeh5MRVU)

## Tests

### Видео уроки
1) Pytest
- [Pytest - первое знакомство](https://www.youtube.com/watch?v=rAKIK5_UMzw&list=PLeLN0qH0-mCVdHgdjlnKTl4jKuJgCK-4b)
- [Pytest - углубленные уровень 1](https://www.youtube.com/watch?v=1HtEPEn4-LY&list=PLlKID9PnOE5hCuNW8L-qxC12U7WPWG6YS)
- [Pytest - углубленные уровень 2](https://www.youtube.com/watch?v=s_aG4tBJoeI&list=PLB2iiSfKWtvykq9s0plSVI_Du60i0iphU)

2) Playwright
- [Playwright - первое знакомство](https://www.youtube.com/watch?v=sWaahzhbzLA)
- [Playwright - угулубленный уровень 1](https://www.youtube.com/watch?v=amcr5vZ_53s)
- [Playwright - угулубленный уровень 2](https://www.youtube.com/watch?v=f1AwiE_M3SE)

### Документации

1) [Pytest - оф. документация](https://docs.pytest.org/en/latest/contents.html)
2) [Playwright - оф. документация](https://playwright.dev/python/docs/intro)

### Статьи + доп материал по тестированию и тд
1) [Как написать свой первый автотест Pytest + Playwright](https://habr.com/ru/articles/714950/)
2) [Тестируем с Playwright](https://tproger.ru/articles/sovremennyj-podhod-k-avtomatizacii-testirovaniya-veb-prilozhenij-s-pomoshhyu-python-playwright-242777)
3) [Логирование Logging](https://habr.com/ru/companies/wunderfund/articles/683880/)
4) [Логирование Loguru](https://habr.com/ru/articles/454436/)
5) [Тестируем на Python: unittest и pytest. Инструкция для начинающих ](https://tproger.ru/articles/testiruem-na-python-unittest-i-pytest-instrukcija-dlja-nachinajushhih)
6) [Основы эффективного тестирования Python программ в Pytest](https://pylot.me/article/26-osnovi-effektivnogo-testirovaniya-python-programm-v-pytest/)
7) [Как правильно писать API авто тесты на Python](https://habr.com/ru/articles/709380/)
7) [Пишем АПИ автотесты на Python по шагам](https://habr.com/ru/articles/765512/)
8) [Git за полчаса](https://proglib.io/p/git-for-half-an-hour)


## Шпаргалка по Python
 - [«Python за час»](https://okpython.net/python/python_za_chas/python_za_chas.html)
 - [Энциклопедия Devman Python](https://dvmn.org/encyclopedia/)
 - [Видео Уроки по основам Python](https://www.youtube.com/watch?v=34Rp6KVGIEM&list=PLDyJYA6aTY1lPWXBPk0gw6gR8fEtPDGKa)
 - [Видео - Python за 15 минут](https://www.youtube.com/watch?v=U0lib5e_c-A)