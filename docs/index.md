![logo_do_projeto](assets/logo.png){ width="300" .center }

# Notas Musicais

Notas musicais é um CLI para ajudar na formação de escalas e acordes.

Temos dois comandos disponíveis: `escala` e `acorde`

## Como usar?

### Escalas

Você pode chamas as escalas via linha de comando, por exemplo:
```bash
poetry run notas-musicais escala
```

Retornando os graus e as notas correspondentes a essa escala
```bash
┏━━━┳━━━━┳━━━━━┳━━━━┳━━━┳━━━━┳━━━━━┓
┃ I ┃ II ┃ III ┃ IV ┃ V ┃ VI ┃ VII ┃
┡━━━╇━━━━╇━━━━━╇━━━━╇━━━╇━━━━╇━━━━━┩
│ C │ D  │ E   │ F  │ G │ A  │ B   │
└───┴────┴─────┴────┴───┴────┴─────┘
```

#### Alteração da tônica da escala

O primeiro parâmetro do CLI é a tônica da escala que deseja exibir. Desta forma, 
você pode alterar a escala retornada. Por exemplo, a escala de `F#`:

```bash
poetry run notas-musicais escala F#
```

Resultando em:
```bash
┏━━━━┳━━━━┳━━━━━┳━━━━┳━━━━┳━━━━┳━━━━━┓
┃ I  ┃ II ┃ III ┃ IV ┃ V  ┃ VI ┃ VII ┃
┡━━━━╇━━━━╇━━━━━╇━━━━╇━━━━╇━━━━╇━━━━━┩
│ F# │ G# │ A#  │ B  │ C# │ D# │ F   │
└────┴────┴─────┴────┴────┴────┴─────┘
```

#### Alteração na tonalidade da escala

Você pode alterar a tonalidade da escala também! Esse é o segundo parâmetro da linha de comando. Por exemplo, a escala de `D#` maior:

```bash
poetry run notas-musicais escala D# menor
```

```
┏━━━━┳━━━━┳━━━━━┳━━━━┳━━━━┳━━━━┳━━━━━┓
┃ I  ┃ II ┃ III ┃ IV ┃ V  ┃ VI ┃ VII ┃
┡━━━━╇━━━━╇━━━━━╇━━━━╇━━━━╇━━━━╇━━━━━┩
│ D# │ F  │ F#  │ G# │ A# │ B  │ C#  │
└────┴────┴─────┴────┴────┴────┴─────┘
```

## Acordes

Uso básico

```bash
poetry run notas-musicais acorde
┏━━━┳━━━━━┳━━━┓
┃ I ┃ III ┃ V ┃
┡━━━╇━━━━━╇━━━┩
│ C │ E   │ G │
└───┴─────┴───┘
```

### Variações na cifra

```bash
poetry run notas-musicais acorde C+
┏━━━┳━━━━━┳━━━━┓
┃ I ┃ III ┃ V+ ┃
┡━━━╇━━━━━╇━━━━┩
│ C │ E   │ G# │
└───┴─────┴────┘
```

Até o momento você pode usar acordes maiores, menores, diminuto e aumentados.

## Mais informações sobre o CLI

Para describrir outras opções, você pode executar a flag `--help`:

```bash
poetry run notas-musicais --help
```

```bash
 Usage: escalas [OPTIONS] [TONICA] [TONALIDADE]                                      
                                                                                     
╭─ Arguments ───────────────────────────────────────────────────────────────────────╮
│   tonica          [TONICA]      Tônica da escala [default: c]                     │
│   tonalidade      [TONALIDADE]  Tonalidade da escala [default: maior]             │
╰───────────────────────────────────────────────────────────────────────────────────╯
```
