
# 1. Introdução 
O Brasil é um país tropical com mais de 8 milhões de km² (MARQUES, s.d), banhado pelo oceano Atlântico e com os mais variados pontos turísticos. De norte a sul, leste a oeste, o país conta com uma cultura vasta e belezas naturais que englobam climas quentes e frios, paisagens paradisíacas, ambientes de lazer e descanso, o que motiva cada vez mais brasileiros a investirem em passeios e lazer.
As atividades turísticas, de acordo com o IBGE, cresceram em 29,9% no ano de 2022 e a entidade prevê um crescimento neste ano de 2,5% em relação ao ano anterior, quando o setor finalmente superou a ociosidade enfrentada pela pandemia do COVID-19 (AMORIM, 2023). 
Em função da alta demanda turística, consequentemente o Brasil registrou no ano de 2022 uma média mensal de cerca de 30 mil voos de janeiro a outubro deste mesmo ano, de acordo com o mais recente relatório da Associação Brasileira de Aviação Geral (ABAG) (MENEZES, 2023).
Neste contexto, o projeto busca desenvolver uma aplicação para projeto de negócio voltada para o setor turístico. Inicialmente, a aplicação trabalhará apenas com voos domésticos (nacionais), além de oferecer pacotes de viagens incluindo aquisição de passagens aéreas, estadia em hotéis, serviços de translado in/out e outros serviços que as demais agências de turismo oferecem. O projeto visa a seriedade e compromisso com seus clientes à luz do recém ocorrido com os clientes da empresa 123 milhas que suspendeu a linha promo e afetou centenas de clientes (CATTO, 2023). Trazer uma excelente proposta de negócio visando lucratividade somada à melhor experiência de seus clientes é o foco da aplicação. 




# 1.1. Objetivos geral e específicos
- Objetivo Geral: Otimizar os processos de negócio na área de agência de viagem.

  
## Objetivos Específicos:
  - Agilizar os processos de negócio da área envolvida;
  - Modernizar as práticas costumeiras atuais;
  - Automatizar os processos de negócio;
  - Organizar as informações processuais;
  - Oferecer uma facilitação para o negócio.



## 1.2. Justificativas
Os sites são vitais para agências de viagens, simplificando o planejamento e reserva de viagens para as pessoas. Eles oferecem conveniência ao explorar destinos, comparar opções e personalizar itinerários. Além disso, proporcionam informações detalhadas, avaliações de outros viajantes e ofertas especiais, facilitando a comunicação e transações online seguras. Em resumo, os sites tornaram-se um recurso indispensável, garantindo praticidade, informações completas e serviços confiáveis aos viajantes.



# 2. Participantes do processo de negócio
Os participantes desempenham um papel crucial nos processos de negócios, sendo os verdadeiros motores que impulsionam a eficiência e o sucesso das operações empresariais, 
tendo o poder de moldar a cultura organizacional. Seu comprometimento, ética de trabalho e colaboração afetam diretamente o ambiente interno. 

Perfis dos Stakeholders: 
 - Clientes: Utilizadores e financiadores do serviço, desde compradores de pacotes ou diárias em hotéis e voos.

- Fornecedores: Inclui companhias aéreas, hotéis, empresas que, em geral, fornecem serviços e produtos que a agência de viagens oferece aos clientes.



# 3.1. Análise da situação atual (AS-IS) 

- Gerenciar clientes 
A problemática do modelo atual do acesso de clientes a plataforma se dá pela necessidade de cadastro no site para se acessar os valores e datas dos planos de hotéis e voos.

Neste AS IS, a tela de início ao cliente se dá por somente uma tela de direcionamento para login ou cadastro, caso não possua conta cadastrada. Em seguida, ambos os caminhos: Verificação de usuário ou Verificação dos dados de cadastro fazem parte de uma tarefa operacional do servidor. Após validado, usuários podem ver todos os pacotes disponíveis para compra.

- Gerenciar hotéis

Acerca do gerenciamento de hotéis, o modelo AS IS apresenta uma defasagem no quesito automático, pois, todo o seu atendimento é baseado em ligações entre cliente e atendente. Por se tratar de um modelo manual ultrapassado, podem haver filas de clientes ou quedas na ligação,  fazendo com que, pelo tempo demandado, procurem outras agências de viagens.


