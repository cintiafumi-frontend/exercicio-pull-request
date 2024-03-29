# Git e Github

### Instruções
##### Configurações básicas iniciais
* Ter o git instalado na sua máquina
	
  ```
  git --version
  ```

* Entre no gitbash
* Verifique se seu usuário está configurado na sua máquina. (Deve aparecer seu ***user.name*** e ***user.email***)
	
  ```
  git config --list
  ```

	* Caso não esteja configurado, fazer a configuração de ***user.name*** e ***user.email***
		
    ```
    git config --global user.name "Seu Nome"
    ```

		
    ```
    git config --global user.email "seu@email.com"
    ```

---

##### Clonar o repositório do exercício na sua máquina
* Abra o gitbash
* Verifique se está no diretório em que deseja clonar o repositório
	
  ```
  pwd
  ```

* Clonar o repositório desta aula
	
  ```
  git clone https://github.com/reprograma/On3-git-e-github.git
  ```

* Entrar nesse repositório local

	```
  cd On3-git-e-github
  ```

* Criar uma branch nova com seu nome.
	
  ```
  git checkout -b suaBranch
  ```

* Entrar no VSCode

	```
  code .
  ```

* Alterar a imagem e o link para seu github na `<div>` que contiver seu nome.
	* Use o link do seu github para colocar no ***href*** na tag `<a>`. (Ex: https://github.com/reprograma)
	* Use o link da imagem do seu avatar no github para colocar no ***src*** da tag `<img>`. Clique com o botão direito sobre a imagem do seu perfil no github e copie o endereço da imagem. (Ex: https://avatars0.githubusercontent.com/u/27314899?s=200&v=4)
  * Adicione seu nome no ***alt*** da tag `<img>`

  Exemplo:

    **Antes:**

    ```
    <div class="container__aluna">
        <a href="#" target="_blank">
            <img class="container__aluna-img" src="https://via.placeholder.com/500" alt="Cintia Fumi">
        </a>
        <p>Cintia Fumi</p>
    </div>
    ```
    
    **Depois:**
    
    ```
    <div class="container__aluna">
        <a href="https://github.com/cintiafumi" target="_blank">
            <img class="container__aluna-img" src="https://avatars0.githubusercontent.com/u/34029172?s=460&v=4" alt="Cintia Fumi">
        </a>
        <p>Cintia Fumi</p>
    </div>
    ```

* Conferir essa alteração no navegador (Chrome).
	* *Comportamento esperado: ao clicar na sua foto, o link do seu github irá se abrir numa aba nova*
* Voltando para o gitbash
* Verificar o status
	
  ```
  git status
  ```

* Adicionar as alterações para área de preparação
	
  ```
  git add index.html
  ```

* Verificar o status novamente
	
  ```
  git status
  ```

* Adicionar mensagem de ***commit***
	
  ```
  git commit -m "adicionando foto e link de Cíntia para Githbub"
  ```

* Subir as alterações para o seu repositório remoto
	
  ```
  git push origin suaBranch
  ```

* Verificar se as alterações foram atualizadas na sua branch lá no github (https://github.com/reprograma/On3-git-e-github)
* Ir para a aba ***Pull requests***
* Criar novo ***New pull request*** pelo github da reprograma verificando se está fazendo a solicitação da suaBranch para a master
	*base: **master**    **<=**    compare: **suaBranch***
---
##### Após todos ***pull request*** serem aceitos, caso queria atualizar localmente seu repositório:
* Voltar para a branch master
	
  ```
  git checkout master
  ```

* Atualizar o repositório local
	
  ```
  git pull origin master
  ```

* Verificar no navegador (Chrome) se todas as atualizações vieram

---
##### Deletar sua branch após seu ***pull request*** ser aceito
* Estar na branch **master** para remover a branch **suaBranch**
	
  ```
  git checkout master
  ```

	
  ```
  git branch -d suaBranch
  ```



---
##### Subir esse repositório no seu github
* Criar um novo respositório no seu github
* Copiar o link desse novo repositório e adicionar o remote ***meuRepo*** como endereço do seu repositório
    
    ```
    git remote add meuRepo https://github.com/<seuLogin>/<seuNovoRepositorio>.git
    ```

	obs: Nesse link acima, substituir `<seuLogin>` e `<seuNovoRepositorio>` com informações do seu login e seu repositório
* Commitar o que está local para seu repo novo

  ```
  git commit -m "Exercício para casa" --allow-empty
  ```

* Subir o repo local para o seu repo
	
  ```
  git push origin master
  ```

