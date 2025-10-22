# 🏋️ Cross Monte Santo - Sistema de Gestão de Academia

Sistema **personalizado e exclusivo** desenvolvido para a **Cross Monte Santo**, voltado à gestão completa de academias de CrossFit.
O projeto foi construído sob medida, atendendo às necessidades específicas do cliente, com foco em desempenho, segurança e praticidade na administração diária.

👉 [http://www.crossmontesanto.com.br](http://www.crossmontesanto.com.br)

> ⚠️ **Atenção:** Este é um sistema proprietário desenvolvido sob contrato.
> O código, design e funcionalidades **não devem ser reproduzidos, redistribuídos ou utilizados** sem autorização expressa do desenvolvedor.

---

## ✨ Principais Funcionalidades

### 👨‍🎓 Área do Aluno

* Login via CPF (sem senha)
* Dashboard personalizado com status de pagamento
* Acesso ao **Treino do Dia (WOD)**
* Sistema de **check-in** em aulas com controle de vagas
* Registro e histórico de **PRs (recordes pessoais)**
* Notificações automáticas de vencimento

### 👨‍💼 Área Administrativa

* CRUD completo de alunos e treinos
* Controle de status de matrícula (Ativo, Pendente, Vencido)
* Criação e edição de treinos diários
* Agendamento e gestão de aulas com capacidade máxima
* Visualização de check-ins em tempo real
* Cadastro e gerenciamento de administradores
* Dashboard interativo e responsivo (desktop e mobile)

---

## 🛠️ Stack Tecnológica

### Frontend

* **React 18 + TypeScript**
* **Vite** – Build e Dev Server rápido
* **Tailwind CSS** – Estilização moderna
* **shadcn/ui** + **Radix UI** – Componentização acessível
* **React Router DOM** – Roteamento
* **Lucide React** – Ícones otimizados
* **React Hook Form + Zod** – Validação de formulários
* **date-fns** – Manipulação de datas
* **Sonner** – Sistema de notificações

### Backend

* **Supabase** (PostgreSQL, Auth, Edge Functions, RLS)
* **Edge Functions** personalizadas:

  * `student-login`
  * `create-admin`
  * `delete-users`

### Infraestrutura

* **Vercel** – Deploy e CI/CD
* **GitHub** – Versionamento

---

### ⚡ Progressive Web App (PWA)

* O sistema foi desenvolvido como um PWA (Progressive Web App), oferecendo:

* Instalação direta no dispositivo (Android, iOS, Desktop)

* Acesso offline a funcionalidades essenciais

* Carregamento rápido com cache inteligente

* Ícones otimizados (192x192 e 512x512)

* Manifest e Service Worker configurados

💡 Permite que a academia e os alunos acessem o sistema como se fosse um aplicativo nativo, diretamente da tela inicial do celular.

---

## 🗄️ Estrutura do Banco de Dados

Principais tabelas:

* `students` – Alunos (nome, CPF, status, plano, vencimento)
* `workouts` – Treinos do dia
* `class_schedules` – Horários de aulas
* `class_checkins` – Check-ins de presença
* `student_prs` – Recordes pessoais
* `user_roles` – Permissões (admin/aluno)

**Segurança:**
Todas as tabelas utilizam **Row Level Security (RLS)** para garantir acesso restrito e seguro aos dados.

---

## 🔐 Autenticação

* **Alunos:** via CPF (Edge Function `student-login`)
* **Administradores:** via Supabase Auth (e-mail e senha)
* Controle de acesso baseado em **roles** e políticas de segurança

---

## 📱 Responsividade

Interface totalmente responsiva, otimizada para:

* 📱 Mobile
* 💻 Tablet
* 🖥️ Desktop

---

## 📦 Deploy

O sistema está hospedado na Vercel com deploy contínuo.
Ambiente de produção:
👉 [https://cross-monte-santo-app-uyj2.vercel.app/](https://cross-monte-santo-app-uyj2.vercel.app/)

---

## 🧩 Arquitetura e Manutenção

* Estrutura modular e escalável
* Padrão de componentes reutilizáveis
* Tipagem estática com TypeScript
* Edge Functions isoladas para segurança
* Integração contínua via GitHub e Vercel

---

## 🧠 Observações Importantes

* Este sistema **não é open source**.
* O código é de uso **exclusivo do cliente Cross Monte Santo**.
* A reprodução, modificação ou redistribuição **não são permitidas**.
* Caso queira desenvolver um sistema semelhante, entre em contato para um projeto **personalizado e licenciado**.

---

## 👨‍💻 Desenvolvedor

Desenvolvido por **Adilson Júnior**
