# Instituto Educar - (S)CSS Style Guide

### Hierarquia de arquivos e pastas
Todo projeto deverá seguir esta estrutura de pastas abaixo.
```
├── resources/
    ├── js/
    ├── css/
        ├── main.scss
        ├── settings/
            ├── _variables.scss
            ├── _tools.scss
        ├── base/
            ├── _generic.scss
            ├── _base.scss
        ├── components/
            ├── _component-1.scss
            ├── _component-2.scss
            ├── _component-N.scss
    ├── fonts/
    ├── images/
```

####main.scss
Este é o arquivo que vai importar todos os arquivos scss que iremos utilizar.
Não pode conter estilização dentro do arquivo, apenas imports.

**main.scss**
```scss
  @import "settings/variables";
  @import "settings/tools";

  @import "base/generic";
  @import "base/base";

  @import "components/component-1";
  @import "components/component-2";
```

####settings/

Aqui devem estar as configurações e ferramentas utilizadas no projeto.

*Exemplo:*

**_variables.scss**
```scss
  //Em geral são as variáveis globais que vão definir cores, espaçamentos e outras configurações desejadas
  $default_bg: #BADA55;
  $menu-height: 120px;
```
____
**_tools.scss**
```scss
  //Aqui você vai declarar os mixins e funções necessários para o seu projeto.
  //Pode ser qualquer coisa, desde mixins de font-face, até mixins de animações, etc.
  @mixin font-brand() {
    font-family: "UI font", sans-serif;
    font-weigth: 400;
  }
```

####base/

Aqui deve estar a estilização generica e a base do projeto.

*Exemplo:*

**_generic.scss**
```scss
  //Aqui é onde devemos colocar a estilização para as propriedades mais genéricas
  //e com menor especificidade possível.
  * {
    box-sizing: border-box;
  }
```

**_base.scss**
```scss
  //Aqui vai ficar toda estilização base do seu projeto.
  @mixin font-brand() {
    font-family: "UI font", sans-serif;
    font-weigth: 400;
  }
```

####components/

Aqui vão ficar os componentes que serão reutilizados no projeto.

*Lembre-se de adicionar o '_' (underline) como prefixo no arquivo*

### Nomeclatura de classes

- O nome da classe deverá ser coerente com a função que o elemento exerce.
- Evite criar classes com nome muito grande.
- Pense de forma escalável e reutilizável
- Ao criar um componente, evite definir propriedades do tipo *position, top, left, float, margin*

*Obs.: Alguns projetos podem não seguir por completo este guia. Porém, deve-se basear nele.

### Comentários

- Para facilitar a organização, todos os arquivos css/html devem ser comentados.  
