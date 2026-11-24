# L1 Patches (Português BR)

Bundle personalizado para **Morphe Manager / Morphe Desktop**, focado no **Prime Video Android TV**.

## Versão compatível e recomendada

**Somente `6.24.13+v16.0.1.93-allAbis`**, pacote `com.amazon.amazonvideo.livingroom`.

Todos os sete patches publicados em `patches-list.json` declaram exclusivamente essa versão. Versões antigas como `6.24.7` e `6.23.23` não são suportadas por esta fonte. O Morphe calcula a indicação **Recomendado** a partir da compatibilidade dos patches; não existe uma opção independente neste repositório para forçar essa etiqueta.

## Adicionar e atualizar no Morphe Manager

**Recomendado: adicionar pelo endereço do repositório**, para permitir que o Morphe acompanhe as atualizações da fonte:

```text
https://github.com/HeliumMarcos/L1-Patches
```

Também é possível usar diretamente os metadados:

```text
https://raw.githubusercontent.com/HeliumMarcos/L1-Patches/main/patches-bundle.json
```

1. Abra **Fontes de patches** → **Adicionar fonte** e informe o endereço.
2. Em atualizações futuras, use **Atualizar** no cartão da fonte.
3. Se ainda aparecerem versões removidas, confirme que a fonte baixou o bundle atualizado. Se necessário, remova e adicione novamente a fonte para reconstruir os dados locais.

## Regra obrigatória de versionamento

**Toda modificação publicada deve gerar uma nova versão, sem reutilizar a versão anterior.** Isso inclui alterações em patches, compatibilidade, código-fonte, metadados e documentação. Para mudanças que afetam o bundle, o lançamento só está concluído quando todos os itens abaixo estiverem sincronizados:

1. Incrementar a versão (por exemplo, `v1.61.1` → `v1.61.2`); nunca sobrescrever uma release anterior.
2. Recompilar e verificar o arquivo `.mpp` quando houver alterações que afetem o bundle.
3. Publicar uma nova GitHub Release com o artefato correspondente.
4. Atualizar juntos `version`, `download_url` e a descrição de `patches-bundle.json`.
5. Atualizar o README e conferir que a versão anunciada coincide com a release e o arquivo baixado.
6. Testar a atualização no Morphe Manager, inclusive se versões removidas deixam de ser oferecidas.

Para mudanças exclusivamente documentais, incrementar a versão documental ou registrar um novo release de manutenção conforme o processo adotado, sem alegar que um bundle foi recompilado quando não foi. **Nunca apontar os metadados para um arquivo de release inexistente.** Um commit isolado não publica automaticamente uma nova release; essa sequência precisa ser executada em cada atualização.

**Importante:** a lista de versões é derivada do bundle `.mpp` efetivamente carregado. Alterar apenas `patches-list.json`, `README.md` ou a descrição do JSON não substitui o conteúdo de um bundle já instalado. Ao alterar a compatibilidade dos patches, é necessário **recompilar o `.mpp` e publicar uma nova release**, atualizando `version` e `download_url` em `patches-bundle.json`. Não reutilize o mesmo número de versão para bundles diferentes.

O cache, os APKs salvos e o comportamento de atualização pertencem ao Morphe Manager. Este repositório não pode apagá-los nem obrigar o gerenciador a invalidar versões antigas. A fonte **TV Morphe Patches** pode ter patches sobrepostos; evite combinar patches conflitantes.

## Bundle atual (`v1.61.1`)

- **Correção de travamento em anúncios mid-roll:** hook nativo `libpvhook.so` (`armeabi-v7a`) com endereço `chapteringAdBreak` `0x00dc6450`.
- **Force highest quality:** incluído como patch experimental, desmarcado por padrão.
- **Override certificate pinning:** removido do bundle.

## Créditos e licença

Baseado em [ajstrick81/morphe-androidtv-patches](https://github.com/ajstrick81/morphe-androidtv-patches) e [semicoloncolonel/tv-morphe-patches](https://github.com/semicoloncolonel/tv-morphe-patches).

Licença **GPLv3**.
