Como é o Fluxo de trabalho com o GIT?
-
-
1 - Primeiro passo: (Configurar)
    -Instalar Git
    - COnfigurar nome de usuário e email
        -git config --global user.name "Seu nome"
        -git config --global user.email "seuemail@exemplo.com"
-
-
2- Segundo passo: (Preparar para começar)
    -Cliar ou clonar repositório
        Se existir repo remoto:
            -git clone <URL_DO_REPOSITORIO>
            -cd <NOME_DO_REPOSITORIO>
        Se não existir repo remoto:
            -mkdir <NOME_DO_PROJETO>
            -cd <NOME_DO_PROJETO>
            -git init
-
-
3- Terceiro passo: (Criando nova branch)
    -Crie nova branch (boas práticas)
        -git checkout -b <NOME-DA-BRANCH>
    -Alterne para uma branch existente
        -git checkout -b <NOME-DA-BRANCH>
-
-
4- Quarto passo: (Fazer as implementações)
    -Fazer as implementações do projeto
-
-
5- Quinto passo: (Enviando ao Stage)
    -Adiocionar ao "Stage"
        -Para adicionar um arquivo específico
            -git add <NOME-DO-ARQUIVO>
        -Para adicionar TODOS os arquivos modificados
            -git add . (LEMBRAR DO PONTO FINAL)
        -Crie um commit para registrar
            -git commit -m "Descrição clara e breve do que foi feito"
-
-
6- Sexto passo: (Enviar para o repo remoto)
    -Certifique que esta na branch correta
        -git branch
    -Enviar para o repo remoto
        -git push origin <NOME-DA-BRANCH>
-
-
7- Sétimo passo: (Sincronizar alterações)
    -Atualize a branch local com mudanças remotas:
        -git merge <NOME-DA-BRANCH>
    -Resolva conflitos se houver
        -Editar arquivos conflitantes
        -Depois de resolver conflitos, adiocione eles corrigidos
            -git add <ARQUIVO-RESOLVIDO>
            -git commit -m "Resolvendo Conflitos"
-
-
8- Oitavo passo: (Determinar o tipo de repo)
    -Se for um repo colaborativo
        -Abra um Pull Request (PR) ou Merge Request (MR) na plataforma do repo remoto (gitHUB, GitLab), para ser aprovado.
    -Se for um repo pessoal
        -Faca o merge na branch principal
            -git chechout main
            -git merge <NOME-DA-BRANCH>
            -git push origin main