FROM python:3.7-slim

COPY . /app
WORKDIR /app
RUN pip install -r requirements.txt

ENV MODEL_NAME EligibilityModel
ENV SERVICE_TYPE MODEL
ENV PERSISTENCE 0

CMD ls /app
CMD exec seldon-core-microservice $MODEL_NAME --service-type $SERVICE_TYPE --persistence $PERSISTENCE 