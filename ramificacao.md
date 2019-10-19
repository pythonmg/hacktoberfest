
# Contribuindo de maneira profissional através do uso de ramificações

Agora que você já sabe como realizar uma contribuição de maneira simples, vamos aprender como fazer uma contribuição da maneira que os projetos open source geralmente recomendam.

Não vamos repetir tudo novamente, mas apenas acrescentar algumas tarefas intermediárias no processo.

Suponha que você fosse seguir o passo a passo novamente:

:package: [Nossa primeira contribuição.](contribuindo.md)

Você vai fazer o **fork** normalmente.

Você também vai **clonar** o repositório da mesma maneira.

Aqui é que as coisas se modificam um pouco.

Quando você trabalha em um projeto colaborativo, você e outros desenvolvedores que estão contribuindo no repositório terão ideias diferentes para novas funcionalidades ou correções ao mesmo tempo. Algumas dessas novas funcionalidades não levarão muito tempo para serem implementadas, mas outras delas poderão demorar. Por isso, é importante ramificar o repositório para que você consiga gerenciar o fluxo de trabalho, isolar seu código e controlar quais funcionalidades de fato serão colocadas na ramificação master do repositório.

Por padrão a ramificação principal do repositório do projeto é normalmente chamada de master branch. Uma boa prática comum é considerar tudo que está na master branch pronta para uso/deploy a qualquer tempo.

Então vamos lá.

## Crie uma nova ramificação

Entre no repositório e crie uma nova ramificação para trabalhar:

`git branch nova-ramificacao`

Mude para a nova ramificação:

`git checkout nova-ramificacao`

Se você quiser retornar à ramificação master local, basta digitar:

`git checkout master`

Agora faça as alterações localmente. Depois de fazer, adicione as mudanças da mesma forma que você fez no primeiro tutorial:

`git add -A`

Da mesma forma, confirme as alterações no repositório:

`git commit -m "Adicionada documentação sobre ramificações"`

Verifique se não há mais nada para alterar:

`git status`

Nesse ponto você pode usar o comando `git push` para enviar as alterações para a ramificação atual do repositório que você fez fork.

`git push --set-upstream origin nova-ramificacao`

## Criando um Remote para o repositório que você fez fork. 

Para poder sincronizar as mudanças que você fez em um fork com o repositório original que você está trabalhando, você precisa configurar um remote que referencia o repositório upstream. Isso é feito apenas uma vez.

Verifique os remotos atuais:

`git remote -v` 

Nesse caso vão aparecer apenas os remotos do repositório que você fez fork.

Agora adicione o repositório original como upstream:

`git remote add upstream https://github.com/nomeusuario-dono-original/repositorio-original.git`

Verifique que agora você tem o upstream, representando o repositório remoto original:

`git remote -v`

## Sincronize o seu fork com o repositório oficial:

`git fetch upstream`

Agora, os commits na ramificação master serão armazenados em uma ramificação local chamada upstream/master.

Vamos para a master então:

`git checkout master`

Agora vamos fazer a mesclagem ou **merge** de quaisquer mudanças feitas na ramificação master do repositório original, as quais poderemos acessar através de nossa ramificação upstream/master:

`git merge upstream/master`

Finalmente, crie o pull request para solicitar o merge da ramificação master do repositório original e a sua ramificação nova-ramificacao. O pull request em si você já sabe fazer, como no primeiro tutorial.

**Obs:** Esse pull request foi feito usando essa prática.
