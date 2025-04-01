# PROJETO-4-MODELAGEM-DE-UM-PEQUENO-SISTEMA-COM-UML-E-BPMN


ALUNA(O): Antonia Soraia Uchôa Verçosa 
2ds


-> PROJETO DE MATRIZ UML E PBMN
meu modelo é criado para o usuario reservar um ou mais livros


# Modelo UML
--------------------           
  USÚARIO                       
--------------------          
- nome: Strig                               
- email: String                                    
- id: int                                                
          
- se cadastrar ()               
- cacelar cadastro ()           
                                                                  
----------------------
RESERVA
----------------------
- nome do livro: String
- data: date
- id: int

-comfirmar reserva()
-cancelar reserva()

-------------------
SALA
-------------------
- id: int
- sala 1 ()
- sala 2 ()
- sala 3 ()

- enviar ()

  
# Modelo BPMN
A[Início] -> B[cadastro do usuario] -> C[verificar reserva] -> D[verificar estoque] - {estoque disponivel?} -> E[sala] -> F[enviar]
B -> [tudo ok]- prosseguir -> [erro]- informar usuario
C -> [tudo ok]- prosseguir -> [não]- informar usuario 
D -> [estoque disponivel]- realizar reserva do livro ->[estoque indisponivel]- informar usuario
E -> [sala disponivel] - tudo ok -> [sala indisponvel] - informar usuario
F -> [enviado] - fim 


