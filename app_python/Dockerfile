FROM python:3-alpine

WORKDIR /main

COPY requirements.txt main.py .

RUN addgroup -S lowuser && adduser -S lowuser -G lowuser && \ 
    chown -R lowuser:lowuser /main && \
    pip install --no-cache-dir -r requirements.txt

USER lowuser

EXPOSE 5000

CMD ["python3", "main.py"]
