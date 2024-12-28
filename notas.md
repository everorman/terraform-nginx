### Comandos basicos de terraform

```
terraform init
terraform plan
terraform apply
terraform destroy
```

### Comando para generar SSH

```
ssh-keygen -t rsa -b 2048 -f "nginx-server.key" 
```

Prueba SSH
Por default EC2 crea un usuario ec2-user, por lo que para testear el funcionamiento del ssh se ejecutaria en este caso:

```
ssh ec2-user@public-ip -i ./nginx-server.key
```
