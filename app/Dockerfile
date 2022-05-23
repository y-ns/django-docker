FROM python:3.10.4
ENV PYTHONUNBUFFERED 1
RUN mkdir /code
WORKDIR /code
COPY requirements.txt /code/
RUN pip install -r requirements.txt
COPY . /code/
WORKDIR /code/
CMD ["gunicorn", "--bind", "0.0.0.0:8000", "app.wsgi:application"]