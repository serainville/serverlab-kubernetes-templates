FROM google/cloud-sdk:alpine

ENV GOOGLE_PROJECT serverlab
ENV GOOGLE_CLIENT_EMAIL shane.rainville@gmail.com
ENV DB_USER \
    DB_PASS \   
    DB_NAME  \
    DB_HOST  \
    ALL_DATABASES  \
    IGNORE_DATABASES  \
    GS_STORAGE_BUCKET demo-backup-serverlab

COPY service-account.json /root/service_key.json
COPY backup.sh /root/backup.sh

RUN gcloud config set project $GOOGLE_PROJECT && \
    gcloud auth activate-service-account --key-file /root/service_key.json && \
    gsutil ls gs://$GS_STORAGE_BUCKET/


VOLUME ["/root/.config"]

