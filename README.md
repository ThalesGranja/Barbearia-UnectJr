# Documentação Barbearia - Unect Jr.

## 1. Introdução

### 1.1 Integrantes do Grupo
- Artur Bertoluci
- Íkaro Alexandre
- Jad Martins
- Thales Granja

### 1.2 Análise do Problema
Atualmente, a barbearia realiza seu atendimento de forma manual, utilizando papel e mensagens informais para controlar agendamentos. Esse modelo gera uma série de limitações e problemas:  
- Gestão ineficiente dos horários:  
Agendamentos são registrados manualmente, o que aumenta a chance de erros (ex.: marcação duplicada, esquecimento de horários) e barbeiros não possuem acesso claro à sua agenda, dependendo do gestor para verificar horários.

- Dificuldade para clientes:  
Para agendar, o cliente precisa enviar mensagens ou se deslocar até o local, não há autonomia para consultar serviços, profissionais disponíveis ou histórico de atendimentos e cancelamentos ou remarcações dependem de contato manual com a barbearia.

- Ausência de relatórios gerenciais:  
O gestor não consegue mensurar com precisão e facilidade o faturamento, despesas, lucro e frequência dos clientes, e também fica difícil tomar decisões estratégicas (promoções, dimensionamento de equipe, controle de custos).

- Falta de comunicação automatizada:  
Não há lembretes automáticos para clientes sobre os horários marcados e o risco de faltas aumenta devido à ausência de notificações.

- Baixa escalabilidade e profissionalismo:  
O modelo atual limita a expansão do negócio e a percepção de modernidade e conveniência para os clientes é prejudicada.

Em resumo, o cenário atual gera ineficiência operacional, má experiência do cliente e falta de informações estratégicas para a gestão da barbearia.

### 1.3 Proposta de Solução
Propõe-se o desenvolvimento e implementação de um sistema de gestão de barbearia (aplicativo móvel) com funcionalidades para clientes, barbeiros e gestor, atendendo aos requisitos funcionais e não funcionais levantados.

#### 1.3.1 Objetivos da Solução
- Automatizar o agendamento: permitir que o cliente escolha serviço, barbeiro, data e horário diretamente no aplicativo, reduzindo erros e trabalho manual.
- Liberdade para barbeiros e clientes: cada usuário terá acesso direto a suas agendas, serviços contratados e histórico.
- Fornecer relatórios inteligentes: possibilitar que o gestor visualize indicadores financeiros e de frequência dos clientes.
- Aprimorar a comunicação: lembretes automáticos via notificação push e WhatsApp, reduzindo faltas e aumentando a satisfação.
- Garantir segurança e confiabilidade: dados criptografados, autenticação de usuários e disponibilidade mínima de 95%.
- Melhorar a experiência do cliente: interface simples, intuitiva e compatível com Android e iOS.

#### 1.3.2 Benefícios Esperados
- Clientes
  - Autonomia para agendar, remarcar ou cancelar horários sem depender de contato manual.
  - Recebimento de lembretes automáticos.
  - Acesso a histórico de serviços e feedback digital.
- Barbeiro
  - Agenda digital própria, com visualização clara dos horários marcados.
  - Redução de imprevistos devido a confirmações automáticas.
- Gestor
  - Controle centralizado dos barbeiros, horários e serviços.
  - Geração de relatórios de desempenho (faturamento, despesas, lucro).
  - Geração de relatórios de frequência dos clientes (ativos, inativos, em análise).
  - Possibilidade de aplicar promoções e estratégias baseadas em dados.

#### 1.3.3 Diferenciais da Solução
- Sistema multiusuário (cliente, barbeiro, gestor).
- Pagamento integrado via Pix com chave dinâmica.
- Personalização de notificações (push, WhatsApp, lembretes).
- Relatórios gerenciais detalhados.
- Interface responsiva e amigável, acessível em mobile.

## 2. Documentos 

### 2.1 Requisitos Funcionais  

