FROM ubuntu:18.04

RUN apt update
RUN apt install -y cron

# task.sh, cron-exampleをdocker側にコピー
COPY task.sh /usr/local/bin/
COPY cron-example /etc/cron.d/

RUN chmod 0644 /etc/cron.d/cron-example

CMD ["cron", "-f"]
