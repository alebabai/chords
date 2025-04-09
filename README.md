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
    - wrap text into `{{% chords lyrics %}}` shortcode for superscript stylized chords
    - wrap text into `{{% chords inline %}}` shortcode for inline stylized chords

    An example of lyrics with chords:

    ```md
    {{% chords inline %}}  
    **[Вступление]** (x2): `[Am]` `[F]` `[C]` `[E]`  
    {{% /chords %}}

    {{% chords lyrics %}}  
    **[Куплет]**  
    Гра`[Am]`ницы кл`[F]`юч пере`[C]`ломлен попо`[E]`лам  
    А наш`[Am]` батюш`[F]`ка Ленин `[C]`совсем у`[E]`соп  
    {{% /chords %}}
    ```

1. Optional: use front matter to add addition metadata to the song:
    - add more artists, prioritizing the first as the main one, using the `artists` taxonomy
    - add tags using the `tags` taxonomy

1. Make sure the song is no longer a draft by removing `draft: true`.
1. Done - publish and enjoy!