| ID       | Requisito                                                                                                                                                     | Prioridade | Requisitos Relacionados |
| -------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | ----------------------- |
| `[RF01]` | O sistema deve permitir que o cliente realize seu próprio cadastro no aplicativo.                                                                             | Alta       | -                       |
| `[RF02]` | O sistema deve permitir que o cliente realize login no aplicativo.                                                                                            | Alta       | RF01                    |
| `[RF03]` | O sistema deve permitir que o cliente selecione o serviço desejado.                                                                                           | Alta       | -                       |
| `[RF04]` | O sistema deve permitir que o cliente selecione o profissional desejado.                                                                                      | Alta       | RF03                    |
| `[RF05]` | O sistema deve permitir que o cliente agende um dia e horário para o serviço escolhido.                                                                       | Alta       | RF03, RF04              |
| `[RF06]` | O sistema deve permitir que o cliente realize o pagamento do serviço via Pix diretamente no aplicativo.                                                       | Alta       | RF05                    |
| `[RF07]` | O sistema deve permitir que o cliente copie uma chave Pix para efetuar o pagamento fora do aplicativo, caso prefira.                                          | Alta       | RF06                    |
| `[RF08]` | O sistema deve permitir que o cliente opte por receber lembretes de seus agendamentos.                                                                        | Média      | RF05                    |
| `[RF09]` | O sistema deve permitir que o cliente configure a antecedência dos lembretes (dias, horas, minutos).                                                          | Média      | RF08                    |
| `[RF10]` | O sistema deve permitir que o cliente edite as informações de seu cadastro.                                                                                   | Alta       | RF01                    |
| `[RF11]` | O sistema deve permitir que o cliente consulte seus agendamentos (serviço, dia, horário e profissional).                                                      | Alta       | RF05                    |
| `[RF12]` | O sistema deve permitir que o cliente encerre sua sessão (logout).                                                                                            | Alta       | RF02                    |
| `[RF13]` | O sistema deve permitir que o cliente escolha o tema de sua preferência (claro ou escuro).                                                                    | Baixa      | -                       |
| `[RF14]` | O sistema deve exibir fotos dos serviços disponibilizados pela barbearia na tela inicial, em formato de carrossel.                                            | Baixa      | -                       |
| `[RF15]` | O sistema deve permitir que o cliente altere um agendamento previamente marcado (remarcar ou cancelar).                                                       | Alta       | RF05                    |
| `[RF16]` | O sistema deve permitir que cada barbeiro visualize seus próprios agendamentos.                                                                               | Alta       | RF05                    |
| `[RF17]` | O sistema deve permitir que o gestor configure os horários de funcionamento da barbearia, podendo bloquear horários para indisponibilidade.                   | Alta       | -                       |
| `[RF18]` | O sistema deve permitir que o gestor agende serviços para clientes já cadastrados.                                                                            | Alta       | RF05, RF01              |
| `[RF19]` | O sistema deve permitir que o gestor agende serviços para clientes não cadastrados (ex.: pessoas de mais idade).                                              | Alta       | RF05                    |
| `[RF20]` | O sistema deve permitir que o gestor cadastre barbeiros com foto, nome e especialidade.                                                                       | Alta       | -                       |
| `[RF21]` | O sistema deve permitir que o gestor acesse o histórico de agendamentos e preferências dos clientes.                                                          | Alta       | RF05, RF11              |
| `[RF22]` | O sistema deve permitir que o gestor crie, edite e remova serviços.                                                                                           | Alta       | -                       |
| `[RF23]` | O sistema deve permitir que o gestor atualize preços e descrições dos serviços exibidos no aplicativo.                                                        | Alta       | RF22                    |
| `[RF24]` | O sistema deve permitir que o gestor altere o status dos clientes (inativo e viajante).                                                                       | Alta       | RF01                    |
| `[RF25]` | O sistema deve permitir que o gestor gere relatórios de desempenho da barbearia (faturamento, despesas, lucro).                                               | Alta       | -                       |
| `[RF26]` | O sistema deve permitir que o gestor gere relatórios de frequência dos clientes (ativos, inativos e em análise).                                              | Alta       | -                       |
| `[RF27]` | O sistema deve alterar automaticamente o status de um cliente para **“em análise”** caso ele não realize agendamentos por 3 meses (exceto status “viajante”). | Alta       | RF24                    |
| `[RF28]` | O sistema deve alterar automaticamente o status de um cliente para **“ativo”** assim que ele efetuar um novo agendamento (exceto status “viajante”).          | Alta       | RF24                    |
| `[RF29]` | O sistema deve enviar uma notificação push solicitando feedback do cliente no dia seguinte à realização do serviço.                                           | Baixa      | RF05                    |
| `[RF30]` | O sistema deve enviar, via WhatsApp, lembretes automáticos de agendamento no horário configurado pelo cliente, se este tiver optado por recebê-los.           | Alta       | RF08, RF09              |
| `[RF31]` | O sistema deve restringir o cadastro de clientes a usuários com idade mínima de 12 anos, salvo exceções definidas pelo gestor.                                | Alta       | RF01                    |
| `[RF32]` | O sistema deve enviar notificações de promoções para clientes com status **“em análise”**.                                                                    | Média      | RF24, RF27              |
| `[RF33]` | O sistema deve permitir que o cliente edite ou cancele um agendamento somente até 24 horas antes do horário marcado.                                          | Alta       | RF15                    |



