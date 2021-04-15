### Aulas Elastic search

Paralelo banco de relacional -> Elasticsearch
Instância -> Index
Tabela -> Type
Schema -> Mapping
Tupla -> Documento
Coluna -> Atributo

> Documentos no elasticsearch são imutaveis, toda vez que um é criado, na atualização, a versão será trocada

> Shards são partições de um "Catalogo (indice)", é possível fazer replica de shards
> Quebrar o indice em Shards (Partições), ex; 10GB em 5 shards (2.5gb cada) e criar replicas de cada shard

> O campo _all, indexa todo documento em uma única string, então quando fazemos /catalogo/pessoas/_search?q=futebol, ele vai procurar no _all a string futebol. mesma coisa que _search?q=_all:futebol

> Para search em campos especificos: _search?q=estado:SP

* Cabeçalho da response:
    - _shards:
        * total: 1 => Número de shards
        * successful: 1 => Número de shards que obteram os dados com sucesso
        * failed: 0 => Número de shards que falharam em obter os dados
    - Hits
        * Max_core => qual semelhante na busca

* _search
    - size = 1 => Retorna o número de registros igual a 1, páginação
    - from = 1 => A partir do 1


______________________________________________

* Mapping
    - 
