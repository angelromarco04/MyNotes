# Markdown Cheat Sheet

Resources:
[The Markdown Guide](https://www.markdownguide.org/cheat-sheet/)
[Basic writing and formatting syntax - GitHub Docs](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)

---

## Heading
~~~
# H1
## H2
### H3
~~~

## Bold
~~~
**bold text**
~~~

## Italic
~~~
*italicized text*
~~~

## Blockquote
~~~
> blockquote
~~~

## Ordered List
~~~
1. First item
2. Second item
3. Third item
~~~

## Unordered List
~~~
- First item
- Second item
- Third item
~~~

## Code
~~~
`code`
~~~

## Horizontal Rule
~~~
---
~~~

## Link
~~~
[Google](https://www.google.com)
~~~

## Image
~~~
![alternative text](image.png)
~~~

## Table
~~~
| Syntax | Description |
| ----------- | ----------- |
| Header | Title |
| Paragraph | Text |
~~~

## Fenced Code Block
~~~
```
{
  "firstName": "John",
  "lastName": "Smith",
  "age": 25
}
```
~~~

## Strikethrough
~~~
~~The world is flat.~~
~~~

## Task List
~~~
- [x] Completed task
- [ ] Uncompleted task
~~~

---

# Some extra notions
## Alerts

```markdown
> [!NOTE]
> Useful information that users should know, even when skimming content.

> [!TIP]
> Helpful advice for doing things better or more easily.

> [!IMPORTANT]
> Key information users need to know to achieve their goal.

> [!WARNING]
> Urgent info that needs immediate user attention to avoid problems.

> [!CAUTION]
> Advises about risks or negative outcomes of certain actions.
```

## Collapsed section

```html
<details>
<summary>Title</summary>
Content
</details>
```

```html
<details open> 
```