
## Poetry command

1) [Оф сайт с командами](https://python-poetry.org/)
2) [Документация подробная](https://python-poetry.org/docs/basic-usage/)


- `poetry new project` - инициализация проекта, если вы делаете не по текущему шаблону
- `poetry add fastapi` - добавить зависимость в toml
- `poetry install` - установить зависимость
- `poetry upgrade` - обновить все зависимости

###  Подключение в Pycharm интерпретатора poetry 
- Полная инструкция в jetbrains [Документации](https://www.jetbrains.com/help/pycharm/poetry.html#poetry-env)
- В случае неудачи писать за помощью к `https://t.me/mob1ss`
- install `pip install poetry`
- Run `poetry install`

### Для тех, кто работает в Других редакторах VisualSt и тд.
- install `python -m venv myenv`
- activate `source myenv/bin/activate` || `myenv\Scripts\activate`

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
- `logger.success("mess")` - в успешного вывода или принта (транслируется зеленным)
- `logger.error("mess")` - в ошибок в except (транслируется зеленным)

