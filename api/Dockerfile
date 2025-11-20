FROM python:3.9

RUN apt-get update && apt-get install -y libgl1

WORKDIR /fabric_defect_api

COPY ./requirements.txt ./requirements.txt
RUN pip install -r requirements.txt

COPY . .

EXPOSE 8080

CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "${PORT}"]
