![logo_do_projeto](assets/logo.png){ width="300" .center }

# Notas Musicais

## Como usar?

Você pode chamas as escalas via linha de comando, por exemplo:
```bash
poetry run escalas
```

Retornando os graus e as notas correspondentes a essa escala
```bash
┏━━━┳━━━━┳━━━━━┳━━━━┳━━━┳━━━━┳━━━━━┓
┃ I ┃ II ┃ III ┃ IV ┃ V ┃ VI ┃ VII ┃
┡━━━╇━━━━╇━━━━━╇━━━━╇━━━╇━━━━╇━━━━━┩
│ C │ D  │ E   │ F  │ G │ A  │ B   │
└───┴────┴─────┴────┴───┴────┴─────┘
```

## Alteração da tônica da escala

O primeiro parâmetro do CLI é a tônica da escala que deseja exibir. Desta forma, 
você pode alterar a escala retornada. Por exemplo, a escala de `F#`:

```bash
poetry run escalas F#
```

Resultando em:
```bash
┏━━━━┳━━━━┳━━━━━┳━━━━┳━━━━┳━━━━┳━━━━━┓
┃ I  ┃ II ┃ III ┃ IV ┃ V  ┃ VI ┃ VII ┃
┡━━━━╇━━━━╇━━━━━╇━━━━╇━━━━╇━━━━╇━━━━━┩
│ F# │ G# │ A#  │ B  │ C# │ D# │ F   │
└────┴────┴─────┴────┴────┴────┴─────┘
```

## Alteração na tonalidade da escala

Você pode alterar a tonalidade da escala também! Esse é o segundo parâmetro da linha de comando. Por exemplo, a escala de `D#` maior:

```bash
poetry run escalas D# maior
```

```
┏━━━━┳━━━━┳━━━━━┳━━━━┳━━━━┳━━━━┳━━━━━┓
┃ I  ┃ II ┃ III ┃ IV ┃ V  ┃ VI ┃ VII ┃
┡━━━━╇━━━━╇━━━━━╇━━━━╇━━━━╇━━━━╇━━━━━┩
│ D# │ F  │ G   │ G# │ A# │ C  │ D   │
└────┴────┴─────┴────┴────┴────┴─────┘
```

## Mais informações sobre o CLI

Para describrir outras opções, você pode executar a flag `--help`:

```bash
poetry run escalas --help
```

```bash
 Usage: escalas [OPTIONS] [TONICA] [TONALIDADE]                                      
                                                                                     
╭─ Arguments ───────────────────────────────────────────────────────────────────────╮
│   tonica          [TONICA]      Tônica da escala [default: c]                     │
│   tonalidade      [TONALIDADE]  Tonalidade da escala [default: maior]             │
╰───────────────────────────────────────────────────────────────────────────────────╯
```
