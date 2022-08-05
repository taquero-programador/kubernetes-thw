# Instalación de gcloud CLI en linux
ir a la pagina de gcloud sdk
bash```
sudo apt-get install apt-transport-https ca-certificates gnupg
`` 

bash```
echo "deb https://packages.cloud.google.com/apt cloud-sdk main" | sudo tee -a /etc/apt/sources.list.d/google-cloud-sdk.list
```

bash```
curl https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo tee /usr/share/keyrings/cloud.google.gpg
```

bash```
sudo apt-get update && sudo apt-get install google-cloud-cli
```


