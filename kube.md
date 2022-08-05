# Instalación de gcloud CLI en linux
ir a la pagina de gcloud sdk
```bash
sudo apt-get install apt-transport-https ca-certificates gnupg
``` 

```bash
echo "deb https://packages.cloud.google.com/apt cloud-sdk main" | sudo tee -a /etc/apt/sources.list.d/google-cloud-sdk.list
```

```bash
curl https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo tee /usr/share/keyrings/cloud.google.gpg
```

```bash
sudo apt-get update && sudo apt-get install google-cloud-cli
```

## Validas que la versión sea >= 338
```bash
gcloud version
```

## Ajustes
durante el proceso solicita acceso a la cuenta
```bash
gcloud init
```
marco error al seleccionar la opcion 7, se lanza el siguiente comando para crear el proyecto.
```bash
gcloud projects create kuber-init
```
```bash
gcloud config set compute/region us-west1
```
marca error durante la selección de región
```bash
gcloud config set project kuber-init
# se ejecuta de nuevo la region
gcloud config set compute/region us-west1
gcloud config set compute/zone us-west1-c
```
activar la sincronizacion de paneles en tmux
```bash
set synchronize-panes on
```

# Install CFSSL

```bash
[200~wget -q --show-progress --https-only --timestamping \
  https://storage.googleapis.com/kubernetes-the-hard-way/cfssl/1.4.1/linux/cfssl \
  https://storage.googleapis.com/kubernetes-the-hard-way/cfssl/1.4.1/linux/cfssljson
```
```bash
chmod +x cfssl cfssljson
```
```bash
sudo mv cfssl cfssljson /usr/local/bin/
```

# Instalación de kubectl
```bash
wget https://storage.googleapis.com/kubernetes-release/release/v1.21.0/bin/linux/amd64/kubectl
```

```bash
sudo chmod +x kubectl && sudo mv kubectl /usr/local/bin/
```

validar versión de cliente
```bash
kubectl version --client
```
