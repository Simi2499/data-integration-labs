<!--
| Group | Features |
| --- | --- |
| Text | headings · paragraphs and line breaks · italic, bold and both · strikethrough · inline code · escaping a character such as `*` |
| Lists | unordered, ordered and nested lists · task lists |
| Links and images | inline and reference-style links · a relative link to another file in your repository · a link to a section · an image with alt text · an image that is a link |
| Code | fenced code blocks with syntax highlighting for Python, Bash and JSON |
| Quotes | blockquotes, nested and with formatting · alerts, like the boxes in this lab |
| Tables | a table with aligned columns, and a cell that contains a link or a `\|` |
| Layout | horizontal rules · collapsed sections, like the hints in this lab · comments that do not render |
| GitHub extras | footnotes · emoji shortcodes · @mentions and references to issues · a Mermaid diagram · a formula |


### Strikethrough

**GitHub** · Two tildes on each side cross text out.

```markdown
~~no longer true~~
```

~~no longer true~~
-->

# Markdown Cheat Sheet

## Contents

- [Text](#text)
- [Lists](#lists)
- [Links and images](#links-and-images)
- [Code](#code)
- [Quotes](#quotes)
- [Tables](#tables)
- [Layout](#layout)
- [GitHub extras](#github-extras)
- [Pitfalls](#pitfalls)

## Text

| Feature       | Einordnung | Beispiel beziehungsweise Hinweis                                              |
| ------------- | ---------- | ----------------------------------------------------------------------------- |
| Headings      | CommonMark | # Heading, ## Heading, ### Heading                                            |
| Paragraphs    | CommonMark | Absätze mit einer Leerzeile trennen.                                          |
| Line breaks   | CommonMark | Für einen erzwungenen Umbruch eine Zeile mit \\ oder zwei Leerzeichen beenden. |
| Italic        | CommonMark | *italic*                                                                      |
| Bold          | CommonMark | **bold**                                                                      |
| Both          | CommonMark | ***bold and italic***                                                         |
| Strikethrough | GitHub     | ~~deleted~~                                                                   |
| Inline code   | CommonMark | `print("Hello")`                                                              |
| Escaping      | CommonMark | \\* zeigt ein wörtliches Sternchen.                                           |

Die Standardfunktionen sind in CommonMark beschrieben; GitHub ergänzt unter anderem durchgestrichenen Text. Bei normalen Zeilenumbrüchen unterscheidet GitHub außerdem zwischen .md-Dateien und beispielsweise Issue-Kommentaren.

## Lists

| Feature         | Einordnung | Beispiel beziehungsweise Hinweis                                    |
| --------------- | ---------- | ------------------------------------------------------------------- |
| Unordered lists | CommonMark | - Item                                                              |
| Ordered lists   | CommonMark | 1. Item                                                             |
| Nested lists    | CommonMark | Unterpunkte passend zum Text des übergeordneten Eintrags einrücken. |
| Task lists      | GitHub     | - [ ] Open und - [x] Done                                           |  

Die Listenstruktur gehört zum Standard; die Darstellung von Checkboxen ist eine GitHub-Erweiterung.

## Links and images

| Feature              | Einordnung                                                    | Beispiel beziehungsweise Hinweis                               |
| -------------------- | ------------------------------------------------------------- | -------------------------------------------------------------- |
| Inline link          | CommonMark                                                    | [GitHub](https://github.com)                                   |
| Reference-style link | CommonMark                                                    | [GitHub][gh] mit separater Definition [gh]: https://github.com |
| Relative link        | CommonMark                                                    | [README](../../README.md)                                      |
| Link to a section    | GitHub, wenn du automatisch erzeugte Überschriftenanker nutzt | [Code](#code)                                                  |
| Image with alt text  | CommonMark                                                    | ![Beschreibung](bild.png)                                      |
| Image that is a link | CommonMark                                                    | [![Beschreibung](bild.png)](https://github.com)                |  \

Beim Abschnittslink ist die Unterscheidung besonders wichtig: Die Linksytnax [...](#...) ist CommonMark; dass eine Überschrift automatisch ein passendes Ziel erhält, ist es nicht. 

## Code

| Feature                    | Einordnung | Hinweis                                             |
| -------------------------- | ---------- | --------------------------------------------------- |
| Fenced code block          | CommonMark | Drei Backticks öffnen und schließen den Block.      |
| Python syntax highlighting | GitHub     | Sprachangabe python hinter den öffnenden Backticks. |
| Bash syntax highlighting   | GitHub     | Sprachangabe bash.                                  |
| JSON syntax highlighting   | GitHub     | Sprachangabe json.                                  |

## Quotes

| Feature                       | Einordnung | Beispiel beziehungsweise Hinweis                                    |
| ----------------------------- | ---------- | ------------------------------------------------------------------- |
| Blockquote                    | CommonMark | > Quote                                                             |
| Nested blockquote             | CommonMark | > > Nested quote                                                    |
| Formatting inside blockquotes | CommonMark | Zum Beispiel Kursivschrift oder Inline-Code innerhalb eines Zitats. |
| Alerts                        | GitHub     | Zum Beispiel > [!NOTE] mit weiteren Zitatzeilen.                    |  \

Ein Alert verwendet zwar die Zitatsyntax, aber die besondere Darstellung als Hinweisbox ist eine GitHub-Erweiterung.

## Tables

| Feature                    | Einordnung                       | Hinweis                                               |
| -------------------------- | -------------------------------- | ----------------------------------------------------- |
| Table with aligned columns | GitHub                           | Ausrichtung mit :---, :---: und ---:.                 |
| Link inside a cell         | GitHub für die Tabelle insgesamt | Innerhalb der Zelle normale Linksyntax verwenden.     |
| Literal \\\| inside a cell | GitHub für die Tabelle insgesamt | Den senkrechten Strich mit einem Backslash maskieren. |

## Layout

| Feature           | Einordnung                                             | Hinweis                                                               |
| ----------------- | ------------------------------------------------------ | --------------------------------------------------------------------- |
| Horizontal rule   | CommonMark                                             | Zum Beispiel ---, am besten durch Leerzeilen vom Text getrennt.       |
| Collapsed section | CommonMark über eingebettetes HTML; Darstellung prüfen | <details> und <summary> sind HTML, keine eigene Markdown-Erweiterung. |
| Hidden comments   | CommonMark über eingebettetes HTML                     | <!-- Kommentar -->                                                    |

## GitHub extras

| Feature          | Einordnung              | Beispiel beziehungsweise Hinweis                         |
| ---------------- | ----------------------- | -------------------------------------------------------- |
| Footnotes        | GitHub                  | Text[^note] mit separater Definition [^note]: Erklärung. |
| Emoji shortcodes | GitHub                  | :smile:                                                  |
| @mentions        | GitHub, kontextabhängig | Einen tatsächlichen GitHub-Benutzernamen verwenden.      |
| Issue references | GitHub, kontextabhängig | Eine existierende Issue-Nummer wie #1 verwenden.         |
| Mermaid diagram  | GitHub                  | Codeblock mit Sprachangabe mermaid.                      |
| Formula          | GitHub                  | Beispielsweise ein Codeblock mit Sprachangabe math.      |

## Pitfalls

+ Einfacher Zeilenumbruch wurde in der .md-Datei nicht als sichtbarer Umbruch angezeigt. Lösung: Backslah am Zeilenende oder eine Leerzeile für einen neuen Absatz verwenden.
