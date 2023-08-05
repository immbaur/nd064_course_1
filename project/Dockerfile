FROM python:3.8

WORKDIR /app

EXPOSE 3111

COPY techtrends/requirements.txt /app/
COPY techtrends/app.py /app/
COPY techtrends/init_db.py /app/
COPY techtrends/schema.sql /app/
COPY techtrends/static /app/static
COPY techtrends/templates /app/templates

RUN pip3 install -r requirements.txt

RUN python init_db.py

CMD ["python", "app.py"]
