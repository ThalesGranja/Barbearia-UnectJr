# 1. Requisitos Funcionais

<p align="justify">A <i>Tabela 1</i> a seguir contém os Requisitos Funcionais (RF) elicitados utizando a técnica de Brainstorm.</p>

| ID   |                                 Requisito                                 | Prioridade | Requisitos Relacionados |
| :--: | :-----------------------------------------------------------------------: | :--------: | :---------: |
| RF01 | O software deve permitir que o cliente faça o seu próprio cadastro no aplicativo. | Alta | - |
| RF02 | O software deve permitir que o cliente faça login no aplicativo. | Alta | - |
| RF03 | O software deve permitir que o cliente selecione o serviço desejado. | Alta | - |
| RF04 | O software deve permitir que o cliente selecione o profissional. | Alta | - |
| RF05 | O software deve permitir que o cliente agende um horário para o serviço desejado. | Alta | - |
| RF06 | O software deve permitir que o cliente pague o serviço via Pix dentro do aplicativo. | Alta | - |
| RF07 | O software deve fornecer um QR Code e uma chave aleatória para o cliente efetuar o pagamento. | Alta | RF06 |
| RF08 | O software deve permitir que o cliente escolha receber lembrete do horário agendado. | Baixa | - |
| RF09 | O software deve permitir que o cliente defina a antecedência do lembrete (dias, horas ou minutos). | Baixa | RF08 |
| RF10 | O software deve enviar uma mensagem de lembrete via WhatsApp conforme definido pelo cliente. | Alta | RF08, RF09 |
| RF11 | O software deve permitir que o cliente edite as informações de seu cadastro. | Alta | - |
| RF12 | O software deve permitir que o cliente consulte seus agendamentos (serviço, dia, horário e barbeiro). | Alta | - |
| RF13 | O software deve permitir que o cliente saia (Log Out) do aplicativo. | Alta | - |
| RF14 | O software deve permitir que o cliente escolha o tema de sua preferência (claro/escuro). | Baixa | - |
| RF15 | O software deve permitir que o cliente veja fotos dos serviços disponibilizados pela barbearia na página Home em formato de carrossel. | Baixa | - |
| RF16 | O software deve permitir que o cliente cancele ou remarque um horário previamente agendado. | Alta | RF05 |
| RF17 | O software deve permitir que o cliente edite um horário previamente agendado apenas até 24 horas antes do horário reservado, bloqueando alterações após esse prazo. | Alta | RF16 |
| RF18 | O software deve enviar uma mensagem de lembrete via WhatsApp para os barbeiros os relembrando dos atendimentos do dia | Alta | RF05 |
| RF19 | O software deve permitir que o gestor gerencie os horários de funcionamento (podendo bloquear horários indisponíveis). | Média | - |
| RF20 | O software deve permitir que o gestor agende horários para clientes já cadastrados. | Baixa| RF05 |
| RF21 | O software deve permitir que o gestor agende horário para clientes não cadastrados (voltado para pessoas de mais idade). | Baixa | RF05 |
| RF22 | O software deve permitir que o gestor cadastre barbeiros com foto, nome e especialidade. | Alta | - |
| RF23 | O software deve permitir que o gestor acesse o histórico de agendamentos e preferências dos clientes. | Alta | RF05, RF12 |
| RF24 | O software deve permitir que o gestor crie, edite e remova serviços. | Alta | - |
| RF25 | O software deve permitir que o gestor atualize preços e descrições dos serviços exibidos no aplicativo. | Alta | RF24 |
| RF26 | O software deve alterar o status de um cliente para inativo caso ele não agende nenhum horário em 3 meses, exceto usuários com status "viajante". | Média | RF05 |
| RF27 | O software deve enviar notificações de promoções de cortes para clientes com status inativo. | Alta | RF26 |
| RF28 | O software deve gerar um relatório de desempenho da barbearia (mostrando: faturamento, despesas e lucro). | Alta | - |
| RF29 | O software deve gerar um relatório de frequência dos clientes (ativos e inativos). | Média | RF26 |

<div style="text-align: center">
<p>Tabela 1: Requisitos Funcionais</p>
</div>

# 2. Referências


<a href="../README.md">VOLTAR INÍCIO</a>





