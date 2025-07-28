это проэкт для написания и версирования телеграм постов
новый пост новый файл посты пишем в описаном ниже формате MarkdownV2

MarkdownV2 style
To use this mode, pass MarkdownV2 in the parse_mode field. Use the following syntax in your message:

_bold \*text_
_italic \*text_
**underline**
~strikethrough~
||spoiler||
_bold \_italic bold ~italic bold strikethrough ||italic bold strikethrough spoiler||~ **underline italic bold\_** bold_
[inline URL](http://www.example.com/)
[inline mention of a user](tg://user?id=123456789)
![👍](tg://emoji?id=5368324170671202286)
`inline fixed-width code`

```
pre-formatted fixed-width code block
```

```python
pre-formatted fixed-width code block written in the Python programming language
```

> Block quotation started
> Block quotation continued
> Block quotation continued
> Block quotation continued
> The last line of the block quotation
> \*\*>The expandable block quotation started right after the previous block quotation
> It is separated from the previous block quotation by an empty bold entity
> Expandable block quotation continued
> Hidden by default part of the expandable block quotation started
> Expandable block quotation continued
> The last line of the expandable block quotation with the expandability mark||
> Please note:

Any character with code between 1 and 126 inclusively can be escaped anywhere with a preceding '\' character, in which case it is treated as an ordinary character and not a part of the markup. This implies that '\' character usually must be escaped with a preceding '\' character.
Inside pre and code entities, all '`' and '\' characters must be escaped with a preceding '\' character.
Inside the (...) part of the inline link and custom emoji definition, all ')' and '\' must be escaped with a preceding '\' character.
In all other places characters '_', '*', '[', ']', '(', ')', '~', '`', '>', '#', '+', '-', '=', '|', '{', '}', '.', '!' must be escaped with the preceding character '\'.
In case of ambiguity between italic and underline entities ** is always greadily treated from left to right as beginning or end of an underline entity, so instead of \_**italic underline**_ use _**italic underline\_\*\*\_\_, adding an empty bold entity as a separator.
A valid emoji must be provided as an alternative value for the custom emoji. The emoji will be shown instead of the custom emoji in places where a custom emoji cannot be displayed (e.g., system notifications) or if the message is forwarded by a non-premium user. It is recommended to use the emoji from the emoji field of the custom emoji sticker.
Custom emoji entities can only be used by bots that purchased additional usernames on Fragment.