Após a ligação do cliente, é perguntado sobre sua situação cadastral. Caso não possua, será feito. Após esse processo, é perguntado sobre a escolha de hotel, juntamente com a data planejada. É feita uma checagem de disponibilidade e que, caso haja, será direcionado para o processo de reserva.


- Gerenciar voos

Novamente, a problemática se encontra na necessidade inicial do usuário já possuir uma conta para acessar os pacotes de vendas de voos.


Após o processo de cadastro/login, o usuário poderá escolher se deseja listar seus voos ou se deseja buscar outro. Após selecionada a data e o horário, caso seja validado, será encaminhado para a área de pagamento. Feito isso, o voo estará reservado.


# 3.2.  Modelagem dos processos aprimorados (TO-BE) 

  a. Gerenciar clientes

  
Neste processo, o intuito é o cadastramento de usuários e a confecção de possíveis clientes que irão comprar pacotes e/ou viagens. O objetivo se encontra na melhoria de acesso, fácil compreensão das etapas percorridas e menor tempo percorrido pelo usuário.

b. Gerenciar hotéis


Neste upgrade, vemos como melhoria da versão a automatização dos processos. Que traz maior liberdade, clareza e agilidade ao cliente. Para a agência há uma maior possibilidade de captação de clientes, para o usuário, melhor performance e agilidade de compra.


c. Gerenciar voos


Neste gerenciador, podemos ver a evolução do sistema de voos, anteriormente o usuário tinha informações de viagens apenas logado. Com a atualização o cliente pode ver tais informações, como preços, horários e destinos. Além do mais, foram adicionadas ações que facilitam a utilização do sistema como, cancelamento de voos, listagem de viagens e procura de voos. 



# 4. Projeto da arquitetura de dados da solução proposta
## I. DER - Entidade Voo

Na figura há a entidade relacionada aos Voos. Presente a entidade, estão os atributos: companAérea, Destino, DataVolta, DataEmbarque, Aeroporto de Partida e Aeroporto de Destino , também os balões com os conteúdos únicos PK CODVOO e FK CODCLI. Como relacionamento, um voo pode ser "consumido" por n clientes.

## II. DER - Entidade Cliente


Na figura encontra-se a entidade Cliente. Seus atributos são: dataNasc, Telefone, Cpf e Email e sua PK, CODCLI, além de outra FK CODEND fazendo ligação com o seu respectivo endereço. Ainda conectado a entidade, o mesmo pode conter acompanhantes, nesse caso, possuindo também atributos como CPF e dataNasc. Um cliente pode ter "n" acompanhantes.


## III. DER - Entidade Endereço

Na figura acima, há a entidade endereço. Ligado ao retângulo, estão os seus atributos (CEP, logradouro, estado, bairro, cidade e país) e também o balão com o conteúdo grifado (CODEND). Próximo ao balão (país) há um texto com o conteúdo 1,1.






## IV DER - Entidade Formas de Pagamento

Na figura, a entidade Formas de Pagamento. Estão nela presentes os seguintes atributos: sua PK CODPAG, valor, forma de pagamento e a PK do cliente (CODCLI). Relacionamento de 1:n tipos de pagamentos com a entidade Cliente.

## IV. DER - Entidade Hotel

Entidade hotéis: Atributos: Dataentrada, Plano e Data Saída, além da PK CODEND, CODHOTEL e FK CODCLI. Seu relacionamento se baseia de 1:n com Clientes.

# 4.2. Impactos da implementação em um banco de dados NoSQL
Como base de dados geral da aplicação, a escolha de uma alternativa NoSQL poderia, em resumo, trazer diversos riscos de consistência e integridade ao projeto. Isso ocorre devido à sua arquitetura organizacional, que, com foco no desempenho, utiliza clusters e particionamento de nós para realizar tarefas de forma assíncrona, nem sempre validando rigorosamente o conteúdo renderizado. Essa condição pode resultar, por exemplo, em dados inválidos e/ou incorretos relacionados aos usuários, hotéis, voos e até mesmo ao pagamento, como cobranças indevidas no pacote ou falha na autenticação do pagamento realizado, entre outros problemas.
Além disso, a estrutura distribuída dos dados, ao contrário do modelo relacional SQL, tende a ser mais flexível e menos adequada para parâmetros transacionais, tornando-se um custo adicional para sua implantação. Em busca de melhorar e modernizar a solução no que diz respeito à experiência do usuário (User Experience), a adoção de um modelo não relacional traria significativas melhorias e otimizações para a usabilidade da plataforma.
Essas melhorias se dão pelo conjunto de ferramentas e técnicas de englobamento a um único objeto, que, na prática, otimizam e facilitam processos de PUT e GET entre servidor e cliente-side. Por tal razão, ferramentas como sessão de usuário, preferências e até carrinhos de compras seriam mais eficientes, rápidas e mais tolerantes a falhas.

