# APIs REST - O que são?

    Basicamente, uma API (application programming interface) REST (representational state transfer) é um **conjunto de métodos de comunicaçãoclaramente definidos entre diversos componentes distintos**, utilizando um estilo arquitetural de software chamado **representational state transfer**, ou transferência representacional de estado, em tradução livre, quando em contexto de serviços _web_
    As APIs cuja comunicação se baseia em HTTP possuem certos métodos que auxiliam o entendimento da dinâmica:
    - GET -> "Cata" uma representação do estado do recurso-alvo;
    - POST -> Deixa o recurso-alvo processar a representação anexada no pedido;
    - PUT -> Cria ou substitui o estado do recurso-alvo pelo estado definido pela representação anexada no pedido
    - PATCH -> Atualiza parcialmente o estado de um recurso;
    - DELETE -> Exclui o recurso;
    - OPTIONS -> Mostra as esquisitices opcionais do servidor, não do recurso;

    Aos detalhes: o método GET é seguro, ou seja, não resulta numa mudança do estado do recurso (somente leitura, read-only). Os métodos GET, PUT e DELETE são idempotentes, significando que, ao aplicá-los diversas vezes, o estado alterado resultado será idêntico ao aplicá-los somente uma vez, apesar da resposta obtida poder variar. Os métodos GET e POST são cacháveis (dá pra fazer cachinhos neles, ou armazená-los em memória para uso futuro - e mais rápido).

    Existem alguns tipos diferentes de API além das baseadas na _web_:
    - APIs de sistemas operacionais (como, por exemplo, a API do Win32);
    - APIs de Libraries (ex.: Library de classes do Java, uma Library de usuários);
    - APIs remotas (caindo em desuso), que necessariamente precisam ser escritas na mesma plataforma e se comunicam por protocolos proprietários;
    - WEB APIs (sim, de novo, já que o foco é justamente aqui), que se comunicam por meio de protocolos _web_, na internets.


   
# Quais tipos de APIs web existem?

    SOAP - Simple Object Access Protocol (Protocolo Simples de Acesso a Objetos), baseado em XML.
    REST - Representational State Transfer (Transferência Representacional de Estado), baseado em URL + JSON.
    GraphQL - É uma linguagem de consulta que permite flexibilidade ao atualizar, subscrever e criar queries. Baseado em JSON.
    gRPC - Google Remote Procedure Call. Usa HTTP/2 e buffers de protocolo para codificar os dados, cuja especificação é mais rígida.

# HTTP REST Requests e Responses

    CLIENT ---> GET /api/order/13 ---> SERVER
    CLIENT <---   200 OK, JSON    <--- SERVER

# Estrutura de requisição e resposta de uma REST API

### Estrutura de requisição (request)

    MÉTODO - verbo HTTP (GET, POST, PUT, DELETE...)
    URL - Localização do recurso + parâmetros
    CABEÇALHO - Contém os metadados da requisição (developer.mozilla.org/pt-BR/docs/Web/HTTP/Headers para mais infos)
    CORPO - Conteúdo da requisição, opcional

### Exemplo de requisição (request):

    GET api/v1/entities/13
    User-Agent: PostmanRuntime/7.15.2
    Accept: */*
    Cache-Control: no-cache
    Postman-Token: f7f64f44-2580-4707-8f7c-d3e657bf21ee
    Host: memitest.free.beeceptor.com
    Accept-Encoding: gzip, deflate
    Connection: keep-alive

### Estrutura de resposta (response):

    CÓDIGO - 200 (success), 404 (not found), etc.
    CABEÇALHO - Metadados da resposta
    CORPO - Conteúdo da resposta

### Exemplo de resposta:

    HTTP/1.1 200
    status: 200
    Date: Fri, 02 Aug 2020 10:13:13 GMT
    Content-Type: text/plain
    Transfer-Encoding - chunked
    Connection: keep-alive
    access-control-allow-origin: *
    Vary: accept-encoding
    
    { "orderID" : "13", "orderDate" : "13.10.2019", "items" : [ "id" : "19", "id" : "31"] }





 




