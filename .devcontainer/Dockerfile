FROM mcr.microsoft.com/devcontainers/java:dev-21

USER root
WORKDIR /

ENV DEBIAN_FRONTEND=noninteractive
ENV PYTHONUNBUFFERED=1
ENV SPARK_HOME=/opt/spark
ENV PATH="${SPARK_HOME}/bin:${SPARK_HOME}/sbin:${PATH}"
ENV PYSPARK_PYTHON=python3
ENV PYSPARK_DRIVER_PYTHON=python3

RUN apt-get update \
    && apt-get install -y --no-install-recommends python3-pip \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

RUN wget -q https://dlcdn.apache.org/spark/spark-4.1.0/spark-4.1.0-bin-hadoop3.tgz \
    && tar -xzf spark-4.1.0-bin-hadoop3.tgz \
    && mv spark-4.1.0-bin-hadoop3 /opt/spark \
    && rm spark-4.1.0-bin-hadoop3.tgz

RUN /usr/bin/python3 -m pip install --disable-pip-version-check --no-cache-dir --break-system-packages --root-user-action=ignore \
    pyspark==4.1.0 \
    ipykernel==7.1.0 \
    pandas==2.3.3 \
    numpy==2.4.0 \
    pyarrow==22.0.0 \
    msal==1.34.0
