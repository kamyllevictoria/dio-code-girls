
  <h1>Visão Geral dos Serviços AWS</h1>

  <h2>Amazon EC2 (Elastic Compute Cloud)</h2>
    <p>As instâncias Amazon EC2 (Elastic Compute Cloud) são máquinas virtuais (servidores) que você pode usar na nuvem da Amazon Web Services (AWS). A escolha do tipo de instância ideal depende de fatores como a carga de trabalho, o desempenho necessário e o custo.</p>

  <h3>Propósito Geral</h3>
  <ul>
        <li><strong>Famílias:</strong> <code>T, M, A</code></li>
        <li><strong>Descrição:</strong> São ideais para a maioria das cargas de trabalho, como servidores web, bancos de dados de pequeno a médio porte e aplicações corporativas.</li>
        <li><strong>Características:</strong> Oferecem um equilíbrio entre CPU, memória e recursos de rede.</li>
  </ul>

  <h3>Otimizadas para Computação</h3>
  <ul>
        <li><strong>Famílias:</strong> <code>C</code></li>
        <li><strong>Descrição:</strong> São projetadas para cargas de trabalho que exigem um alto desempenho de processamento.</li>
        <li><strong>Características:</strong> Possuem uma alta proporção de CPU em relação à memória.</li>
  </ul>
    
  <h3>Otimizadas para Memória</h3>
    <ul>
        <li><strong>Famílias:</strong> <code>R, X, Z</code></li>
        <li><strong>Descrição:</strong> São ideais para cargas de trabalho que precisam de muita memória (RAM).</li>
        <li><strong>Características:</strong> Oferecem uma alta proporção de memória em relação à CPU.</li>
    </ul>

  <h3>Otimizadas para Armazenamento</h3>
    <ul>
        <li><strong>Famílias:</strong> <code>I, D, H</code></li>
        <li><strong>Descrição:</strong> São indicadas para cargas de trabalho que exigem alto desempenho de I/O (entrada/saída) e grandes volumes de armazenamento.</li>
        <li><strong>Características:</strong> Possuem armazenamento local (disco SSD ou HDD) de alta velocidade.</li>
    </ul>

  <h3>Computação Acelerada</h3>
    <ul>
        <li><strong>Famílias:</strong> <code>P, G, F, DL</code></li>
        <li><strong>Descrição:</strong> Utilizam hardware especializado, como GPUs ou FPGAs, para acelerar o desempenho de certas tarefas.</li>
        <li><strong>Características:</strong> Possuem processadores gráficos (GPU), FPGAs ou ASICs.</li>
    </ul>

  <h2>Amazon EBS (Elastic Block Store)</h2>
    <p>O EBS fornece armazenamento no nível de bloco. Isso significa que ele se comporta como um disco rígido físico, permitindo que o sistema operacional da sua instância formate o volume, instale um sistema de arquivos e salve dados em blocos.</p>
    
  <h3>Características Principais</h3>
    <ul>
        <li><strong>Durabilidade e Disponibilidade:</strong> Os volumes EBS são replicados automaticamente dentro de uma única Zona de Disponibilidade (AZ) para protegê-los contra a falha de um único componente.</li>
        <li><strong>Escalabilidade:</strong> O EBS permite que você aumente a capacidade de armazenamento de uma instância EC2 de forma flexível sem precisar reiniciá-la.</li>
        <li><strong>Snapshots:</strong> Um snapshot é uma cópia de segurança <em>point-in-time</em> de um volume EBS. Eles são incrementais, o que economiza espaço e tempo.</li>
    </ul>

  <h3>Como o EBS se relaciona com o EC2?</h3>
    <p>O <strong>EC2</strong> fornece o processamento, a memória e a rede. O <strong>EBS</strong> funciona como o <strong>disco rígido</strong> para as instâncias EC2, armazenando o sistema operacional, aplicativos e dados. Sem o EBS, todos os dados da instância seriam perdidos quando ela fosse encerrada.</p>

   <h2>Amazon S3 (Simple Storage Service)</h2>
    <p>O S3 é um serviço de armazenamento de objetos altamente escalável e durável. Ele é projetado para armazenar e recuperar qualquer tipo de dado, de qualquer lugar da web. A maior diferença para o EBS é que ele armazena dados como <strong>objetos</strong> e não como um sistema de arquivos tradicional.</p>

  <h3>Principais Usos</h3>
    <ul>
        <li>Hospedagem de Sites Estáticos</li>
        <li>Backup e Recuperação de Desastres</li>
        <li>Data Lakes</li>
        <li>Armazenamento de Conteúdo</li>
    </ul>

  <h3>Classes de Armazenamento</h3>
    <ul>
        <li><strong>S3 Standard:</strong> Para dados acessados frequentemente.</li>
        <li><strong>S3 Standard-IA (Infrequent Access):</strong> Para dados acessados com pouca frequência.</li>
        <li><strong>S3 One Zone-IA:</strong> Mais econômico, armazena dados em apenas uma Zona de Disponibilidade.</li>
        <li><strong>S3 Glacier Instant Retrieval:</strong> Para arquivamento com acesso imediato.</li>
        <li><strong>S3 Glacier Flexible Retrieval:</strong> Arquivamento de baixo custo com recuperação em minutos ou horas.</li>
        <li><strong>S3 Glacier Deep Archive:</strong> A classe mais barata para arquivamento de longo prazo.</li>
    </ul>

  <h2>Amazon AMI (Amazon Machine Image)</h2>
    <h3>O que são?</h3>
    <p>As AMIs (Amazon Machine Images) são a base para lançar suas instâncias do Amazon EC2. Pense nelas como um molde ou um modelo pré-configurado que contém o sistema operacional e softwares necessários para criar um servidor virtual.</p>

  <h3>Tipos de AMIs</h3>
    <ul>
        <li><strong>AMIs da Comunidade:</strong> Gratuitas, criadas e mantidas por membros da comunidade AWS.</li>
        <li><strong>AMIs do Marketplace:</strong> Pagas, desenvolvidas por fornecedores de software, com aplicativos pré-instalados.</li>
        <li><strong>AMIs Privadas:</strong> Criadas por você a partir de uma instância EC2 configurada, garantindo consistência.</li>
    </ul>

  <h3>Principais benefícios das AMIs</h3>
    <ul>
        <li><strong>Padronização:</strong> Garante que todas as instâncias lançadas sejam idênticas.</li>
        <li><strong>Velocidade e Agilidade:</strong> Permite lançar novas instâncias prontas para uso em minutos.</li>
        <li><strong>Backup e Recuperação de Desastres:</strong> Uma AMI funciona como um backup de uma instância para recuperação rápida.</li>
    </ul>

  <h3>Diagramas feitos em aula: </h3>
