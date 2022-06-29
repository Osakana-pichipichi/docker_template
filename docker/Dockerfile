FROM python:3.8

RUN apt-get update && apt-get install -y \
    gosu \
    x11-apps \
 && apt-get clean \
 && rm -rf /var/lib/apt/lists/*

RUN pip install --upgrade pip

RUN pip install numpy

COPY entrypoint.sh /usr/local/bin/entrypoint.sh
RUN chmod u+x /usr/local/bin/entrypoint.sh
ENTRYPOINT ["/usr/local/bin/entrypoint.sh"]

CMD ["/bin/bash"]