# 📱 Civis+

**Civis+** é um aplicativo guia de cidades desenvolvido com **.NET MAUI** para Android.  
O projeto explora funcionalidades nativas do dispositivo, como geolocalização, e o consumo de múltiplas APIs públicas para fornecer informações ricas sobre localidades e dados demográficos do Brasil.

Este projeto foi construído passo a passo, focando em resolver problemas comuns de desenvolvimento, desde a criação da interface até o tratamento de erros de compilação e a integração com serviços web.

---

## 📝 Índice
- [Funcionalidades](#-funcionalidades)  
- [Telas do Aplicativo](#-telas-do-aplicativo)  
- [Tecnologias Utilizadas](#-tecnologias-utilizadas)  
- [Como Executar o Projeto](#-como-executar-o-projeto)  
- [Conceitos Implementados](#-conceitos-implementados)  
- [Próximos Passos](#-próximos-passos)  
- [Autor](#-autor)  
- [Licença](#-licença)  

---

## ✨ Funcionalidades

- [x] **Navegação por Abas:** Interface principal com 3 seções (Home, Cidades, Nomes) utilizando o **.NET MAUI Shell**.  

- [x] **Tab "Cidades":**
  - **Geolocalização:** Solicita permissão e obtém as coordenadas GPS do usuário.  
  - **API Chaining:**  
    - Utiliza a API do **Nominatim (OpenStreetMap)** para realizar geocodificação reversa.  
    - Com o **CEP** obtido, consome a **API ViaCEP** para buscar detalhes brasileiros (DDD, IBGE).  
    - Com o código **IBGE**, consome a **API do IBGE** para obter a projeção da população.  
  - **Cache Inteligente:** Armazena os dados da última consulta em **Preferences** para carregamento instantâneo e só busca atualizações quando os dados estão expirados.  
  - **Interface Reativa:** Exibe estados de *carregamento* e apresenta os dados de forma organizada na tela.  

- [x] **Tab "Nomes":**
  - **Consumo de API REST:** Busca e exibe o ranking de nomes mais comuns no Brasil a partir da **API de Censos do IBGE**.  
  - **Lista com Busca Dinâmica:** Apresenta os dados em uma **CollectionView** com uma barra de pesquisa que filtra os resultados em tempo real.  

- [x] **Identidade Visual:**
  - **Ícone e Splash Screen Customizados:** Identidade visual personalizada para o aplicativo.  

---

## 📱 Telas do Aplicativo

- Tela de Permissão (Cidades)  
- Tela de Ranking (Nomes)  

---

## 🛠️ Tecnologias Utilizadas

- **Framework:** .NET 8 / .NET MAUI  
- **Linguagem:** C# e XAML  
- **Bibliotecas e Pacotes:**  
  - CommunityToolkit.Maui  
  - System.Text.Json  
- **APIs Externas:**  
  - Nominatim (OpenStreetMap)  
  - ViaCEP  
  - IBGE Serviço de Dados  

---

## 🚀 Como Executar o Projeto

Para compilar e executar este projeto, você precisará de:  
- **Visual Studio 2022** (versão 17.8 ou superior)  
- **Carga de Trabalho .NET MAUI** instalada no Visual Studio.  
- **SDK do .NET 8**  

### Passos:
1. Clone este repositório:
   ```bash
   https://github.com/MiguelCunha2012/Civis.git
