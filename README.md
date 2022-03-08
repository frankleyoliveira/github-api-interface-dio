# Projeto DIO GitHub API Interface

Playlist do projeto:
https://www.youtube.com/playlist?list=PLTv2Rbwcr_Cru7KIHcffE1Shg9X9Eix7a

Repositório original:
https://github.com/benits/github-api-interface

## Minhas anotações sobre o projeto

**Parte 1**

- Após criar o projeto com npx create-react-app fazer uma limpa da pasta src, deixando apenas app.js e index.js

- Instalar axios e styled-components

- Olhar a documentação do github sobre como usar o github API

- Num primeiro momento usar dados mockados, para depois usar a API efetivamente
  - Mock = Algo que está sendo simulado.

**Parte 2**

- dentro de components foi criada a pasta profile com os arquivos index.js e styled.js

- No styled.js importar styled from 'styled-component'
  - exportar Wrapper = styled.div
  - Ao importar no index usar import * as S from "./styled"; (com isso usamos S.Wrapper ou S. qualquer coisa que criarmos no arquivo styled)

- Criar vários tipos de Wrappers, um para cada ocasião

**Parte 3**

- Criar pasta global dentro de src com um arquivo resetCSS.js
  - Neste arquivo importar o createGlobalStyle do styled-components (copiar código do site oficial)

  - criar uma const chamada resetCSS = createGlobalStyle e dentro dos `` colar o conteúdo do repositório destyle do nicolas cusan (https://github.com/nicolas-cusan/destyle.css)

  - dentro do seletor da tag body no resetCSS foi colocado a fonte roboto

- fontes são adicionadas no index.html na pasta public

- Para fazer tabs ele ia usar chakra-ui, mas mudou para react-tabs

- importar react-tabs dentro do arquivo styled.js no componente repositories
  - import { Tabs, TabList, Tab, TabPanel } from 'react-tabs'
  - export const WrapperTabs = styled(Tab)``

**Parte 4**

- Podemos usar &:focus {} dentro do styled
  - E também &.is-seletected {}

- Aula focada na estilização das tabs

**Parte 5**

- pasta providers com arquivo github-provider.js usando context api

- return <GithubContext.Provider value={contextValue}>{children}</GithubContext.Provider>

- COlocar o GithubContext em volta de tudo dentro da tag main no app.js

- Pasta hooks com arquivo github-hooks.js
  - importar useContext
- Função principal: const useGithub = () => {}

**Parte 6**

- função getUser dentro do github-provider, e usar api.get() dentro dessa função

**Parte 7**

- fazer os componentes consumir os dados da api do github

- fazer as lógicas para renderização condicional
  - Loading...
  - Nenhum usuário pesquisado

**Parte 8**

- Estilizar lista de repositórios
