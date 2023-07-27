FROM apache/spark:3.4.1

USER root

ENV PATH="${SPARK_HOME}/bin:${SPARK_HOME}/sbin:${PATH}"

RUN apt update && \
		apt install -y libpostgresql-jdbc-java && \
		ln -s /usr/share/java/postgresql-jdbc4.jar ${SPARK_HOME}/jars/postgresql-jdbc4.jar && \
		apt-get remove -y wget && \
		apt-get autoremove -y && \
		apt-get clean

USER spark