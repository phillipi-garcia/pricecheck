<p align="center">
  <img src="codigo/assents/image/logo.png" alt="PriceCheck" width="160">
</p>

# PriceCheck

Comparador de preços desenvolvido em equipe no Trabalho Interdisciplinar de Aplicações Web (TIAW) do curso de Análise e Desenvolvimento de Sistemas da **PUC Minas** (2024/1). A aplicação busca produtos na API do Mercado Livre e ajuda o usuário a encontrar o menor preço, acompanhar produtos de interesse e comparar opções antes de comprar.

O projeto foi desenvolvido em sprints, com metodologias ágeis, partindo de um processo de design thinking (personas, mapa de stakeholders, matriz CSD) documentado na pasta [`docs`](docs).

## Funcionalidades

- **Busca de produtos** por nome, com cards de preço, parcelamento e frete grátis, consumindo a API REST do Mercado Livre
- **Página do produto** com carrossel de fotos, especificações técnicas, descrição, produtos relacionados da mesma categoria e botão que leva ao anúncio
- **Lista de desejos** por usuário
- **Comentários e avaliação** com estrelas em cada produto
- **Login, cadastro e painel de usuário** para editar e excluir contas
- **Home** com carrossel e vitrines de ofertas, smartphones e eletrodomésticos

## Tecnologias

- HTML5, CSS3 e JavaScript
- Bootstrap 4, Bootstrap Icons e jQuery
- API REST do Mercado Livre (`fetch` com `async/await`)
- `localStorage` e `sessionStorage` para sessão, lista de desejos e comentários
- Git e GitHub em equipe

## Minha participação

Sou **Phillipi Garcia**, um dos sete integrantes da equipe. No projeto eu:

- desenvolvi a **tela principal (home)**, que serviu de base para a versão final (`codigo/telamain.html` e `codigo/assents/css/telamain.css`);
- criei, nas sprints anteriores, o protótipo da **tela de notificações**, que avisa quando um item da lista de desejos entra em promoção, e um **gráfico de histórico de preços** com Chart.js.

## Como executar

Os caminhos do projeto são absolutos (`/codigo/...`), então o servidor precisa ser iniciado na **raiz do repositório**:

```bash
git clone https://github.com/phillipi-garcia/pricecheck.git
cd pricecheck
python -m http.server 8000
```

Depois, acesse `http://localhost:8000/codigo/telamain.html`.

Também funciona com a extensão Live Server do VS Code, abrindo a pasta raiz do repositório.

## Limitações conhecidas

- Desde 2025, o Mercado Livre passou a restringir o endpoint público de busca (`/sites/MLB/search`), que pode responder **403** sem um token de acesso. Com isso, a busca e as vitrines podem não carregar resultados. A evolução natural seria um back-end próprio que guarde o token no servidor e faça a ponte com a API.
- O login é uma simulação no navegador, feita para fins acadêmicos: os dados ficam no `localStorage` e não há autenticação real.

## Equipe

- Alex Mendes dos Santos
- Arthur Leandro Jacinto
- Higor Antônio da Silva
- João Pedro Gomes da Silva
- Pedro Augusto Cruz de Almeida
- Phillipi Garcia da Silveira
- Ramon Pereira de Souza

**Professores:** Amália Soares Vilela de Vasconcelos e Leonardo Vilela Cardoso

## Licença

Distribuído sob a licença [Creative Commons Attribution 4.0 International](LICENSE).
