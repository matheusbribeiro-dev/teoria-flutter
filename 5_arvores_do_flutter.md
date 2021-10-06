# Árvores do Flutter

O Flutter se diz um framework que tem um nível de composição agressivo, ou seja, toda a aplicação é composta por um conjunto de Widgets e componentes formando outros componentes mais complexos.

A partir do momento de desenvolvimento do código até a rederização na tela existe um processo:

## Widget Tree
> Árvore definida no método ``build``. Estamos falando da própria árvore de widgets.

- Configuração.
- Define a estrutura da aplicação.
- Ao ocorrer um processo de atualização - 'repintagem' da tela por exemplo - o método ``build`` é chamado e os componentes reconstruídos.
- Imutável.
  - > O estado é quem evolui, quando se tem um StatefulWidget ele é recriado a cada mudança. Por isso a separação entre State e StatefulWidget
## Element Tree
> Liga o Widget ao componente renderizado.

- Estrutura lógica.
- Aqui é onde se armazena o estado de um determinado componente.
- Há para todo componente da Widget Tree um Element presente nesta árvore(Element Tree) ligados por uma referência. 
- Nesta ligação o Element é responsável por capturar os dados no Widget e transmitir para o objeto de renderização. 
## Render Tree
> Objeto renderizado na tela.

- O que se vê na tela.
- Objeto renderizado que desenha os pixels na tela.
- Aqui há para cada Element da Element Tree uma referência para o Rendered Box presente neste árvore(Render Tree).