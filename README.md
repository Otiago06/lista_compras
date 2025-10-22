# 🛒 Minha Compra Inteligente - Controle de Gastos em Tempo Real

**Minha Compra Inteligente** é uma aplicação PWA (Progressive Web App) para rastreamento e controle de gastos de supermercado em tempo real. Ela foi desenvolvida para ajudar o usuário a manter o orçamento sob controle enquanto está no carrinho, com funcionalidades avançadas como leitura de código de barras e persistência de dados local.

## ✨ Funcionalidades Principais

- **Rastreamento em Tempo Real:** Visualização imediata do valor total acumulado da compra.
    
- **Adição Rápida de Itens:** Interface simples e eficiente para adicionar a descrição, quantidade e preço unitário de cada produto.
    
- **Scanner de Código de Barras (EAN):** Integração com **QuaggaJS** para usar a câmera do dispositivo e ler códigos de barras, preenchendo o nome do produto automaticamente via API (Open Food Facts).
    
- **Edição e Remoção:** Facilidade para atualizar ou remover itens da lista a qualquer momento.
    
- **Persistência de Dados (PWA):** Todos os dados são salvos localmente no `localStorage` do navegador, permitindo o uso offline e mantendo o histórico da compra.
    
- **Exportação:** Opção de exportar a lista de compras completa, incluindo os totais, para um arquivo CSV.
    

## 🛠️ Tecnologias Utilizadas

Este projeto é um aplicativo de página única (SPA) construído com tecnologias web essenciais:

- **HTML5:** Estrutura base da aplicação.
    
- **Tailwind CSS:** Framework utilitário-first para estilização rápida e responsiva, garantindo uma ótima experiência em dispositivos móveis (Mobile-First Design).
    
- **JavaScript (ES6+):** Lógica de controle, manipulação do DOM e gerenciamento de estado local.
    
- **QuaggaJS:** Biblioteca de processamento de imagem para detecção e decodificação de códigos de barras (EAN13) em tempo real via câmera.
    
- **Open Food Facts API:** Usada para buscar o nome do produto automaticamente a partir do código de barras lido.
    

## 🚀 Como Usar a Aplicação

A aplicação é projetada para ser executada diretamente em um navegador moderno, sem a necessidade de servidor (devido ao uso de `localStorage`).

1. **Acesse o Arquivo:** Abra o arquivo `index.html` em qualquer navegador.
    
2. **Adicionar Item Manualmente:** Clique em **"Adicionar Item"** e preencha o nome, quantidade e preço unitário.
    
3. **Adicionar Item via Scanner (Recomendado):**
    
    - Clique em **"Adicionar Item"**.
        
    - Clique em **"Iniciar Leitor de Código de Barras"** (o botão verde).
        
    - **Permita** o acesso à câmera.
        
    - Aponte a câmera para o código de barras (EAN13).
        
    - Após a leitura, o nome será preenchido. Basta inserir o preço e a quantidade.
        

## 💾 Estrutura de Armazenamento de Dados

Os dados são armazenados localmente no navegador do usuário, seguindo a estrutura:

- **Tipo de Armazenamento:** `localStorage`
    
- **Chave Principal:** `minhaCompraList`
    
- **Estrutura de Dados:** Um array de objetos, onde cada objeto representa um item da lista:
    

```
[
  {
    "id": "item-unique-id-1",
    "name": "Arroz Agulhinha Tipo 1 - 5kg",
    "unitPrice": 25.50,
    "quantity": 1
  },
  {
    "id": "item-unique-id-2",
    "name": "Café em Pó 500g",
    "unitPrice": 12.99,
    "quantity": 2
  }
]
```

## ⚠️ Limitações e Notas

- **Local Storage:** Os dados são atrelados ao navegador e dispositivo em que foram inseridos. Eles não são sincronizados na nuvem.
    
- **API de Busca:** A consulta de produtos depende da disponibilidade e precisão da API Open Food Facts. Caso o produto não seja encontrado, o usuário é direcionado para a inserção manual dos detalhes.
    

**Desenvolvido por Tiago Oliveira**
