# gcp-quick-reference

**Create Keys**

    openssl genrsa -out jwt-rsa.key.pem 2048 #default format
    openssl rsa -in jwt-rsa.key.pem -outform PEM -pubout -out jwt.pub.pem
    openssl pkcs8 -topk8 -in jwt-rsa.key.pem -inform pem -out jwt.key.pem -outform pem -nocrypt #format change

**os-login**

    gcloud compute os-login describe-profile
    gcloud compute os-login ssh-keys add \
        --key-file key-file-path \
        --ttl expire-time
        

**Google Cloud certificate  update**

    sudo apt-get install apt-transport-https ca-certificates gnupg
    curl https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo apt-key --keyring /usr/share/keyrings/cloud.google.gpg add -


**Installing Amazon Jdk on Ubuntu**

    sudo apt-get update
    sudo apt-get install java-common
    wget https://corretto.aws/downloads/latest/amazon-corretto-11-x64-linux-jdk.deb
    sudo dpkg --install amazon-corretto-11-x64-linux-jdk.deb
    rm amazon-corretto-11-x64-linux*