### 2.2 Requisitos Não Funcionais

| ID        | Requisito                                                                                                                                          | Prioridade |
| --------- | -------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- |
| `[RNF01]` | A interface do sistema deve ser intuitiva e de fácil utilização, permitindo que novos usuários aprendam a operá-la em até 2 minutos.               | Alta       |
| `[RNF02]` | O sistema deve permitir a conclusão de um agendamento com no máximo 6 interações (cliques/toques) por meio de uma interface otimizada e eficiente. | Média      |
| `[RNF03]` | O sistema deve fornecer uma seção de ajuda online de fácil acesso e visibilidade em todas as telas principais.                                     | Alta       |
| `[RNF04]` | O sistema deve suportar, no mínimo, 5 requisições simultâneas por segundo para garantir agilidade na confirmação de agendamentos.                  | Baixa      |
| `[RNF05]` | O instalador do sistema não deve ultrapassar 250 MB.                                                                                               | Alta       |
| `[RNF06]` | O sistema deve suportar, no mínimo, 10 usuários simultâneos sem perda perceptível de desempenho.                                                   | Média      |
| `[RNF07]` | O sistema deve estar disponível (uptime) em pelo menos 95% do tempo mensal (máximo de 36 horas de indisponibilidade por mês).                      | Alta       |
| `[RNF08]` | Em caso de falha, o sistema deve garantir a recuperação dos dados do usuário a partir de backups.                                                  | Alta       |
| `[RNF09]` | O sistema deve ser compatível com Android e iOS.                                                                                                   | Alta       |
| `[RNF10]` | Todos os relatórios gerados devem seguir o padrão de cabeçalho e rodapé definido pela empresa.                                                     | Alta       |
| `[RNF11]` | O sistema deve ser desenvolvido utilizando **React Native** para front-end e **JavaScript/Node.js** para back-end.                                 | Média      |
| `[RNF12]` | O sistema deve integrar-se de forma segura com o sistema bancário para processamento de pagamentos.                                                | Alta       |
| `[RNF13]` | O sistema não deve expor informações pessoais de clientes a operadores não autorizados.                                                            | Alta       |
| `[RNF14]` | O acesso a dados sensíveis deve ser protegido por autenticação e autorização robustas.                                                             | Alta       |
| `[RNF15]` | Os dados sensíveis dos clientes devem ser armazenados e transmitidos utilizando criptografia forte.                                                | Alta       |


### 2.3 Protótipos

Apara acessar os protótipos feitos basta clicar [Aqui!](https://www.figma.com/design/0nWVZf9TDifDz3NfcDGRVs/Barbershop-PSUnect?node-id=0-1&p=f&t=yIVJuAg5K3oTrdqS-0)