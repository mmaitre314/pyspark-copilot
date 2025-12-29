# PySpark Copilot

Use GitHub Copilot to author PySpark notebooks running locally in VSCode.

## QuickStart

Open the Dev Container in VSCode and run one of the demo notebooks.

## Test

Build & test the Docker container:
```bash
docker build -t pyspark-copilot .devcontainer
docker run -it pyspark-copilot
```

## References

- VSCode Dev Containers https://code.visualstudio.com/docs/devcontainers/containers
- Spark https://spark.apache.org/docs/latest/
- Local PySpark dev environment https://github.com/jplane/pyspark-devcontainer
- Hadoop Azure Support: ABFS - Azure Data Lake Storage Gen2 https://github.com/apache/hadoop/blob/trunk/hadoop-tools/hadoop-azure/src/site/markdown/index.md
