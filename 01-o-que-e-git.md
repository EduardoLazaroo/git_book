# Bloco 01 — O que é Git?

## Objetivo

Compreender o que é um sistema de controle de versão, por que ele foi inventado e diferenciar com clareza o que é Git e o que é GitHub.

## Conceito

Você com certeza já viveu ou viu isso acontecer com um arquivo de trabalho escolar:
- `trabalho_historia.docx`
- `trabalho_historia_final.docx`
- `trabalho_historia_final_agora_vai.docx`
- `trabalho_historia_final_corrigido_pelo_amor_de_deus.docx`

Na programação, isso se torna um desastre insustentável. Códigos têm centenas de arquivos e dezenas de programadores trabalhando ao mesmo tempo. Se alguém apagar algo por engano, como recuperar?

O **Git** é um **Sistema de Controle de Versão Distribuído** (VCS). Ele registra a história completa do seu projeto ao longo do tempo. Com ele, você sabe exatamente:
- **Quem** alterou
- **Quando** alterou
- **O que** foi alterado
- **Por que** foi alterado

E o mais importante: você pode voltar no tempo para qualquer versão funcional anterior caso faça uma bobagem!

### Git vs GitHub: Não confunda!

| Critério | Git | GitHub |
| :--- | :--- | :--- |
| **O que é?** | Ferramenta de linha de comando (software) | Serviço web / plataforma na nuvem |
| **Onde roda?** | No seu computador local (offline) | Na internet (servidores da Microsoft) |
| **Para que serve?** | Rastrear o histórico dos arquivos | Hospedar repositórios, colaborar e publicar |
| **Precisa de internet?**| Não! Funciona 100% offline | Sim, para sincronizar e navegar no site |

## Analogia

Imagine que o **Git** é uma câmera que registra fotos do seu projeto quando você manda. Cada foto recebe uma descrição e fica guardada em um álbum organizado.

O **GitHub** é o YouTube ou o Google Fotos: um lugar na nuvem onde você faz upload desses vídeos gravados para que seus amigos e colegas de equipe possam assistir, comentar e colaborar de qualquer lugar do planeta.

## Na prática

Vamos fazer um experimento mental e prático para sentir a dor que o Git resolve.

### Passo 1: Observe a pasta do seu computador

Quando alguém não usa Git, o fluxo de backup costuma ser:

```text
meu_site/
meu_site_backup_ontem/
meu_site_tentativa_menu_novo/
meu_site_quebrado_nao_mexer/
```

Isso ocupa espaço desnecessário no disco, espalha dúvidas ("qual é o arquivo mais atual?") e impede duas pessoas de trabalharem no mesmo arquivo.

### Passo 2: O jeito profissional com Git

Com o Git instalado e ativo, você tem **apenas uma única pasta limpa**:

```text
meu_site/
├── index.html
└── style.css
```

Toda a linha do tempo (passado, presente e ramificações de testes) fica guardada de forma compacta e invisível dentro de uma pasta oculta chamada `.git`.

---

## Verificação Rápida

Responda mentalmente ou anote no seu caderno:
1. O Git precisa de internet para salvar uma versão do seu código? *(Resposta: Não, ele roda 100% local no seu computador).*
2. Se o GitHub cair ou ficar fora do ar por 1 hora, você pode continuar programando e salvando versões com o Git? *(Resposta: Sim, porque o controle de versão com o Git é local).*

> Próximo passo: verifique se o Git está instalado no seu computador no [Bloco 02: Instalação e ambiente](02-instalacao-e-ambiente.md).
