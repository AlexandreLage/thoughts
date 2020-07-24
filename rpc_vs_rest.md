Depois de dar uma fork no Kong, tive a seguinte dúvida:
# APIs REST vs APIs RPC?

As APIs baseadas em RPC são ótimas para ações (ou seja, procedimentos ou comandos).

As APIs baseadas em REST são ótimas para modelar seu domínio (isto é, recursos ou entidades), tornando o CRUD (criar, ler, atualizar, excluir) disponível para todos os seus dados.

REST não é apenas CRUD, mas as coisas são feitas principalmente através de operações baseadas em CRUD. REST usará métodos HTTP como GET, POST, PUT, DELETE e OPTIONS para fornecer significado semântico para a intenção da ação sendo tomada.

RPC, no entanto, não faria isso. A maioria usa apenas GET e POST, com GET sendo usado para buscar informações e POST sendo usado para tudo o resto. É comum ver as APIs RPC usando algo como POST /deleteAlgoAgora, passando um corpo {"id":1}


https://medium.com/lfdev-blog/e-agora-api-rest-ou-rpc-c24664d4755b


