This project [publishes the TEI encoding](https://gofilipa.github.io/dorian_encoded/) of the first chapter of Oscar Wilde's manuscript, *The Picture of Dorian Gray* (1890). 

This project uses [ceTEIcean](https://github.com/TEIC/CETEIcean) 

See the [full manuscript of *Dorian Gray*](https://www.themorgan.org/collection/oscar-wilde/the-picture-of-dorian-gray) on the Morgan Library & Museum website.

## What is TEI?

Let's first take a look at some TEI code. Here is an example of some TEI that encodes a line of text and indicates a portion that has been struck out.

    <line>This is a 
        <del>
            paragraph
        </del>
       line of text
    </line>

To those who are familiar with it, TEI, at first glance, looks a lot like HTML. Both use a tagging structure that encloses textual elements to indicate something about those elements. However, while HTML encodes how text should *appear* on a webpage, in the form of titles, headings, paragraphs, or links, TEI encodes the *content* of the text, in addition to some description about its appearance. 

## Hierarchy

The major constraint of TEI is that all elements must be nested within a hierarchical structure. This means there's a root element containing branches. The branches cannot overlap. 

This means that tags must nest properly, that is, you must always close the last tag you opened before closing a tag you opened previous to the last one.

See [page 20](./podg_ms_20.pdf) and [page 21](./podg_ms_21.pdf) from the Dorian Gray manuscript.

Below, we can see part of the transcription to the above image. The `<line>` tags containing other tags, such as `<del>`.

Some tags also contain attributes that further describe the tag, such as `<strikethrough>` to indicate text that has been struck out. 

```xml
         <line>"You</line>
         <line>remember that landscape of mine, for</line>
         <line>which Agnew offered me <gap reason="deleted"></gap> a</line>
         <line><gap reason="illegible"></gap><add place="above">huge</add>price, but which I would</line>
         <line>not part with? It is one of the</line>
         <line>best things I have ever done. And</line>
         <line>why is it so? Because, while I</line>
         <line>was painting it, Dorian Gray sat</line>
         <line>beside me, <del rend="strikethrough">and as he leaned across</del></line>
         <line>
            <del rend="strikethrough">to look at it, his</del> 
            <mod>
               <del rend="strikethrough">cheek</del>
               <add place="above" rend="strikethrough">hair</add>
            </mod>
            <del rend="strikethrough">just</del>
         </line>
         <line>
            <mod>
               <del rend="strikethrough">brushed</del>
               <add rend="strikethrough" place="above">touched</add>
            </mod>
            <mod>
               <del rend="strikethrough">my cheek</del>
               <add rend="strikethrough" place="above">hand.</add>
            <del rend="strikethrough">The world becomes</del>
            </mod>
         </line>
```

## Queer Mark Up Activity

For this project, I created a tagset reflects the general theme of each revision.

For this activity, spend a few minutes coming up with your own themes for the revisions. Use [this transcription from pages 20-21](./diplo.pdf) as your basis for your decisions. 

Then, get into groups, and see if you can decide on a set of tags (maybe 3-5 tags) to mark up the text. 

At the end, we will share our tagsets!