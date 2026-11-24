# L1 Patches (Português BR)

Bundle personalizado de patches para o **Morphe Manager / Morphe Desktop**, unificando as correções de anúncios e vídeo para **Prime Video Android TV** (em especial `6.24.13+v16.0.1.93-allAbis`).

## Como adicionar no Morphe Manager / Morphe Desktop

1. Abra o **Morphe Manager** (ou **Morphe Desktop**).
2. Vá em **Fontes de Patches** (*Patch Sources*) → **Adicionar fonte**.
3. Cole a URL abaixo:

```text
https://raw.githubusercontent.com/HeliumMarcos/L1-Patches/main/patches-bundle.json
```

*(Desative o `TV Morphe Patches` antigo se estiver ativo para evitar conflito com `Skip ads`.)*

## O que foi alterado neste bundle (`v1.61.1`)

- **Correção de travamento em anúncios (*mid-roll* na `6.24.13`):** atualizado o hook nativo `libpvhook.so` (`armeabi-v7a`) com o endereço correto do parser `chapteringAdBreak` (`0x00dc6450`), evitando que o player trave em carregamento infinito ao chegar em um intervalo de anúncio.
- **`Force highest quality` incluído:** integrado diretamente no mesmo bundle (sem conflito de `Skip ads`).
- **`Override certificate pinning` removido:** mantido fora do bundle para uma lista mais limpa e segura.

## Créditos e Licença

- Baseado em [ajstrick81/morphe-androidtv-patches](https://github.com/ajstrick81/morphe-androidtv-patches) e [semicoloncolonel/tv-morphe-patches](https://github.com/semicoloncolonel/tv-morphe-patches).
- Licenciado sob **GPLv3**.
