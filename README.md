# LandingPage_MundoInvertido

Uma landing page criada com foco em prática de HTML, CSS e JavaScript, como parte da Semana Frontend DIO. O tema da página é baseado no universo de Stranger Things, especificamente no Mundo Invertido.

## Funcionalidades

- Alteração de temas (Mundo Normal e Mundo Invertido)
- Reproduz automaticamente uma música temática de acordo com o tema selecionado
- Formulário de inscrição para o Clube Dungeons & Dragons
- Galeria de imagens relacionadas à série Stranger Things
- Trailer da quarta temporada incorporado diretamente do YouTube

## Tecnologias Utilizadas

- **HTML5**: Estrutura do conteúdo da página
- **CSS3**: Estilização dos elementos visuais
- **JavaScript**: Lógica para alternar temas, controlar a reprodução de áudio e manipular o formulário de inscrição
- **Módulos JavaScript**: Utilização de `import` para separar a lógica de inscrição do Clube Dungeons & Dragons em um módulo externo

## Como utilizar

1. Clone o repositório em sua máquina local:
    ```bash
    git clone <url-do-repositorio>
    ```

2. Navegue até o diretório do projeto:
    ```bash
    cd nome-do-diretorio
    ```

3. Abra o arquivo `index.html` em seu navegador.

4. Ao clicar no botão "Inverter Mundos", o tema da página alterna entre Mundo Normal e Mundo Invertido, alterando também a música de fundo.

## Estrutura do Projeto

    ```bash
    /
    ├── assets/
    │   ├── images/         # Imagens utilizadas na página
    │   ├── musics/         # Músicas temáticas para os dois modos (normal e invertido)
    │   ├── style/          # Arquivos CSS
    ├── data/
    │   └── hellfire-clube.js   # Módulo responsável pelo gerenciamento da inscrição no clube
    ├── index.html          # Página principal do projeto
    └── assets/script/
        └── script.js       # Script principal responsável pela lógica de tema e formulário


## Módulo de Inscrição

O arquivo hellfire-clube.js é responsável por gerenciar as inscrições no Clube Dungeons & Dragons. Ele importa e utiliza a função subscribeToHellfireClube para adicionar os dados do formulário em um banco de dados simulado.

Exemplo de uso:

    ```bash
    import { subscribeToHellfireClube } from "./data/hellfire-clube.js";

    // Exemplo de inscrição
    const subscribe = {
    name: "John Doe",
    email: "john.doe@example.com",
    level: "10",
    character: "Barbarian",
    };

    const id = await subscribeToHellfireClube(subscribe);
    console.log(`Inscrição ${id} adicionada com sucesso!`);

## Requisitos

Navegador moderno com suporte a ES6 Modules (por exemplo, Google Chrome, Mozilla Firefox)
Conexão à internet para o carregamento de fontes externas e vídeos