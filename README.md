# 🧪 Sistema de Controle de Amostras | Pantaneiro

Sistema web corporativo desenvolvido para o gerenciamento, rastreabilidade e acompanhamento em tempo real do fluxo de desenvolvimento de amostras entre os setores da empresa (**Vendas, Modelagem, Compras, Produção, Custos e Gerência**).

---

## 🚀 Tecnologias Utilizadas

* **Frontend:** HTML5, CSS3, JavaScript (Vanilla ES6+)
* **Estilização:** [Tailwind CSS](https://tailwindcss.com/) (via CDN)
* **Banco de Dados & Backend:** [Supabase](https://supabase.com/) (PostgreSQL, Autenticação e Storage)
* **Segurança:** Sanitização de inputs contra XSS e controle de acesso baseado em papéis (RBAC).

---

## 👥 Níveis de Acesso e Permissões (RBAC)

O sistema conta com perfis dinâmicos de acesso de acordo com o setor do colaborador:

* **🏷️ Vendas:** Cadastra novas amostras e acompanha o andamento geral.
* **📐 Modelagem:** Gerencia e movimenta as amostras na fila do setor de modelagem.
* **🛒 Compras:** Controla insumos e materiais necessários para as amostras.
* **🚚 Produção:** Acompanha a fabricação física e o avanço operacional.
* **💰 Custos:** Analisa viabilidade financeira e precificação.
* **📊 Gerência / Gantt:** Visualização gerencial completa com métricas de desempenho e Gráfico de Gantt considerando turnos oficiais de expediente.
* **⚙️ Administrador Master:** Acesso total ao sistema, incluindo o painel de gerenciamento de usuários e senhas.

---

## 📋 Funcionalidades Principais

1. **Consulta Geral Pública:** Permite que qualquer colaborador visualize o status atual, solicitante, número do pedido e histórico de linha do tempo de qualquer amostra.
2. **Gráfico de Gantt Inteligente:** Mapeamento de prazos considerando os dias úteis e horários de expediente da Pantaneiro (Seg-Qui: 07h30–17h30 | Sex: 07h30–16h30).
3. **Upload de Fichas Técnicas:** Suporte ao envio de arquivos PDF e imagens diretamente para o armazenamento em nuvem do Supabase.
4. **Design Responsivo:** Interface otimizada tanto para computadores quanto para dispositivos móveis (smartphones e tablets).

---

## ⚙️ Configuração e Instalação

Como o projeto utiliza tecnologias via CDN (Tailwind e Supabase JS Client), não é necessário instalar dependências locais via Node.js para rodá-lo.

1. Clone o repositório ou baixe o arquivo HTML principal.
2. Certifique-se de que as chaves de conexão do Supabase estão configuradas no script:
   ```javascript
   const SUPABASE_URL = "SUA_SUPABASE_URL";
   const SUPABASE_KEY = "SUA_SUPABASE_ANON_KEY";
