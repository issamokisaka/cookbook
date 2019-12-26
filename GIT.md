```sh
$ git commit -am 'Adicionado campos Rais - Task 584807'
```

git checkout master
git pull
git rebase master desenvolvimento 
git checkout master
git merge desenvolvimento
git push

```sh
git checkout desenvolvimento
```

- Crie um novo branch chamado "funcionalidade_x" e selecione-o usando
  ```sh
  $ git checkout -b funcionalidade_x
  ```

- Retorne para o master usando
  ```sh
  $ git checkout master
  ```

- Remova o branch local da seguinte forma
  ```sh
  $ git branch -d funcionalidade_x
  ```

- um branch não está disponível a outros a menos que você envie o branch para seu repositório remoto
  ```sh
  $ git push origin funcionalidade_x
  ```

- remove branch local
  ```sh
  $ git branch -D nome_branch
  $ git branch -d nome_branch
  ```

- remove branch remota:
  ```sh
  $ git push origin --delete nome_branch
  ```
