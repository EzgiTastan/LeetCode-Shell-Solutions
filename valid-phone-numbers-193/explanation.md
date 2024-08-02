In the 193rd question, you need to print all valid phone numbers from a text file. There exist two accepted formats: </br>
`(xxx) xxx-xxxx` or `xxx-xxx-xxxx`.

### My Solution
```
grep -P '^(\(\d{3}\) |\d{3}-)\d{3}-\d{4}$' file.txt
```

- ^: Anchors the match at the start of the line.
- (\(\d{3}\) |\d{3}-): Matches either:
- \(\d{3}\) : Three digits enclosed in parentheses followed by a space.
- \d{3}-: Three digits followed by a hyphen.
- \d{3}-: Matches exactly three digits followed by a hyphen.
- \d{4}: Matches exactly four digits.
- $: Anchors the match at the end of the line.
