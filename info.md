# Equipas
* 4 jogadores
* 1 guarda redes

# Estados
* A -> arriving (ainda não chegou)

* W -> wait (chegou e está à espera para formar uma equipa)

* F -> forming (quando entra forma uma equipa)

* s -> selected team 1

* S -> selected team 2

* p -> playing team 1

* P -> playing team 2

* R -> ready (começa o jogo)

* E -> end (acaba o jogo)

* L -> late (já chegou tarde)

# Funcionalidade

* Árbritro, jogadores, guarda-redes -> procesos indpendentes 

* sincronização dos processos: semáforos, shared memory

# Detalhes

* O árbritro só é selecionado depois de formadas as duas equipas

* O árbritro só começa e termina o jogo. Só começa quando chegarem os jogadores necessários.

* O tempo de chegada pode ser determinado por uma ditribuição de probabilidade uniforme.


# Mundança de estados

* A -> W (chegou mas está à espera de formar equipa)

* A -> F (chegou e já pode formar uma equipa)

* W -> s; F -> s (formaram a equipa)

* Este processo acontece para cada equipa

* A -> L (já chegou tarde (não tem espaço numa equipa), só muda quando ele chega ou quando o jogo acaba)

* s -> P (os jogadores estão prontos a jogar)

* s -> R (o árbrito começa o jogo)

* R -> E (o árbrito termina o jogo)

