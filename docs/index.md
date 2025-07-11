<h2><a href= "https://www.mackenzie.br">Universidade Presbiteriana Mackenzie</a></h2>
<h3><a href= "https://www.mackenzie.br/graduacao/sao-paulo-higienopolis/sistemas-de-informacao">Sistemas de Informação</a></h3>


<font size="+12"><center>
*&lt;Sistema Falcão Sombrio para Drones&gt;*
</center></font>

>*Observação 1: A estrutura inicial deste documento é só um exemplo. O seu grupo deverá alterar esta estrutura de acordo com o que está sendo solicitado na disciplina.*

>*Observação 2: O índice abaixo não precisa ser editado se você utilizar o Visual Studio Code com a extensão **Markdown All in One**. Essa extensão atualiza o índice automaticamente quando o arquivo é salvo.*

**Conteúdo**

- [Autores](#nome-alunos)
- [Descrição do Projeto](#introdução-do-projeto)
- [Análise de Requisitos Funcionais e Não-Fucionais](#descrição-dos-requisitos)
- [Diagrama de Atividades](#diagrama-de-atividades) 
- [Diagrama de Casos de Uso](#diagrama-de-comportamento-atores)
- [Descrição dos Casos de Uso](#descrição-das-funcões)
- [Diagrama de Senquencia](#diagrama-de-ordem-interações)
- [Diagrama de Classes](#diagrama-orientado-objetos)
- [Diagrama de Estados](#diagrama-estrutura-componente)
- [Diagrama de Implantação](#diagrama-de-hardware-software)
- [Referências](#referências)


# Autores

* Aluno 1 Beatriz Aparcida de Mello Barbosa
* Aluno 2 Gabriel Pereira Faravola
* Aluno 3 Guilherme Haddad Borro
* Aluno 4 Henrique Jeam Ferreira Lima

# Descrição do Projeto

*A Securus Dynamics está desenvolvendo o Falcão Sombrio, um novo sistema que permitirá o controle remoto e autônomo de seus drones por meio de uma rede de servidores distribuídos e uma interface avançada. O projeto enfrenta desafios como segurança, concorrência e tempo real nos sistemas operacionais, além de questões de armazenamento distribuído, replicação e auditoria nos bancos de dados. Diante de falhas na arquitetura atual, a empresa contratou a Consultoria Cyber Bullet System (Turma 4G) para reformular toda a estrutura de software e definir um novo modelo de banco de dados que suporte as operações críticas dos drones.*

# Análise de Requisitos Funcionais e Não-Funcionais (Fase I)

 <ins> **Requisitos Funcionais:** </ins>
| ID | RF | Descrição |
|-|-|-|
|RF1| Autenticação de Operadores| O sistema deve permitir a autenticação dos operadores utilizando biometria e autenticação multifator (MFA).|
|RF2| Controle de frotas| O sistema deve possibilitar o gerenciamento remoto e autônomo de múltiplos drones simultaneamente.|  
|RF3| Interface de comando e controle| Deve existir uma interface gráfica para os operadores visualizarem telemetria, status e executar comandos sobre os drones.|
|RF4| Navegação autônoma| Os drones devem ser capazes de realizar missões táticas sem intervenção humana, utilizando sensores como LIDAR, GPS e visão computacional.|
|RF5| Comunicação Segura| A troca de informações entre os drones e o sistema de controle deve ser realizada utilizando criptografia ponta a ponta.|
|RF6| Registro de Missões| O sistema deve registrar dados de cada missão, incluindo logs detalhados das operações realizadas.|
|RF7| Monitoramento em Tempo Real| Os drones devem transmitir dados de telemetria, status e eventos críticos continuamente para o sistema central.|
|RF8| Gerenciamento de Atualizações| O sistema deve permitir a atualização remota de firmware dos drones, garantindo segurança e conformidade operacional.|
|RF9| Failover e Recuperação| Em caso de falha de servidor, o sistema deve permitir o redirecionamento automático das operações para um servidor de backup.|
|RF10| Auditoria de Eventos| Todos os acessos e comandos devem ser armazenados em logs de auditoria imutáveis para fins de segurança e conformidade.|


 <ins> **Requisitos Não Funcionais:** </ins>
|ID | RNF | Descrição |
|-|-|-|
|RNF1| Segurança| O sistema deve implementar criptografia AES-256 para armazenamento de dados e TLS para comunicação.|
|RNF2| Desempenho| A latência da comunicação entre um drone e o sistema não pode ultrapassar 50ms em condições normais.|
|RNF3| Disponibilidade| O sistema deve estar disponível 24/7, com 99,9% de uptime, garantindo operação contínua em missões críticas.|
|RNF4| Escalabilidade| A arquitetura deve permitir a adição de novos drones eservidores sem comprometer a performance e segurança.|
|RNF5| Armazenamento Distribuído| O banco de dados deve ser replicado geograficamente para garantir redundância e integridade dos dados.|
|RNF6 |Conformidade (Boas Práticas)| O sistema deve atender a padrões de segurança como ISO 27001 e NIST 800-53 para segurança cibernética.|
|RNF7| Resiliência| O sistema deve garantir recuperação automática de falhas em até 05 segundos sem perda de dados.|
|RNF8| Tolerância a Falhas| A arquitetura deve suportar balanceamento de carga e replicação para evitar pontos únicos de falha.|
|RNF9| Eficiência Energética| Os drones devem otimizar o consumo de bateria utilizando algoritmos de inteligência artificial para gestão de energia.|
|RNF10| Log e Auditoria| Os logs devem ser armazenados por no mínimo 05 anos e protegidos contra alteração ou exclusão.|


# Diagrama de Atividades (Fase II)

![diagrama](https://github.com/user-attachments/assets/3441ac48-9478-4d90-aee6-326a47ad287d)


# Diagrama de Casos de Uso (Fase III)

![CasosDeUso](https://github.com/user-attachments/assets/6f8e62ce-7976-4843-aa66-bbe842688690)


# Descrição dos Casos de Uso (Fase IV)

 <ins> **Requisitos dos Casos de Uso:** </ins>
|Ator | Descrição |
|-|-|
|Operador|1- O operador fornece credenciais de acesso.|
|-|2- O sistema verifica a autenticidade das informações.|
|-|3- O operador é autenticado com sucesso.|
|-|4- Somente operadores autorizados podem acessar o sistema.|
|-|5- O drone deve estar fisicamente disponível.|
|-|6- O operador liga o drone.|
|-|7- O sistema realiza checagem dos componentes.|
|-|8- Sensores, GPS e bateria são verificados.|
|-|9- O sistema é iniciado e pronto para uso.|
|-|10- Nenhuma missão pode ser iniciada sem a inicialização completa do sistema.|
|-|11- O operador seleciona o modo manual.|
|-|12- O sistema transfere o controle da IA para o operador.|
|-|13- O operador envia comandos em tempo real.|
|-|14- O controle manual deve ser possível a qualquer momento por questões de segurança.|
|-|15- O operador mantém o envio de comandos.|
|-|16- O sistema continua executando os comandos em tempo real.|
|-|17- O operador finaliza a operação ou troca para modo automático.|
|-|18- O operador seleciona o modo autônomo.|
|-|19- A IA deve estar operacional para assumir o controle.|
|-|20- O sistema transfere o controle do operador para a IA.|
|-|21- A IA retoma ou inicia o controle de voo.|
|-|-|
|IA|1- A missão é atribuída à IA.|
|-|2- A IA determina as coordenadas do local da missão.|
|-|3- O drone decola e inicia o deslocamento.|
|-|4- A IA utiliza GPS e sensores para navegação e desvio de obstáculos.|
|-|5- A IA deve evitar obstáculos automaticamente durante o trajeto.|
|-|6- O drone chega ao ponto da missão, pronto para executá-la.|
|-|7- O drone identifica a tarefa definida para a missão.|
|-|8- A tarefa só deve ser iniciada se o drone estiver no local correto.|
|-|9- Os dados (se houver) são registrados e armazenados.|
|-|10- A tarefa é monitorada até sua conclusão.|
|-|11- A missão é finalizada.|
|-|12- A IA calcula a rota de retorno à base.|
|-|13- O drone inicia o trajeto de volta.|
|-|14- Obstáculos são evitados automaticamente.|
|-|15- O drone retorna com segurança à base de controle.|
|-|16- O drone aterrissa na base.|


# Diagrama de Sequência (Fase V)

![Sequencia drawio](https://github.com/user-attachments/assets/3adc7714-477e-44e8-843a-b874f2962232)


# Diagrama de Classes (Fase VI)

![Diagrama_Classes drawio](https://github.com/user-attachments/assets/b159765c-18b8-4a23-8712-d9dc8b5b881f)


# Diagrama de Estados (Fase VII)

![Estados drawio](https://github.com/user-attachments/assets/ab6b6147-c99b-404b-815d-4a293c526196)


# Diagrama de Implantação (Fase VIII)

![implementacao drawio](https://github.com/user-attachments/assets/add6da70-d4f1-49d8-9867-b06c645810fa)

# Referências

*&lt;Lista de referências&gt;*
