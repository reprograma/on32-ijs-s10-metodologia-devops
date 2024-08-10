# Exercício de Casa 🏠 

## Explicação do exercício:

*Vamos usar a mesma aplicação que usamos em sala. [Clique aqui](/exercicios/para-sala/users-api-aula/README.md) para acessar a documentação*

Dividir o [Workflow já existente](/workflows/github-actions-demo.yml) em dois, um para *Pull Request* e um para *Push*. Ambos quando a ação for na Branch principal (main).

O de Pull request deve executar apenas as verificações (testes, lint e etc), o de push deve executar também o build e push para o docker hub.

Um exemplo que pode ser usado para nomear os workflows:

- github-actions-pr.yml
- github-actions-push.yml

*Na entrega, basta adicionar apenas os arquivos novos na pasta workflows, para correção.*

---

Terminou o exercício? Dá uma olhada nessa checklist e confere se tá tudo certinho, combinado?!

- [ ] Fiz o fork do [repositório](https://github.com/reprograma/on32-ijs-s10-metodologia-devops).
- [ ] Clonei o fork na minha máquina (`git clone url-do-meu-fork`).
- [ ] Criei minha branch (` git checkout -b nome-sobrenome `)
- [ ] Adicionei as mudanças. (`git add .` para adicionar todos os arquivos, ou `git add nome_do_arquivo` para adicionar um arquivo específico)
- [ ] Commitei a cada mudança significativa ou na finalização do exercício (`git commit -m "Mensagem do commit"`)
- [ ] Pushei os commits na minha branch (`git push origin nome-da-branch`)
- [ ] Criei um Pull Request seguindo as orientações abaixo

# Como criar meu Pull Request? 🤔

Olá, meninas! <br>
O checklist da atividade ta todo preenchido? Entao agora tá na hora de fazer nosso pull request para o repositório original. <br>
Você deverá navegar até o seu repositório onde você fez o fork e pressionar o botão “New pull request” no lado esquerdo da página. <br> <br>
![alt](https://assets.digitalocean.com/articles/eng_python/PullRequest/PRButton.png)

Você poderá modificar a branch na próxima tela. 

Depois de ter escolhido a branch main do repositório original no lado esquerdo, e a nova-branch do seu fork do lado direito, você deve ver uma tela assim:

![alt](https://assets.digitalocean.com/articles/eng_python/PullRequest/PullRequest.png)
<br> <br>
O GitHub vai lhe alertar de que é possível mesclar as duas branches porque não há código concorrente. Você deve adicionar um título, e um comentário descrevendo o seu PR. <br> <br>
DICAS: <br>
1. Você pode seguir esse modelo para o título do seu PR: 
``` 
Nome da Atividade - Seu nome. 
```
2. Você pode seguir esse modelo para a descrição do seu PR: 
``` 
O que?
Resolução dos exercícios de DevOps.

Como?
* Adicionei um arquivo para resolver a atividade utilizando o GitActions;
* Adicionei novo workflow para pull request 
* Outro ponto que você queira adicionar.
```
Feito isso, é so clicar em “Create pull request”. <br> <br>
Tcharaaaannn! Agora é só esperar a prof revisar seu PR 💜
