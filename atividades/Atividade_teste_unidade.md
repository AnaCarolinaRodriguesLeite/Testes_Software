---
title: 'Testes de Software - Atividade de testes de unidade' 
---

**Disciplina**: Testes de Software

**Professor**: Elaine Venson

**Matrícula**: 190101792

**Aluna**: Ana Carolina Rodrigues Leite

<!--
csv to markdown 
- https://blog.lent.ink/post/start-coding/
- https://stackoverflow.com/questions/41690802/convert-csv-file-contents-to-markdown
- https://github.com/mplewis/csvtomd

csvtomd conditions.csv | xclip -selection c
 -->

## Código

![image](https://user-images.githubusercontent.com/49570180/183272050-cc7bfe8b-f6a1-42c9-880a-09845f51b1b6.png)

`src/main/java/org/jabref/logic/pdf/PdfAnnotationImporter.java`

método `isSupportedAnnotationType(PDAnnotation annotation)`

Classe: `PdfAnnotationImporter`

Caminho: `src/main/java/org/jabref/logic/pdf/PdfAnnotationImporter.java`

Link: [AnaCarolinaRodriguesLeite/jabref](https://github.com/AnaCarolinaRodriguesLeite/jabref)

## Testes existentes

Testes existes estão no arquivo [`PdfAnnotationImporterTest.java`](https://github.com/AnaCarolinaRodriguesLeite/jabref/blob/main/src/test/java/org/jabref/logic/pdf/PdfAnnotationImporterTest.java).

![image](https://user-images.githubusercontent.com/49570180/183271893-5b460a55-f47c-40bf-99fd-8507f283512c.png)

![image](https://user-images.githubusercontent.com/49570180/183271906-38f598be-1bab-4020-8886-9b1dd177a6b9.png)

![image](https://user-images.githubusercontent.com/49570180/183271916-426ff048-2886-451d-9966-e590671a2cdb.png)

![image](https://user-images.githubusercontent.com/49570180/183271930-d38cf9d6-e77b-4464-a246-806e2bf12d35.png)

## Tabela de condições

<!-- 
Link da planilha:
https://docs.google.com/spreadsheets/d/14dO35E1V3v2mx9WWJAip2BABqZEFTjRo-XYvRG7nvqQ/edit#gid=1008933058
 -->

![image](https://user-images.githubusercontent.com/49570180/183304891-66496b0f-51ad-4f3a-a316-a54939a80460.png)

## Especificação dos casos de teste

| ID  | Condições cobertas | Entrada (str)               | Saída esperada |
| --- | ------------------ | --------------------------- | -------------- |
| 1   | 54.V               | `"Record..stuff..INSPEC\n"` | Falso          |
| 2   | 54.F               | `"UT INSPEC:777777\n"`      | Falso          |
| 3   | 58.1.F, 58.2.V     | Impossível                  | Falso          |
| 4   | 58.1.F, 58.2.F     | `"FA:  \n"`                 | Falso          |
| 5   | 58.1.V, 58.2.F     | `"..."`                     | Falso          |
| 6   | 58.1.V, 58.2.V     | `"TI:       \n"`            | Verdadeiro     |


Todos os casos de teste da tabela anterior cobrem a condição da linha 52, por
isso foi omitido na tabela.

A combinação 58.1.F, 58.2.V é impossível por que `str.substring(0, 5)`
não faz sentido se `str` é uma string com menos de 5 caracteres.

## Código fonte dos testes

[Link](https://github.com/yudi-azvd/jabref/blob/main/src/test/java/org/jabref/logic/importer/fileformat/MySilverPlatterImporterTest.java)
para o código no GitHub.

## Resultado dos testes

Os testes deram certo.

![Resultados dos testes](./tests-results.png)
