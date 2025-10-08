# modelagem-de-software
Projeto de Modelagem de Software do 6º Semestre (FEI)

## Diagrama de Casos de Uso:
![Diagrama de Casos de Uso](./resources/img/diagrama.png)
|Identificação|UC_votacao|
|---|---|
|Função|Eleitor vota na urna eletrônica|
|Atores|Eleitor, Urna Eletrônica|
|Prioridade|Essencial|
|Pré-condição|Liberação da Urna para Voto do Eleitor|
|Pós-condição|Voto do eleitor é computado|
|Fluxo Principal|1. Eleitor digita número desejado na urna<br>2. <b>a.</b> Se número for de um candidato válido, urna computa número e retorna informações do candidato<br>2. <b>b.</b> Se número for inválido, urna computa voto nulo<br>2. <b>c.</b> Em caso de voto em branco, urna computa voto em branco<br>3. Eleitor confirma voto<br>4. Urna retorna confirmação<br>5. Loop para seleção de candidato de outro(s) cargo(s)<br>|

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
|Fluxo Principal|1. Administrador requere relatório para o sistema<br>2.Sistema gera relatório com os resultados apresentados em forma de tabelas(FS-002), separados por UEv. Também são contabilizados os votos brancos e nulos, assim como os eleitores ausentes.|
|Fluxo Secundário (FS-001)|1. Abnormalidade é detectada em algum fator da votação<br>2. Relatório é gerado com erros relatados|
|Fluxo Secundário (FS-002)|1. Administrador escolhe apresentar relatório em gráficos<br>2. Relatório é gerado com gráficos, separados por UEv. Também são contabilizados os votos brancos e nulos, assim como os eleitores ausentes.|


|Identificação|UC_cadastro|
|---|---|
|Função|Administrador cadastra candidato no sistema de votação|
|Atores|Administrador|
|Prioridade|Essencial|
|Pré-condição|Nenhuma|
|Pós-condição|Candidato cadastrado no sistema|
|Fluxo Principal|1. Administrador coloca cargo, nome, apelido, número e fotografia do candidato no sistema, a depender da região(FS-001)<br>2. Candidato é cadastrado com sucesso.|
|Fluxo Secundário (FS-001)|1. Sistema retorna situação fora do normal do candidato<br>2. Administrador não cadastra candidato|

## Diagrama de Classes
![Diagrama de Classes](./resources/img/DiagramaClasses.png)

## Diagramas de Sequência
### UC_votacao
![Diagrama de Sequencia1](./resources/img/diagrama_sequencia_votacao.png)
### UC_liberacao
![Diagrama de Sequencia1](./resources/img/diagrama_sequencia_liberacao.png)
### UC_situacao
![Diagrama de Sequencia1](./resources/img/diagrama_sequencia_situacao.png)
### UC_relatorio
![Diagrama de CSequencia4](./resources/img/diagrama_sequencia_relatorio.png)
### UC_cadastro
![Diagrama de CSequencia4](./resources/img/diagrama_sequencia_cadastro.png)

## Diagramas de Estados
### UEv
![Diagrama de Estados1](./resources/img/DiagramaDeEstadosUrna.png)
### Eleitor
![Diagrama de Estados2](./resources/img/DiagramaEstEleitor.png)
### Relatório
![Diagrama de Estados3](./resources/img/DiagramaEstRelatorio.png)

## Diagrama de Atividade
### UC_votacao
![Diagrama de Atividade](./resources/img/AtividadeSitua.png)
### UC_liberacao
![Diagrama de Atividade](./resources/img/AtividadeSitua.png)
### UC_situacao
![Diagrama de Atividade](./resources/img/AtividadeSitua.png)
### UC_relatorio
![Diagrama de Atividade](./resources/img/AtividadeSitua.png)
### UC_cadastro
![Diagrama de Atividade](./resources/img/AtividadeSitua.png)
