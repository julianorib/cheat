# Helm Cheat Sheet

### Quick Referente

<https://helm.sh/docs/intro/cheatsheet/>


### Repositório

| Comando | Descrição | 
|---------|-----------|
| helm repo add stable https://charts.helm.sh/stable | Adicionar um novo Repositorio |
| helm repo update | Atualizar um Repositorio |
| helm repo list | Listas os Repositórios |
| helm repo remove stable | Remover um Repositorio |


### Aplicações

Instalar uma aplicação:
```
helm update --install chartnovo repo/chart
```

| Options | Descrição |
|---------|-----------|
| --create-namespace -n nomenamespace  | Criar e Informar o namespace |
| --values values.yaml | Informar um arquivo de opções / variáveis |
| --dry-run --debug | Executar um teste sem instalar |
| --version <version_number> | Especificar a versão do Chart |

Remover uma aplicação:
```
helm uninstall chart 
helm uninstall chart -n namespace
```


### Pacote (Chart)

Instalar um plugin de push:
```
helm plugin install https://github.com/chartmuseum/helm-push
```

| Options | Descrição |
|---------|-----------|
| helm create <chart> | Criação de um Chart |
| helm package <chart> | Build do Chart |
| helm repo add <chart> <endereço> | Adicionar o Repositorio |
| helm cm-push <chart>-0.1.0.tgz chart | Fazer upload/push no Repositório |