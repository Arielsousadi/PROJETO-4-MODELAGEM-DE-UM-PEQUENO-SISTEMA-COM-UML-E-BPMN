 PROJETO-4-MODELAGEM-DE-UM-PEQUENO-SISTEMA-COM-UML-E-BPMN

equipe: ARIEL & RODOLFO

"BPMN"

[INÍCIO] -> [usuário acessa o sistema] -> [seleciona sala e horário] -> [verifica disponibilidade] -> {sala disponível?}
    -> [SIM] -> [reserva confirmada] -> [FIM]
    -> [NÃO] -> [exibe salas alternativas] -> [FIM]

"UML"

/=======================/
	CLIENTE
/=======================/
	- nome: String
	- email: String
/=======================/
	# agendarSala()
/=======================/

Cliente 1 === 0 (false)
Cliente 1 === 1 (true) --------------|
				     |
/=======================/	     |
	SALA			    <|
/=======================/
	# fazerReserva
/=======================/
reserva [+ local()
	+ data()
	+ horário()]
/=======================/
	reserva 1 === 0 (false)
	reserva 1 === 1 (true) -------------|
					    |
			 Espaço agendado.  <|