<img width="879" height="491" alt="Image" src="https://github.com/user-attachments/assets/5501f958-9100-4773-90c0-ea874a75bf32" />
<img width="862" height="660" alt="Image" src="https://github.com/user-attachments/assets/805aa08e-9fd2-4fa5-86d2-fa0e82f2ef96" />

<img width="708" height="223" alt="Image" src="https://github.com/user-attachments/assets/a35ee529-b62c-417e-b528-ad3e311b81ae" />
<h3>Conhecendo o AWS Step Functions</h3>

<h3>Como funciona?</h3>
<p>
O Step Functions usa um formato chamado Amazon States Language para definir seu fluxo de trabalho. 
É um arquivo JSON que descreve as etapas, as transições entre elas e as ações a serem tomadas. 
Cada etapa é um "estado" que pode ser uma ação (como executar uma função Lambda), uma escolha (como um if/else), ou uma espera. 
O serviço executa a lógica do fluxo de trabalho, garantindo que as etapas ocorram na ordem correta, 
gerenciando erros, tentativas de repetição e o estado de cada execução.
</p>

<h3>Benefícios e Projeto Modelo no AWS Step Functions</h3>
<p>Os benefícios do Step Functions se concentram em simplificar a criação e o gerenciamento de aplicações complexas.</p>

<h4>Benefícios:</h4>
<ul>
  <li><strong>Facilidade de Desenvolvimento:</strong> A interface visual para construir fluxos de trabalho torna o processo intuitivo. Você simplesmente arrasta e solta os serviços e os conecta.</li>
  <li><strong>Tolerância a Falhas:</strong> Ele gerencia automaticamente falhas, permitindo que você defina lógicas de nova tentativa (retries) e tratamento de erros (catch) para lidar com problemas inesperados.</li>
  <li><strong>Monitoramento e Auditoria:</strong> Ele fornece logs e um mapa visual da execução do seu fluxo de trabalho em tempo real. Isso facilita a identificação de gargalos ou problemas.</li>
  <li><strong>Estado e Escala:</strong> O serviço mantém o estado de cada execução, o que é crucial para fluxos de trabalho longos. Ele também escala automaticamente para gerenciar milhares de execuções simultâneas.</li>
