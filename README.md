# Azure OpenAI - DIO - Lab 02
Resumo do conteúdo aprendido durante o curso de Azure OpenAI na DIO

## API do Azure OpenAI  
- O Azure OpenAI oferece suporte a diferentes tipos de modelos:  
  - **Chat**: Interação conversacional com modelos avançados.  
  - **Completar**: Geração de texto baseado em entrada fornecida.  
  - **Imagens**: Criação de imagens a partir de descrições.  
  - **Áudio**: Conversão de fala em texto e vice-versa.  

- Exemplo de requisição `POST` para geração de texto:  
    ```json
    {
      "prompt": ["tell me a joke about mango"],
      "max_tokens": 32,
      "temperature": 1.0,
      "n": 1
    }
    ```
  
- Exemplo de configuração do cliente em Python:  
    ```python
    client = AzureOpenAI(
        azure_endpoint=os.getenv("AZURE_OPENAI_ENDPOINT"),
        api_key=os.getenv("AZURE_OPENAI_API_KEY"),
        api_version="2024-02-01"
    )
    ```

- Principais parâmetros utilizados nas chamadas de API:  
  - **Model ID**: Identifica o modelo de IA utilizado.  
  - **Temperature**: Controla a aleatoriedade das respostas.  
  - **Max tokens**: Define o limite de palavras geradas.  
  - **Top P**: Ajusta a diversidade da geração de texto.  
  - **Presence/Frequency penalties**: Controla repetição e relevância.  

---

## Armazenamento Seguro  
- O armazenamento de dados no Azure deve seguir boas práticas de segurança.  
- O uso de **variáveis de ambiente** evita a exposição de credenciais sensíveis.  
- **Azure Monitor** permite registrar logs e rastrear atividades na API.  

---

## Introdução ao Semantic Kernel  
- O **Semantic Kernel** atua como um middleware para integrar IA em aplicações.  
- Ele possibilita a criação de fluxos automatizados baseados em IA.  
- Seu uso facilita a incorporação de inteligência artificial em sistemas existentes.  

- Componentes principais:  
  - **Kernel Skills**: Pacotes de habilidades específicas para IA.  
  - **Functions**: Unidades de automação para tarefas específicas.  
  - **Memory**: Capacidade de armazenar e recuperar informações passadas.  

- Arquitetura do Semantic Kernel:  
  - **Kernel**: O núcleo que gerencia a execução dos modelos de IA.  
  - **Functions**: Implementação de lógica customizada baseada em IA.  
  - **Vector Stores**: Indexação e busca eficiente de informações.  

- Uso do Semantic Kernel para automação:  
  - Permite implementar agentes de IA personalizados.  
  - Suporte para integrar diferentes fontes de dados.  
  - Possibilita criar assistentes de IA interativos e adaptáveis
