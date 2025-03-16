# Análise de Sentimentos com Azure Language Studio  

Este projeto foi desenvolvido durante o **Bootcamp Decola Tech 2025**. O objetivo foi utilizar os serviços do **Azure** para construir um sistema de pesquisa e análise de sentimentos em resenhas de uma cafeteria.  

---

## 🚀 Implementação  

### 1️⃣ Configuração dos Recursos  

Para viabilizar o projeto, foram criados três recursos essenciais:  
- **Azure AI Search** (mecanismo de busca),  
- **Azure AI Services** (análise de texto),  
- **Conta de Armazenamento** (para armazenar os documentos das resenhas).  

Esses recursos permitiram a organização dos dados e a integração com o serviço de busca.  

### 2️⃣ Upload das Resenhas  

As avaliações foram baixadas do [guia do laboratório de AI Search](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/11-ai-search.html) e enviadas para um _container_ dentro da conta de armazenamento.  

### 3️⃣ Importação e Indexação dos Dados  

No **Azure AI Search**, os dados foram importados e indexados. Durante essa etapa, foram definidos quais elementos seriam extraídos das resenhas, como:  
✅ Localização,  
✅ Opiniões,  
✅ Palavras-chave,  
✅ Sentimentos.  

Após a indexação, os dados estavam prontos para consulta.  

---

## 🔎 Realizando Buscas  

O **Azure AI Search** permite buscas diretamente na aba **Explorador de Pesquisa**. Por exemplo, a seguinte consulta JSON:  

```json
{
  "search": "sentiment:'positive'",
  "count": true
}
```
Retorna todas as resenhas classificadas como **positivas** pela IA.  

Exemplo de resultado:  
```json
{
  "@search.score": 0.6931472,
  "content": "I love the coffee drinks here, but my favorite part is the local art they sell...",
  "locations": ["Seattle", "Washington"],
  "keyphrases": ["coffee drinks", "local art", "paintings"],
  "sentiment": "[\"positive\"]"
}
```  

Além da análise de sentimentos, o sistema também detecta elementos nas imagens anexadas às resenhas, categorizando-as por _tags_ como "pessoa", "computador" e "arte".  

---

## 📌 Conclusão  

O **Azure AI Search** se mostrou uma ferramenta poderosa para busca e análise de dados em grande escala. Sua aplicação vai além da análise de resenhas, podendo ser utilizada para:  
✅ Atendimento ao cliente,  
✅ Análise de feedbacks,  
✅ Gestão de histórico de compras,  
✅ E muito mais!  

A tecnologia da **Microsoft Azure** abre diversas possibilidades para análise automatizada de textos e imagens, otimizando processos e facilitando a extração de informações valiosas. 🚀
