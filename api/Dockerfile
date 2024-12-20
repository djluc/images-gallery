## din ce imagine creem imaginea noastra
FROM python:3.9
## folderul in care se salveaza fisierele de aplicatie
WORKDIR /app
## portul pe care-l exportam
EXPOSE 5050
## se intaleaza toate dependintele

COPY Pipfile ./
COPY Pipfile.lock ./

RUN pip install pipenv

## salveaza intr-un fisier toate dependintele pentru ca apoi acestea sa fie instalate
RUN pipenv requirements > requirements.txt
## RUN pipenv lock --requirements > requirements.txt 
RUN pip install -r requirements.txt

COPY . ./

CMD ["python", "main.py"]
