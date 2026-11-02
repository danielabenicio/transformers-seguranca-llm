# 🛡️ Especialista em Transformers e Segurança de LLMs

Uma **Agent Skill** que transforma o Claude (e outros assistentes compatíveis) em um orientador especialista na arquitetura Transformer aplicada à **segurança de LLMs**, em **português**.

A ideia central: todo ataque ou defesa é explicado a partir do **componente do Transformer** que o torna possível, como tokenização, self-attention, contexto longo, logits, gradientes, alinhamento e representações internas.

## O que ela faz

- **Explica** conceitos indo da intuição à matemática e ao código.
- **Implementa** em PyTorch, Hugging Face e TransformerLens.
- **Analisa papers** de segurança de LLMs e mostra como reproduzi-los em PT-BR.
- **Sugere projetos** publicáveis no GitHub, com escopo e métrica de sucesso.
- **Testa seus conhecimentos** com perguntas de dificuldade crescente.

## Mapa de conteúdo

| Componente do Transformer | Exemplos de ataques | Exemplos de defesas |
|---|---|---|
| Tokenização | Ofuscação por codificação, glitch tokens | Normalização de entrada |
| Self-attention | Prompt injection | Hierarquia de instruções, spotlighting |
| Contexto longo | Many-shot jailbreaking | Limites e monitoramento de contexto |
| Gradientes | Sufixos adversariais (GCG) | Detecção por perplexidade |
| Alinhamento | Fine-tuning malicioso, backdoors | Auditoria e red teaming contínuo |
| Representações internas | Remoção da direção de recusa | Probes, circuit breakers |
| Agentes e RAG | Prompt injection indireta | Privilégio mínimo, confirmação humana |

O mapa completo, com referências, está em [`SKILL.md`](especialista-transformers-seguranca/SKILL.md).

## Como instalar

**No Claude (app ou claude.ai):** compacte a pasta `especialista-transformers-seguranca` em um `.zip` e envie em **Configurações → Capabilities → Skills**.

**No Claude Code:** copie a pasta para `~/.claude/skills/` (uso pessoal) ou para `.claude/skills/` dentro do seu projeto.

```bash
git clone https://github.com/danielabenicio/transformers-seguranca-llm.git
cp -r transformers-seguranca-llm/especialista-transformers-seguranca ~/.claude/skills/
```

## Exemplos de uso

- "Explique por que prompt injection funciona olhando para a self-attention."
- "Implemente um bloco de atenção do zero e mostre onde um sufixo adversarial atua."
- "Analise o paper do GCG e sugira como reproduzir com prompts em português."
- "Me teste sobre tokenização e ataques de ofuscação."

## Uso ético

A skill foi pensada para **estudo, pesquisa e defesa**. Ela orienta testes apenas em ambientes próprios ou autorizados, usa marcadores inofensivos para medir o sucesso de ataques e incentiva a divulgação responsável de vulnerabilidades.

## Autora

**Daniela Benicio** · [@danielabenicio](https://github.com/danielabenicio)
Cientista da Computação, com foco em Segurança de LLMs.

Contribuições são bem-vindas: abra uma issue ou um pull request.

## Licença

[MIT](LICENSE)
