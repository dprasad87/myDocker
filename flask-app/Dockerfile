From alpine:3.6
RUN echo "http://dl-cdn.alpinelinux.org/alpine/v3.6/community" >> /etc/apk/repositories
RUN apk update
RUN apk add --upgrade py-pip
COPY requirement.txt /usr/src/app/
RUN pip install --no-cache-dir -r /usr/src/app/requirement.txt

COPY app.py /usr/src/app/
COPY templates/index.html /usr/src/app/templates/
EXPOSE 5000

CMD ["python", "/usr/src/app/app.py"]