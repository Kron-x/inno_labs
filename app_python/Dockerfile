FROM python:3-alpine

RUN addgroup -S lowuser && adduser -S lowuser -G lowuser

WORKDIR /main

COPY requirements.txt .

RUN pip install --no-cache-dir -r requirements.txt

COPY main.py .

RUN chown -R lowuser:lowuser /main

USER lowuser

EXPOSE 5000

CMD ["python3", "main.py"]
