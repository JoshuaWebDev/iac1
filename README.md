# IaC 1

Script de criação de estrutura de usuários, diretórios e permissões criado durante o Bootcamp Cloud AWS realizado pela [Digital Innovation One](https://www.dio.me/)

## Instruções para criação do script

Dentro do script devem ser executadas as seguintes ações:

- crie os diretórios **/publico**, **/adm**, **/ven** e **/sec**.
- crie os grupos de usuários **GRP_ADM**, **GRP_VEN** e **GRP_SEC**.
- crie os usuários carlos, maria, joao, debora, sebastiana, roberto, josefina, amanda, rogerio, criando também o diretório do usuário, a senha e definindo bash como shell.
- em seguinda adicione os usuários carlos, maria e joao ao grupo GRP_ADM.
- em seguinda adicione os usuários debora, sebastiana e roberto ao grupo GRP_VEN.
- em seguinda adicione os usuários josefina, amanda e rogerio ao grupo GRP_SEC.

**Observação: Para cada ação dentro do script execute um echo antes informando o que esta ocorrendo**

## Principais comandos

### Comando para listar usuários
```
cat /etc/passwd
```

### Comando para criar usuários

```
useradd nome_do_usuario -m -s /bin/bash -p $(openssl passwd -crypt Senha123)
```

- O parâmetro -m informa que deve ser criado o diretório com o nome do usuário
- O parâmetro -s define o shell padrão do usuário
- O parâmetro -p define a senha
- a função $(openssl passwd -crypt ```senha```) cria uma senha criptografada

### Comando para excluir usuários

```
userdel -r nome_do_usuario
```

- O parâmetro -r informa que deve ser excluído o diretório do usuário e email (se houver)

### Comando para listar os grupos

```
cat /etc/group
```

### Comando para criar grupos

```
groupadd nome_do_grupo
```

### Comando para excluir grupos

```
groupdel nome_do_grupo
```

