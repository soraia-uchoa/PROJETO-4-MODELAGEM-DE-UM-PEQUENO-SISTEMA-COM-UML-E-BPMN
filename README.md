# PROJETO-4-MODELAGEM-DE-UM-PEQUENO-SISTEMA-COM-UML-E-BPMN


ALUNA(O): Antonia Soraia Uchôa Verçosa 


-> PROJETO DE MATRIZ UML E PBMN
meu modelo é criado para o usuario reservar um ou mais livros


# Modelo UML
--------------------            -----------------------          ---------------------
  USÚARIO                         RESERVA                           SALA
--------------------            -----------------------          ---------------------
- nome: Strig                   - nome do livro: String           - id: int          
- email: String                 - data: date                      - sala 1 ()
- id: int                       - id: int                         - sala 2 ()
---------------------           ----------------------            - sala 3 ()
- se cadastrar ()               - Confirmar reserva()            ---------------------
- cacelar cadastro ()           - Cacelar reserva()               enviar()
                                                                  cancelar()
---------------------           ----------------------          ----------------------



# Modelo BPMN
A[Início] -> B[cadastro do usuario] -> C[verificar reserva] -> D[verificar estoque] - {estoque disponivel?} -> E[sala] -> F[enviar]
B -> [tudo ok]- prosseguir -> [erro]- informar usuario
C -> [tudo ok]- prosseguir -> [não]- informar usuario 
D -> [estoque disponivel]- realizar reserva do livro ->[estoque indisponivel]- informar usuario
E -> [sala disponivel] - tudo ok -> [sala indisponvel] - informar usuario
F -> [enviado] - fim 


