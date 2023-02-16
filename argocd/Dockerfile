FROM quay.io/argoproj/argocd:v2.6.1

USER root

RUN apt-get update \
    && apt-get install -y --no-install-recommends \
    apt-transport-https ca-certificates gnupg curl \
    && echo "deb [signed-by=/usr/share/keyrings/cloud.google.gpg] https://packages.cloud.google.com/apt cloud-sdk main" \
    > /etc/apt/sources.list.d/google-cloud-sdk.list \
    && curl https://packages.cloud.google.com/apt/doc/apt-key.gpg | apt-key --keyring /usr/share/keyrings/cloud.google.gpg add - \
    && apt-get update \
    && apt-get install -y --no-install-recommends \
    google-cloud-sdk-gke-gcloud-auth-plugin google-cloud-cli

USER argocd