# 4.3. Modelo relacional


Dentro dos containers, são definidas tabelas individuais, cada uma com um propósito específico, como CLIENTE, HOTEL, VOO, ENDEREÇO e PAGAMENTO. Em cada tabela, as chaves primárias são identificadas com a notação "PK" seguida de um sublinhado, e as chaves estrangeiras são identificadas com a notação "FK" também seguida de um sublinhado. Além disso, as chaves estrangeiras estabelecem uma relação com o container que contém a chave primária correspondente."




# 4.4.  Consultas SQL
![image](https://github.com/ICEI-PUC-Minas-PMV-SI/pmv-si-2023-2-pe2-t2-projeto-sky/assets/127517961/0912336a-5e0c-4584-9130-f0e0a74223a9)


# 5. Relatórios analíticos
Quantidade de clientes por estado


Gráfico de pizza para a quantidade de clientes por UF 

Destinos de voos mais frequentes.
Gráfico em formato de pizza referente aos destinos de voos, utiliza o agrupador ListagemVoo > Destino.
III.Voos por Companhia Aérea.
 
Gráfico, referente a quantidade de voos por companhia aérea, utiliza os agrupadores VooSelecionado > Companhia Aérea.









# 5.1. Associação de comandos SQL com relatórios analíticos

![image](https://github.com/ICEI-PUC-Minas-PMV-SI/pmv-si-2023-2-pe2-t2-projeto-sky/assets/127517961/dd8177d9-a0d8-4ea6-8be8-bd7d22f36359)




# 6. Indicadores de desempenho

![image](https://github.com/ICEI-PUC-Minas-PMV-SI/pmv-si-2023-2-pe2-t2-projeto-sky/assets/127517961/e6607823-3065-44b3-94bd-c650222ebb77)
![image](https://github.com/ICEI-PUC-Minas-PMV-SI/pmv-si-2023-2-pe2-t2-projeto-sky/assets/127517961/374118a8-a77c-4700-9ff2-509a5f1c5530)



# 7. Conclusão

O trabalho apresentado foi capaz de prover com o estudo dos processos de agenciamento de viagem, a agilização de processos por meio da digitalização em um sistema onde o usuário tem acesso e provê o agendamento das viagens e hoteis cadastrados no banco de dados, sem precisar ligar, que era um processo manual que dependia do retorno de duas partes, já no sistema por ser mais direto, também provê dados dos diversos processos realizados pelos clientes, podendo extrair informação valiosa para tomadas de decisões para guiar o futuro do negócio, como o mercado de agenciamento de viagens é amplo e diverso, nosso trabalho é limitado a uma especialidade e é sugerido estudos que que contemplem uma maior diversidade, quantidade e um espaço temporal maior, e analisar como os processos desenhados sustentam-se em períodos de alta demanda, com um banco de dados mais robusto e maior.



# REFERÊNCIAS

MARQUES, V. Território brasileiro. Disponível em: <https://www.todamateria.com.br/territorio-brasileiro/>. Acesso em: 20 ago. 2023.

AMORIM, D.; CONTEÚDO, E. Turismo recupera perdas da pandemia, mas estrangeiro não voltou ao Brasil. Disponível em: <https://einvestidor.estadao.com.br/ultimas/turismo-brasil-2022-dados/>. Acesso em: 20 aug. 2023.

Disponível em: <https://www.mercadoeeventos.com.br/noticias/aviacao/media-mensal-de-voos-executivos-ate-outubro-de-2022-supera-niveis-pre-pandemia-no-brasil/#:~:text=A%20avia%C3%A7%C3%A3o%20brasileira%20registrou%20uma,de%20Avia%C3%A7%C3%A3o%20Geral%20(Abag).>. Acesso em: 20 aug. 2023.

Agência de viagens 123 Milhas suspende pacotes e emissão de passagens promocionais. Disponível em: <https://g1.globo.com/economia/noticia/2023/08/18/agencia-de-viagens-123-milhas-suspende-pacotes-e-emissao-de-passagens-promocionais.ghtml>. Acesso em: 20 aug. 2023.






