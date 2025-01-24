### Comandos basicos de terraform

```
terraform init
terraform plan
terraform apply
terraform destroy
```

### Comando para generar SSH

```
ssh-keygen -t rsa -b 2048 -f "nginx-server-qa.key" 
```

Prueba SSH
Por default EC2 crea un usuario ec2-user, por lo que para testear el funcionamiento del ssh se ejecutaria en este caso:

```
ssh ec2-user@public-ip -i ./nginx-server.key
```

### Archivos de variables

Son definidos por .tfvars y podemos tener multiples archivos para diferentes entornos por ejemplo. A la hora de querer aplicar  un archivo en particular se debe indicar el nombre  y se realiza de la siguiente forma: 

```
terraform plan --var-file=qa.tfvars
```

### Módulos

Permiten reutilizar la estructura para poder definir diferentes entornos con sus variables y configuraciones independientes. 

Cada vez que se crea un nuevo módulo se debe ejecutar `terraform init`
