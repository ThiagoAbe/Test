# challenge-QA

Este projeto é um teste prático para qualidade e automação, focado em testes automatizados utilizando Cypress e Docker.

## Detalhes do Entregável

- **Projeto:** [challenge-QA](https://qa-automacao.atlassian.net)
- **Aplicação:** Geek QA Gear

## Requisitos

- [Docker](https://www.docker.com/products/docker-desktop) instalado em sua máquina.
- [Cypress](https://www.cypress.io/) instalado e configurado.

## Configuração do Projeto

### 1. Clonar o Repositório

Abra o terminal do VS Code (ou qualquer terminal de sua preferência) e clone o repositório:

```bash
git clone https://github.com/techops-maitha/challenge-QA.git
Em seguida, acesse a raiz do projeto:

bash
Copiar código
cd challenge-QA
2. Construir e Iniciar os Contêineres
No terminal, execute o seguinte comando para construir e iniciar os contêineres:

bash
Copiar código
docker-compose up --build
3. Acessar a Aplicação
Após os contêineres estarem em execução, você poderá acessar a aplicação em seu navegador, através do endereço:

bash
Copiar código
http://localhost
Estrutura Docker
docker-compose.yml: Arquivo de configuração do Docker Compose.
Dockerfile: Arquivo de configuração para a criação da imagem Docker.
Testes Automatizados com Cypress
1. Configuração do Cypress
O Cypress foi configurado para testar a aplicação localmente. A resolução da tela foi ajustada para 2560x1080 para refletir o monitor ultrawide.

2. Scripts de Teste
a. Homepage
Foi criado um teste para validar a presença dos principais elementos na homepage da aplicação, incluindo:

Contêiner de produtos
Produtos individuais
Elementos da interface (título, botões, campos de busca, etc.)
b. Paginação
Foi implementado um teste para verificar a navegação pelas páginas de 1 a 10. O script inclui:

Validação da presença dos botões de navegação.
Clique em cada botão de página numerada.
Navegação e validação com o botão 'Próximo' após a página 5.
c. Filtros de Categoria
Foi desenvolvido um teste para aplicar cada filtro de categoria e verificar a presença dos produtos esperados. O script cobre:

Aplicação de filtros de categorias como 'all', 'clothing', 'decor', 'posters', entre outros.
Verificação da visibilidade dos produtos de acordo com o filtro selecionado.
d. Ordenação de Produtos
Foi criado um teste para validar a funcionalidade de ordenação dos produtos com as opções disponíveis:

Nome (A-Z)
Nome (Z-A)
Preço (Menor para Maior)
Preço (Maior para Menor)
O teste garante que o contêiner de produtos está visível após a seleção de cada opção de ordenação.

O Que Foi Feito
Montagem e configuração do ambiente Docker para rodar a aplicação localmente.
Implementação de scripts de teste com Cypress para validar funcionalidades principais da aplicação.
Ajuste da configuração do Cypress para refletir a resolução do monitor ultrawide e garantir a visualização completa.
O Que Não Foi Feito
Testes de funcionalidade de login, pois a aplicação não possui uma tela de login.
Testes mais detalhados sobre o conteúdo dos produtos, como preços e descrições, devido ao foco em presença e navegação.
Melhorias Futuras
Implementar testes mais aprofundados para validar o conteúdo dos produtos, como preços e descrições.
Adicionar testes para casos de uso adicionais, como interações mais complexas e fluxos de trabalho de usuários.
Melhorar a cobertura de testes para incluir cenários de erro e validação de mensagens de feedback.
