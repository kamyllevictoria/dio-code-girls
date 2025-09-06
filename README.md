
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
