From python:3.7.5-slim
RUN pip install flask==2.0.3
WORKDIR /src
COPY ./src/server.py /src/
ENV PORT 80
ENTRYPOINT ["python", "-u", "server.py"]