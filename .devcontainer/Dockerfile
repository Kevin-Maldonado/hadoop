# Usar la imagen base oficial de Ubuntu para Codespaces
FROM mcr.microsoft.com/devcontainers/base:ubuntu

# Actualizar el sistema e instalar Java 8 (La versión más estable para Hadoop), wget y ssh
RUN apt-get update && apt-get install -y openjdk-8-jdk wget ssh rsync

# Descargar y descomprimir Hadoop (versión 3.3.6)
RUN wget https://downloads.apache.org/hadoop/common/hadoop-3.3.6/hadoop-3.3.6.tar.gz && \
    tar -xzvf hadoop-3.3.6.tar.gz && \
    mv hadoop-3.3.6 /usr/local/hadoop && \
    rm hadoop-3.3.6.tar.gz

# Configurar las variables de entorno necesarias para Linux
ENV JAVA_HOME=/usr/lib/jvm/java-8-openjdk-amd64
ENV HADOOP_HOME=/usr/local/hadoop
ENV PATH=$PATH:$HADOOP_HOME/bin:$HADOOP_HOME/sbin
