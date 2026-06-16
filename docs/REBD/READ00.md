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
|Id|	Identificador do Enfermeiro |	INT, PK, AUTO_INCREMENT	  |    -	|Sim |	não|
|Nome	|Nome do Enfermeiro 	|VARCHAR(100)NN	  |    -|Não |	Não| 
|DataNascimento	|DataNascimento do Enfermeiro	|VARCHAR(100)	    |  -	|NÃO	|Não|
|HorárioTrabalho	|Horário do enfermeiro |	VARCHAR (50) NN	 |     9h/13h-14h/19h	|Não	|Não |
|Formação |	formação do Enfermeiro	|VARCHAR(150)	    |  -	|Não|	Sim| 
|Certificação	|Certificação do Enfermeiro	|VARCHAR(150) |    -|	Não |	Sim |
|Experiência |	Experiência do Enfermeiro 	|Text	  |    -	|Não |	Sim |

AUXILIAR 

| Nome |	Descriçao|	Dominio	| Por Omissão	| Automatico |	Nulo |
|------|-----------|----------|-------------|------------|-------|
|Id|	Identificador do Auxiliar| 	INT, PK, AUTO_INCREMENT	|      -|	Sim |	não|
|Nome|	Nome do Auxiliar 	|VARCHAR(100)	  |    -	|Não| 	Não |
|DataNascimento	|DataNascimento do Auxiliar	|DATE 	  |    -	|NÃO	|Não|
|HorárioTrabalho	|Horário do Auxiliar	|VARCHAR(50)|	9h/13h;14h/19h|	Não|	Sim|
|Funções |	Funções do Auxiliar|	VARCHAR(150)	   |   -	|Não|	Sim |

RECECIONISTA

| Nome |	Descriçao|	Dominio	| Por Omissão	| Automatico |	Nulo |
|------|-----------|----------|-------------|------------|-------|
|Id|	identificador da Rececionista|	INT, PK, AUTO_INCREMENT	|      -	|Sim| 	não|
|Nome	|Nome da Rececionista	|VARCHAR(100)	|      -|	Não |	Não |
|DataNascimento|	dataNascimento da Rececionista|	DATE 	|      -	|NÃO	|Não|
|HorárioTrabalho	|Horário da rececionista |	VARCHAR(50)	|9h/13h 14h/19h|	Não	|Sim|
|Idiomas| 	VARCHAR(200)	|VARCHAR(100)	 |     -	|Não |	Sim |
|ExperiênciaAtendimento |	ExperiênciaAtendimento da rececionista |	Text	 |     -	|Não 	Sim |
|Competências Informática| 	Competências Informática da Rececionista |	Text	|      -	|Não|	Não |

TOSSADORES

| Nome |	Descriçao|	Dominio	| Por Omissão	| Automatico |	Nulo |
|------|-----------|----------|-------------|------------|-------|
|Id	|Identificador do Tosader-Groomer|	INT, PK, AUTO_INCREMENT	  |    -	|Sim |	não|
|Nome|	Nome do Tosader-Groomer|	VARCHAR(100)	   |   -|	Não |	Não |
|DataNascimento	|DataNascimento do Tosader-Groomer	|DATE 	  |    -	|NÃO|	Não|
|HorárioTrabalho  |	Horário do Tosader-Groomer	|VARCHAR(50)	  |9h/13h 14h/19h	|Não	|Não |
|Certificações |	Certificações do Tosader-Groomer	|VARCHAR(150)	    |  -	|Não	|Sim  |
|Experiências |	Experiências do Tosader-Groomer |	Text	|      -|	Não |	Sim |

Consulta

| Nome |	Descriçao|	Dominio	| Por Omissão	| Automatico |	Nulo |
|------|-----------|----------|-------------|------------|-------|
|id|	Identificador da consulta|	INT, PK, AUTO_INCREMENT	|-|	sim	|não|
|data |	Dia do agendamento	|VARCHAR(100) NN|	Data atual	|Não| 	não|
|tipo	|Rotina/Emergência	|VARCHAR(100) NN	|	não	|não|
|motivo	|Motivo da consulta|	VARCHAR(100)|	-|	não	|não|

Vacina
| Nome |	Descriçao|	Dominio	| Por Omissão	| Automatico |	Nulo |
|------|-----------|----------|-------------|------------|-------|
|Id 	|Identificador único da vacina	|INT, PK, AUTO_INCREMENT	|_	|sim|	não|
|nome	|Nome da vacina aplicada 	|VARCHAR(100) NN|	-|não|	não|
|validade|	Validade da vacina|	Varchar(100) NN	|-|	não|	não|
|Data de aplicação |	Data de aplicação da vacina |	DATE|	-|	não|	não|
|Próxima dose 	|Data da proxima dose da vacina	|DATE|	null	|não	|sim|

Cirurgia 
| Nome |	Descriçao|	Dominio	| Por Omissão	| Automatico |	Nulo |
|------|-----------|----------|-------------|------------|-------|
||Id 	Identificador único da cirurgia |	INT, PK, AUTO_INCREMENT|	-|	sim|	não|
|Tipo 	|Tipo de cirurgia a ser realizado |	VARCHAR(100) NN	|-|não	|não|
|Data |	Data da realização cirurgia 	|DATE| NOT NULL	|-|	não|	não|
|hora 	|Hora da realização cirurgia |	TIME NOT NULL |	-|não|	não|

Serviço estético 
| Nome |	Descriçao|	Dominio	| Por Omissão	| Automatico |	Nulo |
|------|-----------|----------|-------------|------------|-------|
|Id 	|Identificador único do serviço estético |	INT, PK, AUTO_INCREMENT|	-|sim|	não|
|Tipo de serviço |	Tipo de serviço a ser realizado |	VARCHAR(100) NN|	-|	não|	não|
|data|	Data da realização do serviço estético| 	DATE NOT NULL|-|	não|	não|
|hora |	hora da realização do serviço estético	|TIME NOT NULL	|-|	sim|	não|
|preço |	Preço aplicado ao serviço estético realizado |	PRICE NOT NULL|	_	|sim|	não|

























