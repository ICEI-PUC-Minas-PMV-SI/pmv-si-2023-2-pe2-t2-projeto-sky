# Artefatos relativos à modelagem de dados do projeto

## Modelo Relacional base da Aplicação

![image](https://github.com/ICEI-PUC-Minas-PMV-SI/pmv-si-2023-2-pe2-t2-projeto-sky/assets/127517961/ee2b946d-a250-41bc-a7af-48d003694684)

------
### I. DER - Entidade VOOs

![image](https://github.com/ICEI-PUC-Minas-PMV-SI/pmv-si-2023-2-pe2-t2-projeto-sky/assets/127517961/ba67df05-0ba0-43e9-b75c-bf369ade2246)

- Na figura há a entidade relacionada aos Voos. Presente a entidade, estão os atributos: <i>companAérea, Destino, DataVolta, DataEmbarque,  Aeroporto de Partida e Aeroporto de Destino </i>, também os balões com os conteúdos únicos PK <i>CODVOO e FK CODCLI</i>. Como relacionamento, um voo pode ser "consumido" por n clientes.

------

### II. DER - Entidade Cliente

![image](https://github.com/ICEI-PUC-Minas-PMV-SI/pmv-si-2023-2-pe2-t2-projeto-sky/assets/127517961/764ae807-707c-4f05-ab10-2e5ff0bf25b9)

 - Na figura encontra-se a entidade Cliente. Seus atributos são: <i> dataNasc, Telefone, Cpf e Email</i> e sua PK,<i> CODCLI</i>, além de outra FK <i>CODEND</i> fazendo ligação com o seu respectivo endereço. Ainda conectado a entidade, o mesmo pode conter acompanhantes, nesse caso, possuindo também atributos como CPF e dataNasc. Um cliente pode ter "n" acompanhantes.

------

### III. DER - Entidade Endereço do Cliente

![image](https://github.com/ICEI-PUC-Minas-PMV-SI/pmv-si-2023-2-pe2-t2-projeto-sky/assets/127517961/c2a75adb-3757-4899-8f1a-f6ec9697fa4b)

- Na figura acima, há a entidade Endereço. Contém os atributos: <i>CEP, logradouro, estado, bairro, cidade e país</i> e também a PK do cliente, <i>CODEND</i>. Sua relação se baseia de 1:1 entre a entidade Cliente.

------

### IV DER - Entidade Formas de Pagamento

![image](https://github.com/ICEI-PUC-Minas-PMV-SI/pmv-si-2023-2-pe2-t2-projeto-sky/assets/127517961/3c282925-79d7-4f99-96e2-e50c9a503f58)

- Na figura, a entidade Formas de Pagamento. Estão nela presentes os seguintes atributos: sua PK <i>CODPAG, valor, forma de pagamento e a PK do cliente (CODCLI)</i>. Relacionamento de 1:n tipos de pagamentos com a entidade Cliente.

------

### V DER - Entidade Hotéis

![image](https://github.com/ICEI-PUC-Minas-PMV-SI/pmv-si-2023-2-pe2-t2-projeto-sky/assets/127517961/9dd44927-9c9c-4f4c-ad5b-6ac6c873721f)

- Entidade hotéis: Atributos: <i>Dataentrada, Plano e Data Saída</i>, além da PK <i>CODEND, CODHOTEL </i> e FK <i>CODCLI</i>. Seu relacionamento se baseia de 1:n com Clientes.

