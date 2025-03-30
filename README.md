# PROJETO-4-MODELAGEM-DE-UM-PEQUENO-SISTEMA-COM-UML-E-BPMN

equipe: ARIEL & DEUS

"BPMN"

[INÍCIO] -> [usuário acessa o sistema] -> [seleciona sala e horário] -> [verifica disponibilidade] -> {sala disponível?}
    -> [SIM] -> [reserva confirmada] -> [FIM]
    -> [NÃO] -> [exibe salas alternativas] -> [FIM]

    
"UML"

class Usuario {

  - nome: String
    
  - email: String
    
  + fazer reserva()
    
}

class Sala {
  - numero: int
    
  - capacidade: int
    
  + verificar disponibilidade()
    
}

class Reserva {

  - id: int
    
  - data: Date
  
  - horario: String
    
  + confirmar reserva()
    
}

Usuario --> Reserva : "1 faz 0..*"

Reserva --> Sala : "1 reserva 1"

