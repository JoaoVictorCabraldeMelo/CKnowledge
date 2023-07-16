
Como gerar uma chave **ssh** 

### ED25519

```
ssh-keygen -t ed25519 -c "seuemail"
```

### RSA

```
ssh-keygen -t rsa 
```

Inicializar o servidor **ssh**

```
eval "$(ssh-agent -s)"
```

Adicionar uma chave **ssh** para seu servidor

```
ssh-add /caminho/da/sua/chave/publica
```
