<p align="center">
    <img src="https://artifacthub.io/image/aec2a822-2a3f-41a6-8a71-57c5d75d011e@3x" width="220" />
</p>

# Minio - Test

Este repositório contém um exemplo prático de como utilizar o MinIO, um servidor de armazenamento de objetos de código aberto. O MinIO é uma solução escalável e de alto desempenho para armazenamento de grandes quantidades de dados não estruturados, como imagens, vídeos e arquivos de log. Neste exemplo, você encontrará instruções passo a passo com utilização do docker para configurar e interagir com o MinIO, incluindo a criação de buckets, o upload e download de objetos, e a integração com aplicativos. Use este repositório como um guia prático para começar a utilizar o MinIO em seus projetos e explorar seu potencial para armazenamento de objetos em ambientes locais ou em nuvem."

## Pré-requisitos

Para execução é necessário ter instalado no ambiente os softwares abaixo nas versões descritas ou superiores:

- Docker

## Execução com Docker

Para demonstração da aplicação foi criado um **docker-compose.yml**, onde é possível configurar algumas variáveis de ambiente e executar a aplicação.

Os passos abaixo devem ser executados na raiz do projeto.

### Up

``` bash
    docker-compose -p minio-test -f docker-compose.yml up -d
```

### Down

``` bash
    docker-compose -p minio-test -f docker-compose.yml down
```

### Acesso
Após iniciar o serviço através  **docker-compose.yml** seguindo a configuração padrão do arquivo, será exposto 2 endpoints, deve ser exibido na linha de comando um log semelhante ao abaixo: 

``` bash

minio-1  | API: http://192.168.0.2:9000  http://127.0.0.1:9000
minio-1  | WebUI: http://192.168.0.2:9001 http://127.0.0.1:9001

```

O endpoint [http://127.0.0.1:9000](http://127.0.0.1:9000) se refere à API e uma documentação detalhada de sua utilização pode ser encontrada [aqui](https://min.io/docs/minio/linux/developers/javascript/API.html).

O endpoint [http://127.0.0.1:9001](http://127.0.0.1:9001) se refere à interface web que possibilita a configurações, ciração de buckets, upload e download de arquivos, entre outros. Mais detalhes dessa interface [aqui](https://min.io/docs/minio/linux/administration/minio-console.html).


Fonte: [MinIo](https://min.io/)