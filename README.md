# test_selenium_carrinho_cp
# Script de Teste para Adição de Produtos ao Carrinho de Compras

Este repositório contém um script de teste usando Selenium que simula a adição de produtos a um carrinho de compras em um site de e-commerce. Este trabalho pode ser realizado em dupla.

## Componentes da Dupla
- **Nome 1**
- **Nome 2**

## Descrição dos Procedimentos de Teste

### Importações
- **pytest**: Framework de teste que permite executar e gerenciar testes.
- **webdriver**: Fornece a interface para interagir com o navegador.
- **By**: Módulo para localizar elementos na página usando diferentes estratégias (por exemplo, CSS Selector, XPath).
- **ActionChains**: Permite realizar ações complexas, como arrastar e soltar, mover o mouse, etc.
- **expected_conditions** e **WebDriverWait**: Usados para implementar esperas explícitas para garantir que determinados estados sejam atingidos antes de continuar.
- **Keys**: Fornece constantes para simular a digitação de teclas (como ENTER, ESC, etc.).
- **DesiredCapabilities**: Permite definir configurações específicas para o navegador.

### Classe `TestTestlojapc`
- **Método `setup_method`**:
  - Executado antes de cada método de teste para configurar o ambiente.
  - Inicializa uma instância do WebDriver para o Chrome.
  - Inicializa um dicionário `vars` para armazenar variáveis que podem ser usadas durante os testes.
  
- **Método `teardown_method`**:
  - Executado após cada método de teste para garantir que o navegador seja fechado corretamente.
  - Fecha a instância do navegador e encerra a sessão do WebDriver.

- **Método `test_testlojapc`**:
  - Contém o código do teste propriamente dito.
  - Navega até a URL especificada.
  - Define o tamanho da janela do navegador.
  - Localiza e interage com elementos na página usando seletores CSS e realiza cliques.

### Bloco `if __name__ == "__main__":`
- Permite que o script execute os testes diretamente se o arquivo for executado como um script Python, chamando o `pytest.main()`.
  - **Quando Executado Diretamente**:
    - `python nome_do_script.py` executará pytest e rodará os testes definidos no script.
  - **Quando Importado**:
    - Se o script for importado como um módulo em outro script ou em um ambiente de testes (por exemplo, ao rodar todos os testes com pytest), `pytest.main()` não será chamado, evitando a execução dos testes fora do contexto esperado.

### Observações
- **Interações Redundantes**: O código contém duas interações consecutivas com o mesmo elemento CSS. Isso pode ser um erro ou uma duplicação desnecessária.
- **Tratamento de Erros e Esperas Explícitas**: O código não inclui tratamento de erros ou esperas explícitas além do simples `find_element`. Isso pode ser importante para testes mais robustos.

## Conclusão
O bloco `if __name__ == "__main__":` é uma prática recomendada em Python para garantir que certos blocos de código (como o código de teste) só sejam executados quando o script é executado diretamente, e não quando é importado como um módulo. Isso ajuda a evitar efeitos colaterais inesperados e torna o código mais modular e reutilizável.

