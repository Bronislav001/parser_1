
FROM joyzoursky/python-chromedriver:3.9-selenium


WORKDIR /app


COPY backend/requirements.txt .
RUN pip install -r requirements.txt

COPY backend /app/


ENV DB_NAME=${DB_NAME}
ENV DB_USER=${DB_USER}
ENV DB_PASSWORD=${DB_PASSWORD}
ENV DB_HOST=${DB_HOST}
ENV DB_PORT=${DB_PORT}


CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "80"]
