# Chords

> An old-fashioned static website with intentionally wrong chords of my favorite songs

[![build](https://img.shields.io/github/actions/workflow/status/alebabai/chords/ci.yml)](https://github.com/alebabai/chords/actions?query=workflow%3ACI)

## Technologies

- [Hugo](https://gohugo.io/)

## Getting started

1. Install [Hugo](https://gohugo.io/).
1. Clone the repository.
1. Run `hugo server` to locally build and serve the site with live-reload feature.

## Usage

### Adding a new song

1. Create a page for the song:

    ```sh
    hugo new content "songs/<Artist> - <Title>.md"
    ```

    ```sh
    hugo new content "songs/Гражданская Оборона - Всё идёт по плану.md"
    ```

1. Add song lyrics with chords:
    - write chords using the following syntax ``` `[Chord]` ```
    - place chords wherever the music demands, within lines, words, etc
    - use `chords` shortcode and wrap lyrics into `{{< chords class="lyrics ">}}` for superscript stylized chords
    - use `chords` shortcode and wrap text with chords into `{{< chords >}}` for inline stylized chords

    An example of lyrics with chords:

    ```md
    {{% chords %}}  
    Вступление: `[Am]` `[F]` `[C]` `[E]`
    {{% /chords %}}  

    
    {{% chords class="lyrics" %}}  
    Гра`[Am]`ницы `[F]`ключ пере`[C]`ломлен`[E]` пополам  
    А наш`[Am]` батюшка `[F]`Ленин `[C]`совсем`[E]` усоп   
    {{% /chords %}}
    ```

1. Optional: use front matter to add addition metadata to the song:
    - add more artists, prioritizing the first as the main one, using the `artists` taxonomy
    - add tags using the `tags` taxonomy

1. Make sure the song is no longer a draft by removing `draft: true`.
1. Done - publish and enjoy!
