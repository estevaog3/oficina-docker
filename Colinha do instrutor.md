# Colinha do instrutor

## Bônus: monitorando containers em background

1. Imagine um container rodando alguma tarefa longa em background: 
```bash
docker run -it ubuntu:20.04 /bin/bash -c "while true; do date +rodando...%S; sleep 2s; done"
```

2. Podemos monitorar a saída padrão do container com o comando: `docker attach --no-stdin CONTAINER`.
Sem a opção `--no-stdin`, podemos também interagir com a entrada padrão do container, o que pode causar uma parada indesejada.


3. Ainda com o container rodando, podemos `exec`utar algum comando *do container* com o comando `docker exec`. Note que o comando precisa existir *no container*, não necessariamente na máquina local (ou *host*).
Dessa forma, para interagirmos com o container, podemos rodar o comando `/bin/bash` nele e pedir para o docker manter a sessão terminal aberta com a opção `-it`.
```bash
docker exec -it CONTAINER ‘/bin/bash’
```
 