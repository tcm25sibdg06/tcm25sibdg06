Esquema Relacional

Tabelas

Doutor

Regista os doutores da clinica, incluindo os seus dados de contacto.

| Nome |	Descriçao|	Dominio	| Por Omissão	| Automatico |	Nulo |
|------|-----------|----------|-------------|------------|-------|
| Id 	 |Identificador único do médico	| INT, PK, AUTO_INCREMENT|	_	|sim |não|
|nome|	Nome do médico|	VARCHAR(100) NN|	_	|não|	não|
|dataNascimento|	Data de nascimento do medico	|VARCHAR(100)|	_	|não	|não|
|horarioTrabalho	|Horário de trabalho do medico|	VARCHAR(100) NN	|9h/19h,1h de pausa, das 13h as 14h	|não	|não|
|especialidade	|Especialidade do medico 	|VARCHAR(100)	|null	|não	|sim|
