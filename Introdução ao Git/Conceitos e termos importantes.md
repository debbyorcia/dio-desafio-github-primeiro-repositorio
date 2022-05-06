Um repositório, a grosso modo, é uma pasta que contém todos os arquivos do seu projeto e que possui o controle de versões através do Git. 

#### **Alguns conceitos básicos, mas importantes**

- **Clone**

Quando você cria um repositório novo em algum site de hospedagem de repositórios Git, como o GitHub, existe uma funcionalidade chamada Clone. O clone basicamente irá clonar o projeto do site (através de URL fornecida no repositório) para a sua máquina, existe um comando que pode ser executado no terminal ou você pode fazer através de algum programa que forneça uma interface para isso. Calma, avançando mais neste guia vamos mostrar como isso funciona na prática. 

- **Branchs**

Quando você tem um repositório, cada branch funciona como uma ramificação do seu repositório, e com isso, você pode criar várias branchs. 

Para exemplificar, imagine que você tem um projeto, nele existem features que estão em produção (já com usuários usando), existem algumas alterações que estão em desenvolvimento prontas para serem testadas mas não para ir para produção e também existem coisas novas sendo desenvolvidas mas que ainda não estão prontas para teste, como você separaria isso no seu repositório? Utilizando branchs. 

Podemos usar uma estrutura básica de branchs que podem ser: master, develop e features, onde na master ficam as coisas que já estão em produção, develop coisas que estão em desenvolvimento prontas para serem testadas e nas features, para cada funcionalidade nova que estiver desenvolvendo é criada uma nova feature, como mostra a figura abaixo.

Observe que as features sempre são criadas a partir de um ponto na develop. Na feature em amarelo, note que ela é criada em um ponto da develop e mais a frente elas se “unem” novamente, essa “união” é chamada de merge, que vamos explicar mais a frente. 

[![guia-de-git-para-iniciantes-branchs](https://jera.com.br/blog/wp-content/uploads/2020/09/guia-de-git-para-iniciantes-branchs.png)](https://jera.com.br/blog/wp-content/uploads/2020/09/guia-de-git-para-iniciantes-branchs.png)

- **Commits**

Os commits são como um pacote de alterações feitas em uma branch do seu repositório. Sempre que realizamos alterações, o ideal é que seja feito um commit. Esses commits não são alterados nunca pelo Git, a menos que você solicite a alteração.

Através dos commits você vai conseguir ter todo o histórico das versões dos arquivos do seu projeto. Todo commit tem os arquivos alterados, um autor e uma mensagem resumindo o que foi feito na alteração. 

- **Pushs e Pulls**

Sempre que um commit é feito, você precisará dar um push nele, o push é comando do Git que você pode rodar pelo terminal ou fazer por alguma interface gráfica, ele enviará de fato o seu commit para o site que está hospedando seu repositório Git. 

O pull é um comando do Git que pode ser usando em algumas situações, como por exemplo, você está trabalhando em um projeto que tem várias branchs, está codando sua feature na branch x e precisa de uma alteração que está na branch y, você pode usar o pull para pegar essas alterações. O mesmo vale para quando por algum motivo existem alterações novas na sua branch, mas você ainda não tem elas na sua máquina, dando o pull você atualiza a versão da sua máquina com a última versão que está no repositório.

- **Merges**

O merge é uma forma de unir suas alterações de uma branch em outra branch. Por exemplo, você está trabalhando na sua branch chamada feature/x, agora você terminou e quer subir para develop para poderem testar sua funcionalidade, você irá abrir um merge request para que suas alterações na branch feature/x possam ser “colocadas” na develop.

