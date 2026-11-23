# 🎓 RPG: Sobrevivência Acadêmica

Projeto Avaliativo Integrador desenvolvido para as disciplinas de Programação Orientada a Objetos, Banco de Dados e Sistemas Operacionais/Git (IFTO - Campus Pedro Afonso)[cite: 1, 2].

## 👥 Integrantes e Divisão Inicial de Papéis
* **Biel:** Desenvolvimento / POO (Classes, regras do jogo e Game Loop)[cite: 3]
* **Kaique:** Banco de Dados (Modelagem, scripts DDL/DML e persistência)[cite: 3]
* **Luis:** Versionamento / Qualidade (Gestão Git/GitHub, testes e documentação)[cite: 3]

*(Nota: Os papéis serão rotacionados após o Checkpoint 2 conforme diretriz do projeto[cite: 3, 6]).*

## 📖 Objetivo e Mecânica do Jogo
O jogador assume o papel de um estudante tentando sobreviver ao semestre letivo enfrentando desafios acadêmicos em combate por turnos[cite: 2].

* **Classes Jogáveis:**
  * **Nerd do Café:** Alto dano lógico com gasto de recursos[cite: 3].
  * **Procrastinador Sortudo:** Alta chance de acerto crítico de última hora[cite: 3].
  * **Líder de Grupo:** Alta resistência mental e redução de estresse[cite: 3].
* **Mecânica Autoral (Medidor de Estresse e Cafeína):** Habilidades especiais aumentam o nível de estresse (0 a 100)[cite: 6]. Ao atingir 100, o personagem sofre *Burnout* e perde um turno[cite: 6]. O jogador possui doses limitadas de **Café Expresso** para reduzir o estresse e recuperar energia mental[cite: 6].

## 🏛️ Arquitetura de Classes (POO)
* `EntidadeAcademica` (Classe Abstrata): Define atributos encapsulados (`nome`, `energiaAtual`, `foco`) e métodos base[cite: 3].
* `Estudante` / Subclasses: Implementam polimorfismo no método `executarAcao()`[cite: 3].
* `DesafioAcademico`: Representa os inimigos armazenados em `ArrayList`[cite: 2, 4].
* `Main`: Controla o *Game Loop* principal e a integração com o banco.

## 🗄️ Como Preparar o Banco de Dados
1. Certifique-se de ter um SGBD relacional instalado (ex: MySQL / MariaDB).
2. Execute o script `sql/01_criacao.sql` para criar o banco e as tabelas (`estudante`, `desafio_academico`, `historico_aprovacao`)[cite: 6, 7].
3. Execute o script `sql/02_dados_iniciais.sql` para popular os inimigos e o perfil de teste[cite: 6, 7].

## ▶️ Como Executar o Jogo
*(Em desenvolvimento — instruções de compilação e driver JDBC serão adicionadas no Checkpoint 4[cite: 4, 5, 6]).*

## 🧪 Testes de Aceitação
| ID | Teste | Status |
| :--- | :--- | :--- |
| T01 | Iniciar o jogo | Pendente[cite: 7] |
| T02 | Aplicar dano maior que a vida (não ficar negativo) | Pendente[cite: 7] |
| T03 | Polimorfismo entre classes distintas | Pendente[cite: 7] |
| T04 | Eliminar inimigo e atualizar coleção (`ArrayList`) | Pendente[cite: 7] |
| T05 | Eliminar todos os inimigos (Vitória) | Pendente[cite: 7] |
| T06 | Energia chega a zero (Derrota) | Pendente[cite: 7] |
| T07 | Salvar estado no banco | Pendente[cite: 7] |
| T08 | Recuperar estado do banco | Pendente[cite: 7] |
| T09 | Executar scripts SQL em ambiente limpo | Em validação[cite: 7] |
| T10 | Clonar e preparar em outro computador | Pendente[cite: 7] |

## ⚠️ Limitações Conhecidas e Melhorias Futuras
* Interface baseada em console (terminal)[cite: 2, 6].
* Futura implementação de sistema de equipamentos (ex: Notebook Gamer, Fone com Cancelamento de Ruído)[cite: 6].
