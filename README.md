# Organizador de Finanças

Aplicação web simples para acompanhar receitas, despesas e orçamento pessoal. Os
dados ficam salvos no navegador e a aplicação pode ser instalada como PWA.

## Funcionalidades

- Cadastro, edição e exclusão de receitas e despesas
- Dashboard com saldo, total de receitas, despesas e orçamento
- Gráficos por categoria e fluxo mensal
- Filtros por período, tipo e categoria
- Tema claro e escuro
- Exportação dos lançamentos em CSV e PDF
- Armazenamento local com `localStorage`
- Funcionamento offline após o primeiro carregamento, usando Service Worker

## Como executar

O projeto é estático e não exige build ou dependências locais. Para executar:

1. Clone o repositório:

   ```bash
   git clone https://github.com/JvNeves-7/finan-as.git
   cd finan-as
   ```

2. Inicie um servidor HTTP local:

   ```bash
   python -m http.server 8000
   ```

3. Acesse [http://localhost:8000](http://localhost:8000).

> O Service Worker não funciona corretamente quando o arquivo é aberto
> diretamente com `file://`. Use sempre um servidor HTTP local ou publique os
> arquivos em um serviço de hospedagem estática.

## Estrutura

| Arquivo | Descrição |
| --- | --- |
| `index.html` | Interface, estilos e lógica da aplicação |
| `manifest.webmanifest` | Configuração de instalação como PWA |
| `sw.js` | Cache dos recursos para uso offline |
| `icon.svg` | Ícone da aplicação |

## Tecnologias

- HTML5, CSS3 e JavaScript
- [Chart.js](https://www.chartjs.org/) para os gráficos
- [jsPDF](https://github.com/parallax/jsPDF) para exportação em PDF
- Web APIs: `localStorage`, Service Worker e instalação PWA

## Armazenamento e privacidade

Os lançamentos são armazenados apenas no `localStorage` do navegador utilizado.
Não há backend nem sincronização entre dispositivos. Limpar os dados do site ou
utilizar outro navegador remove ou não exibe os lançamentos existentes.

## Licença

Este projeto ainda não possui uma licença definida.
