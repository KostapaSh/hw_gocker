FROM python:3.11
#FROM nginx

WORKDIR /apps

COPY ./apps /apps

RUN pip install --upgrade pip && pip install -r /apps/requirements.txt

ENV SECRET_KEY = 'django-insecure-nw^y+m^wmxza1asgk+)!ua465437347sehsb46wbw37'
ENV DEBUG = True

RUN python manage.py migrate
CMD [ "python", "./manage.py", "runserver", "0.0.0.0:8000"]
