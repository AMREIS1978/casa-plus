# Bomba Certa v3.9 — preços imediatos, validação e denúncias

## Nova regra de preços
Qualquer utilizador pode comunicar um preço.

Assim que o comunica:
- o preço passa imediatamente a ser mostrado no posto;
- não depende do nível/status;
- fica visível quem o comunicou e o respetivo nível;
- aparece a data/hora da atualização.

O preço oficial DGEG continua disponível como referência de origem quando não existe uma comunicação comunitária mais recente.

## Validação
Outros utilizadores podem:
- **Confirmar** o preço;
- marcar como **Incorreto**.

O próprio autor não pode validar o seu próprio preço.

### Pontos
- comunicar preço: não atribui pontos imediatamente;
- confirmação: o autor do preço recebe **+5 pontos**;
- rejeição: o autor perde **5 pontos** (sem descer abaixo de zero);
- quem valida corretamente continua a receber pontos pela participação.

Cada utilizador só pode votar uma vez por comunicação.

## Denunciar utilizador
Junto de um preço comunicado por outra pessoa surge:
- `🚩 Denunciar`

Motivos:
- preço falso ou enganador;
- spam / alterações repetidas;
- comportamento abusivo;
- outro.

A denúncia fica ligada:
- ao utilizador;
- ao preço concreto;
- ao posto;
- ao combustível;
- à data;
- ao denunciante.

## Administração
Nova área:
**Denúncias de utilizadores**

O administrador vê:
- utilizador denunciado;
- email;
- denunciante;
- motivo;
- detalhes;
- posto;
- combustível;
- preço;
- data;
- estado.

Estados:
- Pendente
- Revista
- Arquivada

## Integridade
A denúncia é criada por uma função segura no backend que determina automaticamente o verdadeiro autor do preço. Não é possível indicar arbitrariamente outro utilizador como alvo.
