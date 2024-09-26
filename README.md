
# Automação de Relatórios com Selenium

Este projeto automatiza o processo de geração e download de relatórios a partir de um sistema web específico, utilizando o Selenium WebDriver para controlar o navegador e interagir com a página.

## Funcionalidades

- Login automático no site.
- Navegação por menus para acessar a área de relatórios.
- Preenchimento de campos de data e seleção de opções.
- Download automático de relatórios em formato Excel.

## Requisitos

- Python 3.x
- Google Chrome
- WebDriver do Chrome (compatível com a versão do navegador)
- Bibliotecas Python:

  - `selenium`
  - `openpyxl`
  - `pandas`
  - `datetime`
  - `os`
  - `time`
  - `re`
  - `shutil`

## Instalação

1. **Clone o repositório**:
   ```bash
   git clone https://github.com/seuusuario/seu-repositorio.git
   cd seu-repositorio
   ```

2. **Instale as dependências**:
   Use o `pip` para instalar as bibliotecas necessárias:
   ```bash
   pip install selenium openpyxl pandas
   ```

3. **Configure o WebDriver**:
   Baixe o Chrome WebDriver [aqui](https://sites.google.com/a/chromium.org/chromedriver/downloads) e extraia o executável para uma pasta acessível.

4. **Configure as variáveis de login**:
   No código principal, ajuste as credenciais de login (`txtLogin` e `txtSenha`) e outras informações conforme sua necessidade.

## Uso

1. **Execute o script**:
   No terminal, navegue até o diretório do projeto e execute o script Python:
   ```bash
   python nome_do_script.py
   ```

2. **Processo Automatizado**:
   O script fará o seguinte:
   - Abrirá o navegador Chrome e acessará o site.
   - Preencherá automaticamente os campos de login e senha.
   - Navegará até o menu de relatórios.
   - Inserirá a data de início e fim.
   - Selecionará todas as entradas no dropdown.
   - Baixará o relatório em formato Excel.

## Configurações

### Alterar Datas

No código, as datas são inseridas automaticamente com a função `inserir_data_atual` para a data de início. Caso queira alterar a data de fim, modifique o seguinte trecho:
```python
campo_data_fim.send_keys("31/12/2024")
```

### Ajustar Login e Senha

No bloco de login, altere as credenciais diretamente no código:
```python
navegador.find_element(By.NAME, "txtLogin").send_keys("SEU_LOGIN")
navegador.find_element(By.NAME, "txtSenha").send_keys("SUA_SENHA")
```


