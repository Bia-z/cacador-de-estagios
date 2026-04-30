# Caçador de Estágios

## Sobre o Projeto
**Projeto:** Caçador de Estágios
**Problema que resolve:** Dificiculdade de universitários para encontrar estágio

## Integrantes
| Nome | GitHub |
|------|--------|
| Beatriz Caroline Moreno Tavares | Bia-z |
| Cauã Queiroz Guerra | Caua-Guerra |
| Natã de Almeida Santos  | Natan938 |

## Arquitetura

```mermaid
flowchart LR
    A[Usuário envia formulário] --> B[Requisição HTTP GET<br/>LoopCV API]
    B --> C[(JSON da API)]
    C --> D[Processamento com Gemini<br/>Extração e interpretação]
    
    D --> E{Cargo = Júnior<br/>ou Estágio?}
    
    E -- true --> F[Webhook / Resposta<br/>Vaga relevante]
    E -- false --> G[Webhook / Resposta<br/>Vaga ignorada]
```
