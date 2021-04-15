### ELK Stack

* Elasticseach
    - Engine de search e analytics
* Logstash
    - Processador de dados através de pipelines que consegue receber, transformar e enviar dados simultaneamente (incluindo ao elasticseach)

* Kibana
    - Permite usuários a visualizarem os dados do elasticsearch através de gráficos etc

### Elasticsearch

* Banco de dados Orientado a Documentos
* Engine de Busca
* Análise de dados (Quase um BI)
* Rápido / Escalável
* API Rest / JSON

### Logstash

* Teve início como manipulador de logs
* Evolui para o data processing pipeline
* Eventos podem ser log files entries, chat messages, queues etc
* Funciona com input, filter e output, passsar csv, xml, json
* Recebe eventos e processa e envia para stashes
* Engine coletora de dados em tempo real
* Trabalha com pipelines
* Recebe dados de multiplas fontes
* Normalize / Transforma dados
* Envia dados para múltiplas fontes
* Plugins


* Pode receber logs e processar linha por linha, utilizando Grok pattern, que é basicamente uma expressão regular, podendo organlizar o dado do log para enviar ao elastic search

### Kibana

* Dashboards
* Roda em cima do elastic search
* Constroe gráticos em tempo real
* Ferramenta de visualização e explração de dados
* Usado com: Logs, Análise de séries, Monitoramente de aplicações, e inteligência operacional
* Gráficos interativos, com pie charts, bar charts, line charts etc
* Mapas
* Também pode ser utilizado para medir visitar no website, extremamente útil para os negócios
* Salvar mto tempo de nao precisar implementar
* Possível criar dashboard para system administration (CPF usage, memory usage), dashboard com error, response time, KPIs etcs, Quase todo tipo de dados

### Diferença entre ELK stack para Elastic Stack?

* Beats! (Anuncioado em 2015)
* Lightweight data shipper
* Entregam informações ao Logstash e ao elasticsearch
* Logs, métricas, network data, Audit data, uptime monitoring
* Você pode construir seu próprio Beat

* Elastic Stack
    - Kibana - Elasticsearch - Beats / Logstash

* Elastic
    - Empresa por trás das soluções
    - Cloud Solution
    - Oferecem plugin e recursos licenciados
    - Produtos
        * APM
        * Maps
        * Site search, enterprise search
        * APP search
        * Infrastructure

## Exemplos práticos:

* Utilizar o logstash para importar um banco de dados de cidade no elasticsearch
* Visualizaremos os dados no Kibana
* Filebeat + logstash para importar um conjunto de logs do apache
    - Visualizaremos os dados no kibana
    - Entenderemos o padrão grok
