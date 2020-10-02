# Install Guide: Vault

# Know-How “Hashicorp Vault”
- - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - 

- [ ] Author Gopalam Moram
_ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _  _ _ _ _ _ _ _  _ _ _ _

![Vault](.../vault.jpg)

## What is Vault?

- [ ] It allows you to safely store and manage sensitive data in hybrid cloud environments.
- [ ] It is also called a modern secret management.

## Summary:

- [ ] Install guide for Windows, Linux OS, Mac OS.
- [ ] How to install on different environments and Cloudsexplained.

### Vault installation:

- [ ] Installing Vault is simple. 
- [ ] There are two approaches to install Vault on Windows.
- [x] Using a precompiled binary
- [x] Installing from [source](https://www.vaultproject.io/docs/install)
  
### Installation steps on Linux/Mac OS

#### Pre-requisites:

- [ ] Docker Hub account
- [ ] Running on Linux OS/Mac OS/ Ubuntu OS 
- [ ] Create a virutal machine on AWS/GCP cloud (Optional, instead you use virtual box, easy option to use AWS/GCP  > Provision Virtual machine /EC2 instance, Download docker on top of it to install Vault.

```
Terminology :
+ On GCP: It is called as (Virtual Machine) or (VM)
+ ON AWS: It is called as  (Elastic Cloud Compute)
```

#### Baby steps:

- [ ] [dockerhub](https://hub.docker.com/)
- [ ] Search “Vault” > official image.
- [ ] Copy the query 
```
1. docker pull vault
2. docker images (To list all the docker images)

# expose Vault on 8200 (Vault listener port : 8200)
 
# usage: docker run -d --name {container_name} -p 8200:8200 {image/Image ID}

3. docker run -d --name myvault -p 8200:8200 vault  

4. Docker ps -a  # show all the containers ( Copy the container ID and run the below cmd)

5. Docker logs -f container ID # To get the vault login credentials

6. Copy the logs content vault token login, export, root token In which will use to connect CLI and UI. (see below example)
```
![Example](/Users/gopalam.moram/Documents/login.jpg)

#### Login via CLI

```
1. Export VAULT_ADDR=’http://0.0.0.0:8200’

2. vault login {token which you saved : it starts with "s."}

3. You will be "Authenicated!"
```
##### Gettting started : “First Secrets”

```
# usage
vault kv put secret/{your path} password={password to store}

vault kv put secret/iaccirlce password=weautomateeverthing

see below example

```

![secrets](/Users/gopalam.moram/Documents/sec.jpg)

[first-secret](https://learn.hashicorp.com/vault/getting-started/first-secret)





 	



