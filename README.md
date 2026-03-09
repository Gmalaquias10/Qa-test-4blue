# Qa-test-4blue
Teste funcional de QA - Processo seletivo


# Sistema testado:
https://qa-play-sim.lovable.app/

## Durante os testes foram analisados:
- Validação de campos
- Página de cadastro
- Página de login
- Experiência do usuário
- Possíveis falhas básicas de segurança
 
 
     #                                  Relatório de Bugs – QA Test
                                     
 
 #           Bug 1 – Campo “Nome Completo” aceita números e caracteres especiais e campo Nome em branco

## Descrição:
Durante o cadastro de um novo usuário, o campo Nome Completo aceita números, caracteres especiais e campo em branco permitindo que o usuário crie uma conta com dados inválidos.

## Passos:
Acessar a página inicial de login do sistema.
Clicar na opção Criar conta.
Preencher o campo Nome Completo utilizando números.
Preencher os demais campos obrigatórios (Telefone, Email e Senha).
Clicar no botão Criar conta.

## Resultado atual:
O sistema aceita números no campo Nome Completo e a conta é criada com a mensagem “Conta criada com sucesso”.

## Resultado esperado:
O sistema deveria validar o campo Nome Completo, aceitando apenas letras e exibindo uma mensagem de erro ao inserir números.

**Severidade:** Médio
**Prioridade:** Média

 #            Bug 2 – Cadastro realizado com um ou mais campos em branco

## Descrição:
O sistema permite a criação de uma conta mesmo quando um ou mais campos obrigatórios estão em branco.
ex: o usuario consegue cadastrar preenchendo apenas telefone e email. somente nome e telefone. telefone e confirmar senha, senha e telefone, Nome completo e Senha.

## Passos:
Acessar a página inicial.
Clicar em Criar conta.
Deixar um ou mais campos em branco.
Clicar no botão Criar conta.

## Resultado atual:
A conta é criada exibindo a mensagem “Conta criada com sucesso”.

## Resultado esperado:
O sistema deveria impedir o cadastro e exibir uma mensagem informando que os campos obrigatórios precisam ser preenchidos.

**Severidade:** Crítico
**Prioridade:** Alta


#            Bug 3 – Cadastro realizado com campo “Nome Completo” em branco

## Descrição:
O sistema permite a criação de uma conta mesmo quando o campo Nome Completo não é preenchido.

## Passos:
Acessar a página inicial.
Clicar em Criar conta.
Deixar o campo Nome Completo em branco.
Preencher os demais campos obrigatórios.
Clicar em Criar conta.

## Resultado atual:
A conta é criada com sucesso.

## Resultado esperado:
O sistema deveria impedir o cadastro e exibir uma mensagem de erro informando que o campo Nome Completo é obrigatório.

**Severidade:** Alto
**Prioridade:** Alta

 #           Bug 4 – Cadastro realizado sem número de telefone

## Descrição:
O sistema permite a criação de uma conta mesmo com o campo Telefone em branco.

## Passos:
Acessar a página inicial.
Clicar em Criar conta.
Deixar o campo Telefone em branco.
Preencher os demais campos obrigatórios.
Clicar em Criar conta.

## Resultado atual:
A conta é criada com sucesso.

## Resultado esperado:
O sistema deveria exibir uma mensagem informando que o campo Telefone é obrigatório.

**Severidade:** Alto
**Prioridade:** Média

#            Bug 5 – Campo telefone aceita letras e caracteres especiais

## Descrição:
O campo Telefone aceita letras e caracteres especiais durante o cadastro de um usuário.

## Passos:
Acessar a página inicial.
Clicar em Criar conta.
Preencher o campo Telefone utilizando letras e caracteres especiais.
Preencher os demais campos obrigatórios.
Clicar em Criar conta.

## Resultado atual:
A conta é criada com sucesso.

## Resultado esperado:
O campo está aceitando letras e caracteres especiais, O sistema deveria aceitar somente números.

**Severidade:** Médio
**Prioridade:** Média



#             Bug 6 – Campo e-mail aceita formato inválido

## Descrição:
O sistema permite a criação de contas utilizando e-mails em formato inválido.

## Passos:
Acessar a página inicial.
Clicar em Criar conta.
Inserir no campo e-mail um valor sem o formato correto (ex: Teste123).
Preencher os demais campos.
Clicar em Criar conta.

## Resultado atual:
O sistema cria a conta mesmo com o e-mail inválido.

## Resultado esperado:
O sistema deveria validar o formato do e-mail e aceitar apenas endereços válidos (ex: usuario@email.com).

**Severidade:** Alto
**Prioridade:** Alta

            
#            Bug 7 – Cadastro realizado com campo senha em branco

## Descrição:
O sistema permite criar uma conta sem preencher o campo Senha.

## Passos:
Acessar a página inicial.
Clicar em Criar conta.
Deixar os campos Senha e Confirmar senha em branco.
Clicar em Criar conta.

## Resultado atual:
A conta é criada com sucesso.

## Resultado esperado:
O sistema deveria impedir o cadastro e exibir uma mensagem informando que o campo Senha é obrigatório.

**Severidade:** Crítico
**Prioridade:** Alta

           
 #           Bug 8 – Sistema permite cadastro com senhas diferentes

## Descrição:
O sistema permite criar uma conta mesmo quando os campos Senha e Confirmar senha possuem valores diferentes.

## Passos:
Acessar a página inicial.
Clicar em Criar conta.
Inserir uma senha no campo Senha.
Inserir uma senha diferente no campo Confirmar senha.
Clicar em Criar conta.

## Resultado atual:
A conta é criada com sucesso.

## Resultado esperado:
O sistema deveria validar se as senhas são iguais e exibir uma mensagem de erro caso sejam diferentes.

