---
description: Instruções gerais de como configurar o kubernetes para produção
---

# Kubernetes

## Kubernetes

Antes de rodar o seu arquivo kubernetes você deve atualizar suas variáveis de ambiente do seu projeto, geralmente dentro da pasta kubernetes possuirá um arquivo chamado deploysecrets template

```
kubectl apply -f ./kubernetes/deploysecrets.yml
```

{% hint style="info" %}
Pode ser necessário também configurar da mesma maneira suas credenciais para coletar a imagem docker do dockerhub
{% endhint %}

Depois de configuradas as variáveis de ambiente basta você subir o arquivo de configuração, utilizando o comando abaixo

```text
kubectl apply -f ./kubernetes/nome_do_projeto.yml
```

Para debugar os erros que podem acontecer durante a subida do container há dois comandos importantes que podem ser utilizados.

```text
kubectl describe pod <nome_do_pod>
```

```text
kubectl logs <nome_do_pod>
```

{% hint style="info" %}
Para obter o nome do pod é possível utilizar comando: kubectl get pods
{% endhint %}

