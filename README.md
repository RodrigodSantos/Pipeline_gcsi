# Execução do Projeto `Pipeline` com Jenkins
## Permissões Necessárias:
Acesse o diretório indicado abaixo
```
  cd /var/run
```
Conceda as permissões ao docker.sock
```
  sudo chmod 777 docker.sock
```
Adicione um novo usuário chamado `jenkins`
```
  useradd jenkins
```
Adicione o user `jenkins` ao grupo `docker`. Permitindo que o user `jenkins` execute comandos Docker sem precisar de `sudo`.
```
  sudo usermod -aG docker jenkins
```
 Use o seguinte comando para verificar se o usuário `jenkins` foi adicionado ao grupo `docker`.
```
  grep docker /etc/group
```
# Criando a Pipeline
Faça login no Jenkins e siga estes passos:

1. Clique em: `+ Nova Tarefa`
2. Insira o nome da sua pipeline
3. Selecione a opção `pipeline` e clique em `Tudo certo`
4. Adicione uma descrição (opcional)
5. Desça até a seção `Pipeline`
6. Em `definition`, onde está escrito `Pipeline script`, clique e escolha `Pipeline script from SCM`
7. Na seção `SCM`, clique e escolha `git`
8. Preencha o campo `Repository URL` com a URL do seu projeto, por exemplo: `https://github.com/RodrigodSantos/Pipeline_gcsi.git`
9. Em seguida, no campo `Branch Specifier`, insira o nome da sua branch, por exemplo: `*/main`
10. Finalize clicando em `Salvar`

# Executando a pipeline criada

* Após criar a pipeline, do lado direito, você verá a opção `Construir agora`. Clique nela e em seguida, clique em `Open Blue Ocean` para gerenciar a sua pipeline com uma interface mais intuitiva.

