FROM quay.io/argoproj/argocd:v2.4.15

USER root

RUN apt-get update && \
    apt-get install -y --no-install-recommends \
    google-cloud-sdk-gke-gcloud-auth-plugin

USER argocd
