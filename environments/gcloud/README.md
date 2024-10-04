* Updated: 2024-10-04 (Fri)
* Created: 2024-10-04 (Fri)

# Google Cloud > Cloud SDK

# Install
Source: Google Cloud > Cloud SDK > Doc. > Guides > [Install the gcloud CLI](https://cloud.google.com/sdk/docs/install#deb)

```bash
# Before you begin
sudo apt-get update
sudo apt-get install apt-transport-https ca-certificates gnupg curl

# Installation
curl https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo gpg --dearmor -o /usr/share/keyrings/cloud.google.gpg
echo "deb [signed-by=/usr/share/keyrings/cloud.google.gpg] https://packages.cloud.google.com/apt cloud-sdk main" | sudo tee -a /etc/apt/sources.list.d/google-cloud-sdk.list
sudo apt-get update && sudo apt-get install google-cloud-cli
```
/[Docker Tip/] If installing the gcloud CLI inside a Docker image, use a single RUN step instead:
```bash
RUN echo "deb [signed-by=/usr/share/keyrings/cloud.google.gpg] https://packages.cloud.google.com/apt cloud-sdk main" | tee -a /etc/apt/sources.list.d/google-cloud-sdk.list && curl https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo gpg --dearmor -o /usr/share/keyrings/cloud.google.gpg && apt-get update -y && apt-get install google-cloud-cli -y
```

# Get started with
```bash
gcloud init
```


