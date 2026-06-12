# Modelo Entidade-Associação

## ENTIDADES:
MEDICOS (nome, dataNascimento, horarioTrabalho, especialidade)

ENFERMEIROS(nome, dataNascimento, horarioTrabalho, formação, certificação, experiencias)

AUXILIAR(nome, dataNascimento, horarioTrabalho, funçoes)

TOSSADORES(nome, dataNascimento, horarioTrabalho, certificações, experiencias)

RECECIONISTAS(nome, data Nascimento, horaria Trabalho, idiomas, experiencia Atendimento, competências informáticas)

CLIENTE(id, nome, contacto, NIF)

ANIMAL(id, nome, data de nascimento, espécie, raça, caderno de vacinação)

CONSULTA(id, data hora, tipo de consulta, motivo )

VACINA( nome, validade, data de aplicação, próxima dose)

CIRURGIA (tipo de cirurgia, data, hora) 

SERVIÇO_ESTÉTICO (tipo de serviço, data, hora, preço)

## ASSOCIAÇÕES:

Possui (CLIENTE, ANIMAL) 1:N 	T:T

Faz (ANIMAL, CONSULTA) 1:N 	P:T

Marca (RECECIONISTA, CONSULTA) 1:N 	T:T

Realiza (MEDICO, CONSULTA) 1:N 	P:T

Auxilia (ENFERMEIRO, CONSULTA) 1:N 	P:P

Participa (AUXILIAR, CONSULTA) 1:N 		P:P

Recebe (ANIMAL, VACINA) 1:N 		P:T

Aplica (ENFERMEIRO, VACINA) 1:N 		P:T

Submete-se (ANIMAL, CIRURGIA) 1:N 	P:T

Recebe (ANIMAL, SERVIÇO_ESTETICO) 1:N 	  P:T

Executa (MEDICO, CIRURGIA) 1:N 		P:T

ResponsavelPelo (TOSADOR, SERVIÇO_ESTETICO) 1:N	T:T

### Regras de Negócio Adicionais (Restrições)
* não pode existir uma marcação de consulta sem um animal e um médico atribuito,
* A hora de qualquer consulta, serviço estético ou cirurgia deve obrigatoriamente estar dentro do horário de funcionamento da clícica. Um único médico não pode ter duas marcaçãoes no mesmo horário.
* Um animal só pode receber determinadas vacinas se a sua idade calculada for maior a 3 meses.

Nome	Descrição	Domínio	Por Omissão	Automático	Nulo
id_registo	Identificador do histórico	INT, PRIMARY KEY, AUTO_INCREMENT	-	Sim	Não
notas_clinicas	Observações do médico	TEXT	-	Não	Sim
id_animal	Animal intervencionado	INT, FOREIGN KEY → Animal(id_animal) NOT NULL	-	Não	Não
id_acao	Procedimento médico aplicado	INT, FOREIGN KEY → Acao_Medica(id_acao) NOT NULL	-	Não	Não
id_consulta	Consulta de origem do tratamento	INT, FOREIGN KEY → Consulta(id_consulta) NOT NULL	-	Não	Não
  

