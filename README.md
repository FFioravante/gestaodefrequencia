# Gestão de Frequência SENAI

Aplicativo web (React + Tailwind, tudo em um único arquivo HTML, sem back-end) para
apoiar o controle de frequência dos alunos do Prof. Fábio Fioravante no CT 7.90 -
SENAI "Edward Sávio".

O app lê os relatórios oficiais em PDF de "Controle de Frequência" do sistema do
SENAI (extração de texto feita no próprio navegador, com pdf.js) e calcula, por
disciplina, dois indicadores de falta:

- **Compensar**: mais de 25% de faltas sobre a carga horária total prevista (CHP).
- **Ação Preventiva**: 30% ou mais de faltas sobre as aulas já dadas até o momento.

## Funcionalidades

- Importação de múltiplos PDFs (um PDF pode conter várias disciplinas/turmas).
- Persistência local dos dados importados (localStorage) — nada é enviado a nenhum servidor.
- Filtro por turma e por disciplina (a lista de disciplinas se ajusta à turma escolhida).
- Exportação em CSV (formatado para Excel em português) para enviar à coordenação.
- Formulário de compensação de ausência pronto para impressão/PDF.
- "Ranking para Compartilhar": um relatório visual (baixável como imagem PNG) com os
  alunos de frequência exemplar (zero faltas) e os que estão em ação preventiva —
  pensado para compartilhar com a turma, por exemplo no WhatsApp.

## Uso

É um arquivo único (`index.html`) sem etapa de build. Basta abrir no navegador, ou
publicar como está em qualquer hospedagem de site estático (Netlify, GitHub Pages, etc.).

## Privacidade

Todo o processamento acontece no navegador do usuário. Nenhum dado de aluno é
enviado a servidores externos — os PDFs são lidos localmente e os dados ficam
salvos apenas no armazenamento local do navegador (localStorage).
