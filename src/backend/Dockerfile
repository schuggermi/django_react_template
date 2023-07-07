FROM python:3.11

WORKDIR /app/src/backend

ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

COPY requirements.txt /app/src/backend/requirements.txt
RUN pip install --upgrade pip
RUN pip3 install --no-cache-dir -r /app/src/backend/requirements.txt

COPY . /app/src/backend
COPY ./entrypoint.sh /app/src/backend/entrypoint.sh

#EXPOSE 8000
#CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8000", "--reload"]

ENTRYPOINT ["sh", "./entrypoint.sh"]