From alpine:3.5
RUN apk add --upgrade python-pip
COPY requirement.txt /usr/src/app/
RUN pip install --no-cache-dir -r /usr/src/app/requirement.txt

COPY app.py /usr/src/app/
COPY templates/index.html /usr/src/app/templates/
EXPOSE 5000

CMD["python", "/usr/src/app/app.py"]