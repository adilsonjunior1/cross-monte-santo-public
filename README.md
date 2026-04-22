# 🏋️ Cross Monte Santo - Sistema de Gestão de Academia

Sistema personalizado e exclusivo desenvolvido para a **Cross Monte Santo**, voltado à gestão completa de academias de CrossFit. O projeto foi construído sob medida, atendendo às necessidades específicas do cliente, com foco em desempenho, segurança, engajamento dos alunos e praticidade na administração diária.

👉 [http://www.crossmontesanto.com.br](http://www.crossmontesanto.com.br)

⚠️ **Atenção:** Este é um sistema proprietário desenvolvido sob contrato. O código, design e funcionalidades não devem ser reproduzidos, redistribuídos ou utilizados sem autorização expressa do desenvolvedor.

---

## ✨ Principais Funcionalidades

### 👨‍🎓 Área do Aluno

* Login simplificado via **CPF** (sem senha), com sessão persistente
* Dashboard personalizado com **status do plano** e contagem regressiva de vencimento (banner ≤ 15 dias)
* Acesso ao **Treino do Dia (WOD)** publicado pela academia
* **Check-in por QR Code** fixo na unidade (1 presença por dia)
* **Meus PRs** — registro e histórico dos 6 movimentos fundamentais (Snatch, Clean, Jerk, Back Squat, Front Squat, Deadlift)
* **Ranking de Presença** com ciclos, prêmios e quadro de campeões
* **Avisos da academia** com marcação de leitura
* **Compartilhamento do treino** como card de imagem para redes sociais
* **Mensagens motivacionais diárias** personalizadas
* **Foto de perfil** com upload e ajuste (mover + zoom)
* Notificações automáticas de vencimento

### 👨‍💼 Área Administrativa

* CRUD completo de **alunos**, **treinos**, **horários**, **avisos** e **administradores**
* **Status automático de matrícula** (Aprovado, Pendente, Vencido) — atualizado por cron e em tempo real
* **Status de engajamento do aluno** (🟢 Engajado · 🟡 Regular · 🔴 Em risco) calculado pelos check-ins dos últimos 30 dias
* Criação e edição de treinos diários, com **histórico organizado** (últimos 6 dias + arquivo)
* Agendamento e gestão de aulas com **capacidade máxima**
* **Visualização de check-ins em tempo real**
* **Aba Financeiro** — receita por regime de caixa, despesas, lucro e indicadores
* **Aba Frequência** — visualização dos check-ins por dia
* **Aba Metas** — acompanhamento de objetivos da academia
* **Gerenciador de Ranking** — abertura, encerramento e premiação de ciclos
* **Dashboard interativo** com cards-filtro
* Cadastro e gerenciamento de administradores
* Interface 100% responsiva (desktop e mobile)

---

## 🛠️ Stack Tecnológica

### Frontend

* **React 18 + TypeScript 5**
* **Vite 5**
* **Tailwind CSS 3**
* **shadcn/ui + Radix UI**
* **React Router DOM 6**
* **TanStack Query**
* **Lucide React**
* **React Hook Form + Zod**
* **date-fns**
* **Recharts**
* **html5-qrcode + qrcode.react**
* **Sonner**

### Backend

* **Supabase** (PostgreSQL, Auth, Storage, Edge Functions, RLS)

**Edge Functions:**

* `student-login`
* `create-admin`
* `delete-users`

**Funções SQL:** `qr_checkin`, `update_expired_students`, `update_student_avatar`, `has_role`

* **Cron Job** para atualização de planos vencidos

---

## ⚡ Progressive Web App (PWA)

O sistema foi desenvolvido como um PWA (Progressive Web App), oferecendo:

* Instalação direta no dispositivo (Android, iOS, Desktop)
* Carregamento rápido com estratégia de cache
* Atualização automática com aviso de nova versão
* Manifest e Service Worker configurados

💡 Permite uso como aplicativo nativo diretamente da tela inicial.

---

## 🗄️ Estrutura do Banco de Dados

Principais tabelas:

* `students`
* `workouts`
* `class_schedules`
* `class_checkins`
* `student_prs`
* `student_progress`
* `student_goals`
* `announcements` / `announcement_reads`
* `attendance_rankings` / `ranking_champions`
* `expenses`
* `goals`
* `user_roles`
* `profiles`

**Storage:** `student-avatars`

**Segurança:** Row Level Security (RLS) em todas as tabelas

---

## 🔐 Autenticação

* **Alunos:** login via CPF com sessão persistente
* **Administradores:** login com e-mail e senha
* Controle de acesso baseado em roles (`user_roles`)
* Validação de CPF no cadastro

---

## 📱 Responsividade

Compatível com:

* 📱 Mobile
* 💻 Tablet
* 🖥️ Desktop

---

## 💰 Planos Suportados

* 6× por semana
* 3× por semana
* 2× por semana

Controle financeiro baseado em **regime de caixa**.

---

## 📦 Deploy

Hospedado na Vercel com deploy contínuo:
👉 [https://cross-monte-santo-app-uyj2.vercel.app/](https://cross-monte-santo-app-uyj2.vercel.app/)

---

## 🧩 Arquitetura e Manutenção

* Estrutura modular e escalável
* Componentização reutilizável
* Tipagem com TypeScript
* Edge Functions para operações sensíveis
* Integração contínua com GitHub e Vercel

---

## 🧠 Observações Importantes

* Sistema **proprietário**
* Uso exclusivo da Cross Monte Santo
* Reprodução ou redistribuição não permitidas
* Projetos similares sob demanda

---

## 👨‍💻 Desenvolvedor

**Adilson Júnior - Klyven Solutions**