</ul>

<h4>Projeto Modelo:</h4>
<p>Um projeto modelo comum é um fluxo de trabalho de processamento de pedidos:</p>
<ul>
  <li><strong>Estado 1 - Receber Pedido:</strong> Executa uma função Lambda para validar os dados do pedido.</li>
  <li><strong>Estado 2 - Processar Pagamento:</strong> Chama um serviço de pagamento externo. Se o pagamento falhar, ele pode retornar ao cliente com um erro. Se for bem-sucedido, ele avança.</li>
  <li><strong>Estado 3 - Atualizar Estoque:</strong> Executa outra função Lambda para subtrair os itens do estoque.</li>
  <li><strong>Estado 4 - Notificar Cliente:</strong> Envia um e-mail de confirmação ao cliente.</li>
  <li><strong>Estado 5 - Enviar para Entrega:</strong> Chama um serviço de entrega para agendar o envio.</li>
</ul>
<p>
O Step Functions orquestra essas cinco etapas, garantindo que o pedido só seja enviado para entrega após o pagamento e a atualização do estoque serem bem-sucedidos.
</p>

<h3>Realizando Validações no AWS Step Functions</h3>
<p>
A validação é a etapa em que você verifica se os dados de entrada ou o resultado de uma etapa atendem aos critérios desejados. 
O Step Functions permite que você faça isso de forma robusta.
</p>

<h4>Como funciona?</h4>
<p>
Você usa o estado <code>Choice</code> para criar uma ramificação condicional no seu fluxo de trabalho. 
O estado avalia uma ou mais condições e, com base nisso, direciona a execução para um estado diferente.
</p>

<h4>Exemplo de validação:</h4>
<p>Imagine que, após a etapa de "Processar Pagamento", você queira verificar o código de retorno.</p>

<pre><code>{
  "ChoiceState": {
    "Type": "Choice",
    "Choices": [
      {
        "Variable": "$.statusCode",
        "NumericEquals": 200,
        "Next": "UpdateInventory"
      },
      {
        "Variable": "$.statusCode",
        "NumericEquals": 400,
        "Next": "Refund"
      }
    ],
    "Default": "HandleError"
  }
}
</code></pre>

<p>
Neste exemplo, o Step Functions avalia a variável <code>$.statusCode</code>:
</p>
<ul>
  <li>Se for <code>200</code> (sucesso), ele passa para a próxima etapa <strong>UpdateInventory</strong>.</li>
  <li>Se for <code>400</code> (erro), ele vai para a etapa <strong>Refund</strong> (reembolso).</li>
  <li>Se for qualquer outro valor, ele segue para o estado <strong>Default</strong> de <strong>HandleError</strong>.</li>
</ul>

<h3>Criando e Executando Lambda no AWS Step Functions</h3>
<p>
O AWS Lambda é um serviço de "computação sem servidor" que permite executar código em resposta a eventos. 
A combinação de Step Functions e Lambda é extremamente poderosa, pois o Step Functions fornece a lógica de orquestração 
e o Lambda fornece a lógica de negócios em código.
</p>

<h4>Como funciona?</h4>
<ul>
  <li><strong>Crie sua função Lambda:</strong> Escreva o código que realiza uma tarefa específica (por exemplo, validação de dados, envio de um e-mail, etc.).</li>
  <li><strong>Defina o estado Task no Step Functions:</strong> No seu arquivo JSON da máquina de estados, você cria um estado do tipo <code>Task</code> e especifica a função Lambda que ele deve chamar.</li>
  <li><strong>Passe dados entre as etapas:</strong> O Step Functions permite que você passe a saída de uma função Lambda como entrada para a próxima etapa, criando um fluxo contínuo de dados.</li>
</ul>

