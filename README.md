# 💡 Detecção de Queda de Energia com Python e MediaPipe

### 👥 Grupo:
- **Guilherme Dal Posolo Matheus** – RM: 98694  
- **Ryan Perez Pacheco** – RM: 98782  
- **Guilherme Faustino Vargas** – RM: 98278  

---

# LINK VIDEO: https://www.youtube.com/watch?v=bhFrP2f4oms&ab_channel=GuilhermeDal

## 🛑 Descrição do Problema

As quedas de energia em ambientes urbanos podem causar transtornos significativos à segurança pública, à mobilidade e ao funcionamento de serviços essenciais. No entanto, a identificação automática e em tempo real desses eventos em áreas externas — como ruas e avenidas — ainda é um desafio, principalmente devido à dificuldade de monitorar a iluminação pública de forma precisa.

Esse é um problema bastante atual, especialmente quando analisamos a cidade de São Paulo, que tem enfrentado frequentes apagões, gerando caos em diversas regiões.

**O problema central deste projeto é:**

> Como identificar automaticamente, por meio de vídeo, quando ocorre uma queda de energia em postes de luz urbanos e notificar autoridades e cidadãos de forma mais assertiva e rápida, permitindo uma resposta adequada ou até mesmo a prevenção de circulação por áreas afetadas?

---

## 💡 Visão Geral da Solução

A solução proposta utiliza **Python**, **MediaPipe** e **OpenCV** para analisar um vídeo gravado em um cenário real, simulando postes de luz. O sistema é capaz de:

- Detectar **presença humana** por meio de *pose detection* com MediaPipe.
- Calcular o **brilho médio** de cada poste monitorado.
- Identificar **variações de brilho** que indicam um possível "apagão".
- Verificar o **horário do dia** (via API de meteorologia solar) para considerar apenas eventos noturnos como quedas reais de energia.

---

### 📌 Funcionalidades Adicionais:

- Mostra visualmente os postes monitorados no vídeo, com indicação de brilho.
- Registra logs de eventos em um arquivo `.json`, contendo:
  - Nome do poste
  - Tipo do evento ("apagão" ou "luz voltou")
  - Horário exato
  - Localização aproximada (com base no IP ou coordenadas reais)
- Envia **alertas por e-mail** automaticamente sempre que uma queda ou retorno de luz for detectado durante o período noturno.

---

### 🔁 Integração com Outros Projetos

Este projeto de IoT foi integrado ao projeto de **Arquitetura de Software**, onde:
- Os **logs de eventos de queda de energia**, gerados localmente pelo sistema IoT, são disponibilizados como uma **API**.
- O projeto de Arquitetura consome essa API, permitindo visualização e análise dos dados coletados.

---

### 🌕 Antes da Queda de Energia  
*Postes de luz acesos com brilho alto sendo monitorados pelo sistema.*
![image](https://github.com/user-attachments/assets/b9be4463-f720-4358-a8c6-2bd3036c2a58)

### 🌑 Após a Queda de Energia  
*Postes com brilho reduzido indicando queda de energia detectada pelo sistema.*
![image](https://github.com/user-attachments/assets/5b0510fe-eb9c-443b-bfd0-31e6e6546bf6)

### 🖥️ Terminal - Notificação da Queda  
*Print do console com mensagens de detecção de apagão e retorno da luz.*
![image](https://github.com/user-attachments/assets/5c9a5814-87ee-47c8-8d58-21ef03f09356)

### 🗂️ Log JSON Gerado  
*Estrutura de log contendo o registro da queda de energia.*

![image](https://github.com/user-attachments/assets/81fd250c-48db-4078-84c4-dce74c588779)

### 📧 Alerta de Apagão no E-mail  
*Confirmação do envio automático do alerta por e-mail.*
![image](https://github.com/user-attachments/assets/9a628d66-4e00-41d5-8522-f9bc8c24512f)


