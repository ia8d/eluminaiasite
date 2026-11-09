# ♾️ Elumina IA - Corporate Website & Blog Engine

Site institucional e motor de blog da **Elumina IA**, projetado para atuar como o principal canal de conversão B2B da empresa. A arquitetura foi desenhada propositalmente sem o uso de frameworks pesados (Zero-Framework Approach) para garantir tempo de carregamento (TTFB) próximo a zero e máxima otimização de SEO.

## 🚀 Arquitetura e Engenharia do Projeto
Diferente das tradicionais Single Page Applications (SPAs), este projeto adota uma abordagem "Lean Web", utilizando tecnologias nativas do navegador para garantir performance extrema em redes móveis e desktops. A página atua como a porta de entrada para um ecossistema de automação interna.

### 🛠️ Core Tech Stack & Metodologia
*   **Front-end Nativo:** HTML5 semântico e JavaScript Vanilla (ECMAScript moderno).
*   **Estilização:** CSS3 puro integrado com Tailwind CSS (via `tailwind-config.js` customizado) para tipografia e responsividade fluida.
*   **Gestão de Conteúdo (Headless JSON):** O motor do blog não depende de banco de dados relacional. Os artigos são servidos e renderizados dinamicamente a partir de uma estrutura de dados estática (`blog-posts.json`), garantindo segurança e consumo zero de processamento no servidor.
*   **Captação de Leads & Alertas em Tempo Real (Tally + n8n):** O site incorpora formulários Tally para triagem B2B. Cada submissão atua como um gatilho (Webhook) que aciona um fluxo no **n8n**. O n8n processa a carga de dados (Nome, Empresa, Setor, Demanda) e dispara, via Evolution API, um alerta estruturado instantâneo (🚨 *NOVO LEAD*) diretamente no grupo de WhatsApp da equipe comercial.
*   **SEO & Automação:** Scripts de automação Node/PowerShell (`generate_sitemap.js` e `.ps1`) para geração dinâmica de sitemaps, garantindo indexação instantânea no Google.
*   **AI-Augmented Development:** Prototipagem estrutural e refatoração de componentes visuais orquestradas via Inteligência Artificial (Cursor), mantendo o foco humano na arquitetura leve e na regra de negócios da conversão B2B.

## 📂 Estrutura de Diretórios
A organização do repositório reflete a simplicidade do *Vanilla Web Development*:
*   `/assets`: Gestão de mídia estática otimizada para web.
*   `/data`: Hospeda o banco de dados em formato JSON (`blog-posts.json`), atuando como um CMS local.
*   `*.html`: Templates estáticos das páginas de destino e postagens do blog.
*   `script.js`: Lógica de injeção dinâmica de conteúdo e interatividade do DOM.

## 💡 Por que esta arquitetura?
Para uma Landing Page de conversão, a velocidade é o fator crítico. Remover o *overhead* de bibliotecas como React ou Vue permitiu criar uma página que carrega instantaneamente. A escolha por um "Blog JSON" elimina vulnerabilidades de injeção SQL, enquanto a integração com o **Tally Forms** garante que a captura de dados alimente as automações do n8n e o WhatsApp da equipe comercial sem adicionar nenhum milissegundo de peso ao carregamento do front-end.

## 🔗 Acesso ao Projeto
🌐 **Site Oficial em Produção:** [eluminaia.com](https://eluminaia.com/)