<h4>Exemplo:</h4>
<pre><code>{
  "ValidateData": {
    "Type": "Task",
    "Resource": "arn:aws:lambda:us-east-1:123456789012:function:ValidateFunction",
    "Next": "ChoiceState"
  }
}
</code></pre>

<p>
Neste exemplo, o Step Functions executa a função Lambda <code>ValidateFunction</code>. 
A saída dessa função será então passada para o próximo estado, <code>ChoiceState</code>, 
para que o fluxo de trabalho possa tomar uma decisão com base nos resultados da validação.
</p>

<h1>AWS CloudFormation</h1>

  <p>O <strong>AWS CloudFormation</strong> é um serviço da AWS que permite que você gerencie sua infraestrutura na nuvem de maneira programática, como se fosse código. Essa abordagem é conhecida como <strong>Infraestrutura como Código (IaC)</strong>.</p>

  <p>Em vez de criar manualmente recursos como servidores, bancos de dados e redes através do console da AWS, o CloudFormation permite que você defina toda a sua infraestrutura em um <strong>arquivo de modelo (template)</strong>. Esse arquivo pode ser escrito em <strong>YAML</strong> ou <strong>JSON</strong>.</p>

  <h2>Como ele funciona?</h2>
  <ol>
      <li><strong>Criação de Template:</strong> Você começa criando um template que descreve todos os recursos AWS que você precisa, suas propriedades e como eles se relacionam. Por exemplo, você pode definir que precisa de uma instância EC2, um grupo de segurança associado a ela e um banco de dados RDS.</li>
      <li><strong>Criação de Stack:</strong> Você envia o template para o CloudFormation, que então cria um <strong>stack</strong>. Um stack é uma coleção de recursos AWS que são criados e gerenciados juntos como uma única unidade.</li>
      <li><strong>Provisionamento:</strong> O CloudFormation lê o template e provisiona os recursos na ordem correta, garantindo que as dependências sejam resolvidas. Por exemplo, ele não tentará associar um grupo de segurança a uma instância EC2 antes que a instância seja criada.</li>
      <li><strong>Gerenciamento do Ciclo de Vida:</strong> Com o CloudFormation, você pode facilmente atualizar, excluir ou recriar toda a sua infraestrutura. Se você precisa fazer uma alteração, basta atualizar o template e o CloudFormation aplicará as mudanças de forma segura e controlada.</li>
  </ol>

  <h2>Principais Benefícios</h2>
  <ul>
      <li><strong>Automação e Consistência:</strong> Garante que sua infraestrutura seja replicada de forma consistente em diferentes ambientes (desenvolvimento, teste, produção). Isso elimina erros humanos e economiza tempo.</li>
      <li><strong>Gerenciamento Centralizado:</strong> Um stack do CloudFormation gerencia um grupo de recursos como uma unidade única. Você não precisa se preocupar em gerenciar recursos individuais, o que simplifica muito a administração.</li>
      <li><strong>Controle de Versão:</strong> Como os templates são arquivos de código, você pode armazená-los em sistemas de controle de versão, como o Git. Isso permite rastrear mudanças, reverter para versões anteriores e colaborar em equipes.</li>
      <li><strong>Reuso de Código:</strong> Você pode criar templates reutilizáveis, usando parâmetros para personalizar a implantação. Isso é ideal para criar ambientes repetíveis para diferentes projetos ou clientes.</li>
  </ul>

  <h2>Exemplo Prático</h2>
  <p>Imagine que sua empresa precisa implantar um novo ambiente de e-commerce. Esse ambiente requer:</p>
  <ul>
      <li>Um balanceador de carga (ELB).</li>
      <li>Um grupo de auto scaling para instâncias EC2.</li>
      <li>Um banco de dados RDS.</li>
      <li>Um bucket S3 para armazenar imagens.</li>
  </ul>

  <p>Em vez de criar esses recursos um por um, o que poderia levar horas e ser propenso a erros, você escreve um único template do CloudFormation. Em seguida, você executa o CloudFormation, que cria todos esses recursos em questão de minutos, garantindo que as configurações e as dependências estejam corretas. Se precisar de um ambiente idêntico em outra região, basta usar o mesmo template.</p>

  <p>Em resumo, o CloudFormation é uma ferramenta poderosa para transformar o gerenciamento de infraestrutura em um processo programático, previsível e escalável, essencial para qualquer operação em grande escala na AWS.</p>



