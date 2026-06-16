Esquema Relacional

Tabelas

Medico

Regista os doutores da clinica, incluindo os seus dados de contacto.

| Nome |	Descriçao|	Dominio	| Por Omissão	| Automatico |	Nulo |
|------|-----------|----------|-------------|------------|-------|
| Id 	 |Identificador único do médico	| INT, PK, AUTO_INCREMENT|	_	|sim |não|
|nome|	Nome do médico|	VARCHAR(100) NN|	_	|não|	não|
|dataNascimento|	Data de nascimento do medico	|VARCHAR(100)|	_	|não	|não|
|horarioTrabalho	|Horário de trabalho do medico|	VARCHAR(100) NN	|9h/19h,1h de pausa, das 13h as 14h	|não	|não|
|especialidade	|Especialidade do medico 	|VARCHAR(100)	|null	|não	|sim|


Cliente

Regista os clientes da clinica.

| Nome |	Descriçao|	Dominio	| Por Omissão	| Automatico |	Nulo |
|------|-----------|----------|-------------|------------|-------|
|id	|Identificador do cliente	|INT, PK, AUTO_INCREMENT	|-	|sim	|não|
|nome|	Nome do dono|	VARCHAR(100) NN|	-|	não|	não|
|nif	|N.º Contribuinte (UK)|	VARCHAR(9) UK	|-|	não	|não|
|contacto	|Contacto do cliente	|VARCHAR(100)NN	|-	|não	|sim|

Animal

Regista os animais que frequentam a clinica.

| Nome |	Descriçao|	Dominio	| Por Omissão	| Automatico |	Nulo |
|------|-----------|----------|-------------|------------|-------|
|id|	Identificador do animal	|INT, PK AUTO_INCREMENT	|-|	sim	|não|
|nome|	Nome do animal|	VARCHAR(100) NN|	-|	não|	não|
|data de nascimento|	data de nascimento do animal	|VARCHAR(100) (UK)|	-|	Não |	sim|
|espécie	|Espécie do animal consultado|VARCHAR(100) NN|	-	|não|	não|
|Raça |	Raça do animal|	VARCHAR(100) NN	|-|	não	|sim|
|Caderno de vacinação|	Estado do registo de vacinas do animal|	VARCHAR(100) NN	|-|	não	|não|

Enfermeiro

| Nome |	Descriçao|	Dominio	| Por Omissão	| Automatico |	Nulo |
|------|-----------|----------|-------------|------------|-------|






