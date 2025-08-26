SIte de agendamento de horários
Modifique os titulos de acordo com sua necessidade
Permite que responsáveis escolham turma e horário disponíveis, com controle de ocupação em tempo real via Firestore.

✨ Funcionalidades

Formulário responsivo (HTML + CSS + JS).

Lista de turmas pré-definidas.

Horários de manhã/tarde atribuídos automaticamente conforme a turma.

Bloqueio visual de horários já ocupados.

Registro no Cloud Firestore.

🧱 Tecnologias

HTML5 / CSS3 / JavaScript (ES Modules)

Firebase Web SDK (Firestore)

🗃️ Estrutura de Dados (Firestore)

Coleção: agendamentos
Campos:

nome → Nome do responsável

aluno → Nome do aluno

turma → Ex.: 2º ano MA

horario → Ex.: 07:10

(recomendado) dataEvento + createdAt

▶️ Uso

Abra index.html em um navegador moderno.

Se abrir direto não funcionar, use um servidor local (python -m http.server 8080).

Selecione turma → escolha horário disponível → clique em Agendar.

⚠️ Observações Importantes

Hoje o bloqueio de horários é apenas visual. Para evitar agendamentos duplicados simultâneos, recomenda-se:

Usar transação no Firestore.

Adicionar campo dataEvento e regras de segurança que impeçam duplicidade (turma+horario+dataEvento).

Adicione createdAt: serverTimestamp() para auditoria.

Defina regras no Firestore para permitir somente criação e bloquear edição/remoção no cliente.

🚀 Deploy

Funciona em qualquer serviço de páginas estáticas:

GitHub Pages

Netlify

Vercel
