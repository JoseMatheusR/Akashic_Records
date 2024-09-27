# Git e GitHub: Diferenças e Comandos
![Git symbol](https://github.com/user-attachments/assets/b228e316-cdf5-47e0-a179-ec834f8ae42c)
## **Git vs GitHub**

| Característica | Git | GitHub | 
| --- | --- | --- |
| **O que é** | Sistema de controle de versão distribuído. | Plataforma web para hospedagem de repositórios Git. |
| **Função** | Facilita a colaboração de várias pessoas no mesmo projeto, com controle de versões e criação de ramificações independentes. | Oferece hospedagem de repositórios Git e ferramentas adicionais para gerenciamento de projetos, controle de acesso, revisão de código e colaboração. |
| **Local de hospedagem** | O Git funciona localmente, mas pode ser configurado para repositórios remotos. | O GitHub hospeda repositórios na nuvem, acessíveis de qualquer lugar, desde que haja permissão. |

Além dessas características, o Git pode operar independentemente de qualquer plataforma online, como o próprio GitHub.

### **Principais Comandos do Git**

O Git possui uma ampla gama de comandos que podem ser executados via terminal, permitindo o uso completo de suas funcionalidades. Abaixo estão listados alguns comandos fundamentais e suas funções:

### Configuração Inicial

```bash
git config --global user.name "SeuNomeDeUsuario"
git config --global user.email "seuemail@example.com"
git config --global init.defaultBranch main
```

Estes comandos configuram o Git para se conectar ao GitHub, definindo seu nome de usuário e e-mail. O terceiro comando define a branch padrão como "main", que é uma convenção atual.

### Acesso à Documentação

```bash
git help ---
```

Este comando fornece a documentação detalhada sobre o comando especificado. Por exemplo:

```bash
git help add
```

Ele abrirá a documentação correspondente ao comando `git add` em sua máquina local, explicando como usá-lo.

### Configuração Inicial e Primeiro Push

Para iniciar um repositório Git, use o comando:

```bash
git init
```

Isso transforma o diretório local em um repositório Git. A partir daí, você pode utilizar os comandos a seguir.

No Git, os arquivos podem estar em três estados:

| Untracked | Staged | Committed |
| --- | --- | --- |
| Arquivos não rastreados ainda, suscetíveis a serem perdidos. | Arquivos preparados para o commit. | Arquivos prontos para serem enviados ao repositório remoto. |

Por padrão, arquivos começam como `Untracked`. Para adicionar ao controle do Git, use:

```bash
git add SeuArquivo.txt
```

Após isso, o arquivo estará `Staged`, pronto para receber o commit. Para realizar o commit:

```bash
git commit -m "Mensagem do commit"
```

O commit marca o ponto de controle, permitindo registrar informações relevantes sobre as mudanças feitas.

Para associar o repositório local ao repositório remoto, use:

```bash
git remote add origin https://github.com/SeuUsuario/SeuRepositorio.git
```

Finalmente, para enviar o repositório local ao GitHub:

```bash
git push -u origin main
```
## **Abaixo, segue uma série de comandos git úteis:**

## Visualizar hitórico de commits realizados

Para visualizar o histórico de commits:

```bash
git log
```

## Mesmo que o acima, mas com o output de uma única linha

Para uma visão simplificada do histórico:

```bash
git log --oneline
```

## Ver hitórico detalhado

Para ver o histórico com detalhes das modificações:

```bash
git log -p
```

## Commit automático de todas as alterações

Para fazer commit de todas as mudanças diretamente:

```bash
git commit -a -m "Mensagem do commit"
```

## Remover do working directory

Para remover o arquivo tanto do `staged` quanto do sistema de arquivos:

```bash
git rm MeuArquivo.txt
```

## Restaurar arquivos do estágio

Para remover um arquivo do estado `staged` mas manter suas modificações:

```bash
git restore --staged MeuArquivo.txt
```

## Renomear arquivos

Para renomear um arquivo:

```bash
git mv MeuArquivo.txt novoNome.html
```

## Alterar mensagem do último commit

Para modificar a mensagem do último commit:

```bash
git commit --amend -m "Nova mensagem do commit"
```

## Git reset

Existem três opções de reset no Git:

|Tipo|Descrição|
|-|-|
|**Soft**|Reverte o commit, mantendo as mudanças no estágio, prontas para novo commit.|
|**Mixed**|Semelhante ao soft, mas deixa as mudanças como unstaged. Necessário adicionar novamente.|
|**Hard**|Remove todas as alterações feitas após o commit escolhido. Não é possível restaurar.|

O reset *mixed* é o comportamento padrão. Exemplos:

```bash
git reset --soft <commit_id>
git reset --mixed <commit_id>
git reset --hard <commit_id>
```

## Git alias

Para criar atalhos de comandos Git, use:

```bash
git config alias.log1 "log --oneline"
git config --global alias.log1 "log --oneline"
```

## Branches

Recomenda-se trabalhar em branches ao invés de alterar diretamente a *main*. Crie sua própria branch e faça o merge depois.

### Criar uma nova branch:

```bash
git branch novaBranch
```

### Trocar para outra branch:

```bash
git switch novaBranch
# ou
git checkout novaBranch
```

### Fazer o merge de uma branch na *main*:

```bash
git merge novaBranch -m "Mensagem do merge"
```

### Deletar uma branch:

```bash
git branch -d novaBranch
```

---

## GitHub
| Issues | Releases |
| - | - |
|Issues no GitHub são relatórios usados para rastrear e discutir tópicos como bugs, melhorias, sugestões de funcionalidades ou perguntas relacionadas a um projeto de software. | Releases no GitHub são versões publicadas de um projeto, que incluem um conjunto específico de alterações e um ponto de controle para distribuição. Elas são baseadas em tags de commits, representando uma versão estável ou significativa do software.|
| Servem como um sistema de rastreamento de problemas e tarefas, ajudando na colaboração entre desenvolvedores e a comunidade do projeto. Elas podem ser usadas para gerenciar bugs, melhorias, e outras atividades do projeto. | As releases permitem que os usuários acessem versões específicas de um projeto de forma organizada, oferecendo pacotes de código, binários ou documentação associados a uma versão. |
| Qualquer pessoa com permissão pode criar uma issue. Depois de resolvido o problema ou implementada a sugestão, a issue pode ser encerrada (fechada). Elas também podem ser reabertas, se necessário. | Uma release é criada a partir de uma tag já existente ou uma nova tag que marca um commit no histórico. O desenvolvedor define a versão e disponibiliza um arquivo ou binário de lançamento.|

### Pull

Para atualizar o repositório local com as mudanças do remoto, utilize o comando:

```bash
git pull
```

Este comando combina *git fetch* e *git merge*.
