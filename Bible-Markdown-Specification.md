# Bible Markdown Specification

Bible Markdown extends the Markdown syntax. For how to write in Markdown, see [Markdown Guide](https://www.markdownguide.org/basic-syntax/).

## License

Bible Markdown is licensed under the MIT-0 license. That means that it can be freely used by anyone.

## Elements

Here are the elements that are specific to Bible Markdown. They will be given as examples.

### Metadata

Metadata must be the very first paragraph in the document, it must be separated by single line breaks.

The Bible Markdown reading app should not display the metadata for the reader.

Version: World English Bible (WEB)
Publisher: eBible.org
Editor: Michael Paul Johnson
Copyright: Public Domain
Website: https://worldenglish.bible/
Description: A Public Domain modern Bible translation.

### Book names

For the name of a book of the Bible, use an H1 heading, with the abbreviation of the book in parentheses. Preferably use the standard three-letter abbreviation. Example:

    # Genesis (GEN)

The Bible Markdown reading app should display the name of the book, not the part in parentheses.

### Chapter numbers

For chapter numbers, use a number followed by a colon, followed by either a space or another number that's followed by a space. Examples:

    1: In the beginning was the Word.
    1:1 In the beginning was the Word.

Do not use the chapter number in front of each verse. That will make the text harder to read. Instead, use verse numbers as described in the next section.

Chapter numbers should be used
1. At the beginning of each chapter
2. (Optionally) at the beginning of a quotation that doesn't start with verse 1. Example: `3:16 For God so loved the world`

The Bible Markdown reading app can choose how chapter numbers are displayed, and whether the two options above are displayed the same or differently.

### Verse numbers

For verse numbers, use a number separated by spaces. You can also use two hyphenated numbers, if you're labeling a span.

    14 “You are the light of the world. A city located on a hill can’t be hidden. 15 Neither do you light a lamp and put it under a measuring basket, but on a stand; and it shines to all who are in the house. 16 Even so, let your light shine before men, that they may see your good works and glorify your Father who is in heaven.

    14 “You are the light of the world. A city located on a hill can’t be hidden. 15-16 Neither do you light a lamp and put it under a measuring basket, but on a stand; and it shines to all who are in the house. Even so, let your light shine before men, that they may see your good works and glorify your Father who is in heaven.

The Bible Markdown reading app can choose how to display verse numbers or whether to show them at all. Here is one option:

> <sup>14</sup> “You are the light of the world. A city located on a hill can’t be hidden. <sup>15</sup> Neither do you light a lamp and put it under a measuring basket, but on a stand; and it shines to all who are in the house. <sup>16</sup> Even so, let your light shine before men, that they may see your good works and glorify your Father who is in heaven.

### Numbers that aren't verse numbers

If the text contains a number, usually the number will be written out ("fifty"). However, where it needs to be written in numerals ("483"), it should be followed by a backslash: `483\`. The Bible Markdown reading app should remove the backslash.

### Line Breaks

Line breaks work as they do in normal Markdown (a single break is a new line in the same paragraph, while a double line break starts a new paragraph). Chapter and verse breaks don't need to coincide with line breaks.

The Bible Markdown reading app can choose whether to honor the paragraph breaks, or to show verses in their own line, etc.

### Additions

Some Bible translations use separate formatting for words that aren't contained in the original text, but are added for flow or clarity. Place square brackets around the added word or phrase:

   to all [those] who are in Rome in [the] love of God, appointed saints---[may] favor [be] with you and peace from God our Father and [the] Lord Jesus Christ.

The Bible Markdown reading app can choose whether and how to format this.

### Footnotes

For footnotes, put curly brackets around the word or phrase that is being expanded on. Make sure that the closing curly bracket is where you want the footnote number/letter to be placed.

    1:1 The beginning of the gospel of Jesus {Christ,} the Son of God, 2 as it is written in {the prophets:}

The footnote itself should be found below the footnoted text, maybe at the end of the paragraph or chapter. It should be formatted like the following. Note that the text in curly brackets in the footnote must exactly match the footnoted text.

    {Christ,}: or "the anointed one"
    {the prophets:}: some manuscripts "Isaiah the prophet"

The Bible Markdown reading app should
1. Remove the curly brackets from the footnoted text.
2. Place the footnote number or letter where the closing curly bracket was.
3. Remove ending punctuation from the footnote, since there might be punctuation that
4. Format footnotes as it chooses.
5. Put the footnotes in the right order and gather them to where they should be (end of page, end of document, or wherever).

Here's an example of good formatting:

> The beginning of the gospel of Jesus Christ,<sup>[a]</sup> the Son of God, <sup>2</sup>&nbsp;as it is written in the prophets:<sup>[b]</sup>
>
> -----
> [a] "Christ": or "the anointed one"
> 
> [b] "the prophets": some manuscripts "Isaiah the prophet"

### Poetry

For poetry, use a forward slash, followed by a space at the very start of each line:

    / Blessed is the man who doesn’t walk in the counsel of the wicked,
    /   nor stand on the path of sinners,
    /   nor sit in the seat of scoffers;

The Bible Markdown reading app should can format this as it chooses. If it uses poetry formatting, it should honor the white spaces between the forward slash and the text, like this:

> Blessed is the man who doesn’t walk in the counsel of the wicked,<br/>
> &nbsp;&nbsp;nor stand on the path of sinners,<br/>
> &nbsp;&nbsp;nor sit in the seat of scoffers;<br/>
