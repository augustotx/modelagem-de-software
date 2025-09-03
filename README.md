# modelagem-de-software
Projeto de Modelagem de Software do 6º Semestre (FEI)
## Casos de Uso:
|Identificação|UC_votacao|
|---|---|
|Função|Eleitor vota na urna eletrônica|
|Atores|Eleitor, Urna Eletrônica|
|Prioridade|Essencial|
|Pré-condição|Liberação da Urna para Voto do Eleitor|
|Pós-condição|Voto do eleitor é computado|
|Fluxo Principal|1. Eleitor digita número do candidato (ou branco/nulo) desejado na urna<br>2. Urna computa número e retorna informações do candidato (FS-001)<br>3. Eleitor confirma voto<br>4. Urna retorna confirmação<br>5. Loop para seleção de candidato de outro(s) cargo(s)<br>|
|Fluxo Secundário (FS-001)|1. Urna computa número e retorna "candidato inválido"<br>2. Urna retorna para página de seleção de candidato<br>3. Candidato digita outro número<br>4. Loop até que um candidato válido (ou branco/nulo) seja escolhido<br>|

|Identificação|UC_liberacao|
|---|---|
|Função|Mesário Valida Eleitor para Votar|
|Atores|Mesário|
|Prioridade|Essencial|
|Pré-condição|Normalidade do título do eleitor|
|Pós-condição|Eleitor é liberado para votar|
|Fluxo Principal|1. Mesário reseta urna eletrônica para iniciar outra votação|

|Identificação|UC_situacao|
|---|---|
|Função|Mesário verifica a situação do eleitor|
|Atores|Mesário|
|Prioridade|Essencial|
|Pré-condição|Eleitor compareceu na eleição|
|Pós-condição|Mesário está pronto para liberar a urna eletrônica|
|Fluxo Principal|1. Mesário verifica no sistema a situação do título do eleitor (FS-001)<br>2. Mesário sobe ao sistema que eleitor compareceu|
|Fluxo Secundário (FS-001)|1. Situação do título do eleitor não está normal<br>2. Mesário informa a situação e não libera a urna|

|Identificação|UC_relatorio|
|---|---|
|Função|Administrador gera relatório de votação|
|Atores|Administrador|
|Prioridade|Essencial|
|Pré-condição|Votação ocorreu|
|Pós-condição|Relatório de votação é gerado|
|Fluxo Principal|1. Administrador requere relatório para o sistema<br>2. Sistema gera relatório (FS-001)|
|Fluxo Secundário (FS-001)|1. Abnormalidade é detectada em algum fator da votação<br>2. Relatório é gerado com erros relatados|



|Identificação|UC_cadastro|
|---|---|
|Função|Administrador cadastra candidato no sistema de votação|
|Atores|Administrador|
|Prioridade|Essencial|
|Pré-condição|Nenhuma|
|Pós-condição|Candidato cadastrado no sistema|
|Fluxo Principal|1. Administrador coloca informações do candidato no sistema (FS-001)<br>2. Candidato é cadastrado com sucesso.|
|Fluxo Secundário (FS-001)|1. Sistema retorna situação fora do normal do candidato<br>2. Administrador não cadastra candidato|