**Severidade:** Critico
**Prioridade:** Alta

#             Bug 9 – Cadastro realizado sem preencher campos obrigatórios (Email e Senha)

## Descrição:
O sistema permite criar uma conta preenchendo apenas os campos Nome Completo e Telefone, sem informar Email e Senha.

## Passos:
Acessar a página inicial.
Clicar em Criar conta.
Preencher apenas os campos Nome Completo e Telefone.
Deixar os campos Email, Senha e Confirmar Senha em branco.
Clicar no botão Criar conta.

## Resultado atual:
O sistema cria a conta e exibe a mensagem “Conta criada com sucesso”.

## Resultado esperado:
O sistema deveria impedir o cadastro e exibir uma mensagem informando que Email e Senha são campos obrigatórios.

**Severidade:** Crítico
**Prioridade:** Alta


#            Bug 10: Campo senha aceita senhas muito curtas

## Descrição:
O sistema permite criar conta ou fazer login com senha extremamente curta sem respeitar a regra exigida.

## Passos:
Acessar pagina inicial.
Acessar Criar Conta
Inserir e-mail válido
Inserir senha com menos caracteres
Criar conta

## Resultado atual
Conta é criada normalmente.

## Resultado esperado
Sistema deve exigir senha com regras mínimas: mínimo 8 caracteres e 1 caracter especial

**Severidade:** Crítico
**Prioridade:** Alta

        
                
#             Bug 11 Título: Criação de cadastros duplicados

## Descrição:
O sistema permite criar múltiplas contas com o mesmos dados.

## Passos:
Acessar pagina inicial
clicar no botão Criar Conta
preencher campo e-mail com ex:'teste@email.com'
preencher novamente com o mesmo e-mail
clicar botão criar conta

## Resultado atual:
Sistema permite criar cadastro novamente.

## Resultado esperado:
Sistema deveria bloquear e exibir mensagem: 'Este e-mail já está cadastrado'

**Severidade:** Critico
**Prioridade:** Alta

 #             Bug 12 Inconsistência visual nos campos do formulário

## Descrição:
 Os campos Nome Completo, Telefone, Senha e Confirmar Senha apresentam diferenças de alinhamento e tamanho em relação ao padrão visual da página.

## Passos:
Pagina inicial
Ao acessar criar Conta
Layout fora do padrão 
                
                
## Resultado atual:
Layout fora do padrão

## Resultado esperado:
Layout no padrão da pagina.
                
                             
**Severidade:** Médio
**Prioridade:** Médio
                
             
             
#             Bug 13 Título: Login efetuado com campos em branco

## Descrição: O login está sendo efetuado com um campo obrigatório em branco.

## Passos:
Acessar pagina inicial.
preenchendo apenas campo de login ou senha 
clicar no botão entrar


## Resultado atual:
Login realizado com sucesso

## Resultado esperado:
ao preencher apenas um dos campos de login, O sistema deveria apresentar mensagem de erro informando preenchimento obrigatório de todos os campos de login.

**Severidade:** Crítico
**Prioridade:** Alta

#             Bug 14 Título: Login com campo email e senha em branco

## Descrição:
 O login está sendo efetuado com campo email e senha em branco.

## Passos: 
Acessar página inicial.
deixar campos email e senha em branco.
clicar no botão entrar.

## Resultado atual:
Login realizado com sucesso
                
## Resultado esperado:
ao deixar campo email e senha em branco, mensagem de erro informando preenchimento obrigatório de todos os campos para login.                 

**Severidade:** Crítico
**Prioridade:** Alta                       
                
 #            Bug 15 – Credenciais de login sendo exibida no console do navegador

## Descrição:
  Durante o processo de criação de conta ou login, foi identificado que as informações do usuário, como email e senha, estão sendo exibidas no console do navegador.Isso seria um problema de segurança colocando os dados do usuario em risco.

## Passos: 
Acessar a página inicial do sistema.
Abrir as ferramentas de desenvolvedor do navegador pressionando F12.
Selecionar a aba Console.
Preencher os campos de cadastro ou login com email e senha.
Clicar no botão Criar conta ou Entrar.

## Resultado atual:
 Os dados inseridos pelo usuário, como email e senha, aparecem exibidos no console do navegador. 
  
## Resultado esperado:
 Informações sensíveis como email e senha não devem ser exibidas no console do navegador, a fim de evitar exposição de dados do usuário.
  
**Severidade:** Crítico
**Prioridade:** Alta 
  
  
  
  
 ##  Quais 2 bugs você corrigiria primeiro e por quê?
                
#  1- Credenciais exibidas no console (Bug- 15)
Esse bug possui severidade crítica, pois expõe informações sensíveis do usuário como email e senha no console do navegador.
Esse tipo de falha representa um risco de segurança, podendo permitir que terceiros tenham acesso a dados confidenciais.
Por esse motivo, esse problema deveria ser corrigido imediatamente.

#  2-Cadastro realizado com campos obrigatórios em branco (bug-2)
Esse bug permite a criação de contas sem dados essenciais, comprometendo a integridade do sistema.            
A ausência de validação dos campos obrigatórios pode gerar: contas inválidas, problemas no login e inconsistência no banco de dados.
                
                
#                Melhorias para tela

   - Exibir mensagens de erro específicas para cada campo obrigatório não preenchido. 
   - Adicionar na Página incial 'Esqueceu a senha'
   - colocar * Campos obrigatórios para os campos 'Nome' 'Email' 'Senha' e 'Confirmar Senha'.    
   - Adicionar validações imediatas enquanto o usuário digita, informando erros de preenchimento antes da criação do cadastro.
   - Adicionar um indicador visual mostrando se a senha criada é fraca, média ou forte, melhorando a segurança das contas.
               
