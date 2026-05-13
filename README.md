# 📚 Miniguia de Estudos: Wireshark e Fundamentos de Redes

## 📝 Contexto e Objetivos

Este caderno temático foi desenvolvido para consolidar conhecimentos sobre o funcionamento das redes de computadores, utilizando o **Wireshark** como ferramenta principal de análise.

* **Objetivo Principal:** Aprender a capturar, filtrar e analisar pacotes de dados para diagnosticar problemas de conectividade e entender protocolos de comunicação.
* **Público-alvo:** Estudantes de tecnologia e profissionais de infraestrutura/segurança.

## 🔍 Curadoria de Fontes

Utilizei as seguintes fontes abertas para alimentar o NotebookLM:

1. **Wireshark User's Guide (v4.1.0):** Documentação oficial detalhando funcionalidades avançadas.
2. **Tutorial de Wireshark (Mauro Oliveira):** Guia prático em português focado em primeiros passos.
3. **Artigo Acadêmico - As Camadas do Modelo OSI:** Estudo sobre a relação entre o modelo teórico e os protocolos reais.
4. **Curso de Fundamentos de Redes (2024):** Base teórica sobre topologias, meios físicos e arquitetura cliente-servidor.

## 🛠️ Engenharia de Prompts e "Cicatrizes"

Aqui registro como interagi com a IA para extrair o melhor conhecimento:

| Pergunta Estratégica (Prompt) | Resultado/Insight | Dificuldade Encontrada (Troubleshooting) |
| --- | --- | --- |
| "Explique o processo de Three-Way Handshake do TCP usando uma metáfora de atendimento telefônico." | A IA explicou o SYN, SYN-ACK e ACK de forma muito didática. | Inicialmente, a resposta foi muito técnica. Tive que pedir para "usar uma metáfora cotidiana" para facilitar a memorização. |
| "Quais são os filtros de exibição mais usados para identificar lentidão no DNS?" | Forneceu filtros como `dns.flags.response == 1` e explicou o cálculo de tempo. | A IA misturou filtros de captura com filtros de exibição. Precisei corrigir o prompt especificando que queria "filtros de visualização após a captura". |
| "Resuma as principais diferenças entre o modelo OSI e o modelo TCP/IP conforme as fontes." | Gerou uma tabela comparativa clara entre as 7 camadas OSI e as 4 do TCP/IP. | Algumas fontes divergiam levemente na nomenclatura das camadas. Precisei pedir para a IA priorizar a definição do Guia Técnico. |

---

## 📖 Miniguia de Estudo

### 1. Resumos Estruturados

* **O que é o Wireshark:** É um analisador de protocolos de rede que permite examinar o que está acontecendo dentro de um cabo de rede em detalhes. É comparado a um "multímetro" para eletricistas.
* **Captura de Dados:** O processo envolve selecionar uma interface (NIC), iniciar a captura em modo promíscuo e aplicar filtros para não ser "inundado" por tráfego irrelevante.
* **Análise de Protocolos:** Através das cores e flags (como SYN, FIN, RST), é possível identificar se uma conexão foi estabelecida com sucesso ou se houve uma falha de comunicação.

### 2. Glossário de Conceitos

* **PDU (Protocol Data Unit):** A unidade de dados em cada camada (ex: Frames na Camada 2, Pacotes na Camada 3, Segmentos na Camada 4).
* **Three-Way Handshake:** Processo de três etapas (SYN, SYN-ACK, ACK) usado pelo TCP para estabelecer uma conexão confiável.
* **Promiscuous Mode:** Configuração que permite à placa de rede capturar todo o tráfego que passa pelo segmento, não apenas o destinado a ela.
* **Encapsulamento:** Processo de adicionar cabeçalhos de protocolos à medida que os dados descem as camadas do modelo OSI.

### 3. Prompts Reutilizáveis para Revisão

* *"Atue como um instrutor de redes e crie um quiz de 5 perguntas sobre análise de tráfego HTTP no Wireshark."*
* *"Dada uma captura com muitos pacotes 'TCP Retransmission', quais são os 3 primeiros passos para investigar a causa raiz?"*
* *"Explique para um iniciante a diferença entre um Hub, um Switch e um Roteador com base no modelo OSI."*

--
