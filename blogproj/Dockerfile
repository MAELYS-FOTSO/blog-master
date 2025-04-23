FROM python:3.12
WORKDIR /blogproj
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt
COPY . .
RUN mkdir -p /blogproj/data
VOLUME /blogproj/data
EXPOSE 8000
CMD ["gunicorn", "--chdir", "/blogproj", "--bind", "0.0.0.0:8000", "blogproj.wsgi:application"]
