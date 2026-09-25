# 🔁 Cadastro de Notas — For e While

![Python](https://img.shields.io/badge/Python-3.x-3776AB?logo=python&logoColor=white)
![Status](https://img.shields.io/badge/status-conclu%C3%ADdo-2F6F6B)
![Tema](https://img.shields.io/badge/tema-estrutura%20de%20repeti%C3%A7%C3%A3o-8A5A2B)
![License](https://img.shields.io/badge/license-MIT-lightgrey)
![Claude](https://img.shields.io/badge/claude-%23D97757.svg?style=for-the-badge&logo=claude&logoColor=white)

Programa em Python que registra a nota de vários alunos, combinando duas estruturas de repetição: **for** (para percorrer a lista de alunos) e **while** (para validar cada nota digitada).

## 📋 O que o programa faz

- Pede a nota de cada aluno de uma turma.
- Não aceita notas fora do intervalo de 0 a 10 — se o valor digitado for inválido, o programa pede novamente até receber um valor correto.
- Ao final, exibe todas as notas registradas e a média da turma.

## 💻 Código

```python
quantidade_alunos = 5
notas = []

for aluno in range(1, quantidade_alunos + 1):
    nota = float(input(f"Digite a nota do aluno {aluno}: "))

    while nota < 0 or nota > 10:
        print("Nota inválida! Digite um valor entre 0 e 10.")
        nota = float(input(f"Digite a nota do aluno {aluno}: "))

    notas.append(nota)

print("\nNotas registradas:", notas)
print("Média da turma:", sum(notas) / len(notas))
```

## 🔍 Por que for e while juntos

| Estrutura | Papel no programa |
|---|---|
| 🔢 `for` | Controla o que já se sabe de antemão: são exatamente `quantidade_alunos` alunos, um após o outro. |
| ⏳ `while` | Controla o que não se sabe de antemão: quantas vezes será necessário pedir a nota novamente até que um valor válido seja digitado. |

O `for` decide **quantas vezes** o processo geral se repete. O `while`, dentro dele, garante **a qualidade de cada repetição individual**.

## ▶️ Como executar

Pré-requisito: Python 3 instalado.

```bash
python cadastro_notas.py
```

## 🖥️ Exemplo de execução

```
Digite a nota do aluno 1: 8.5
Digite a nota do aluno 2: 15
Nota inválida! Digite um valor entre 0 e 10.
Digite a nota do aluno 2: 7
Digite a nota do aluno 3: 9
Digite a nota do aluno 4: -2
Nota inválida! Digite um valor entre 0 e 10.
Digite a nota do aluno 4: 6
Digite a nota do aluno 5: 10

Notas registradas: [8.5, 7.0, 9.0, 6.0, 10.0]
Média da turma: 8.1
```

---

📚 Desenvolvimento de Sistemas I · Agenda 08 — Estrutura de Repetição
