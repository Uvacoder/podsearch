# podsearch

Search for Podcasts (in the iTunes store). 
Podsearch is Python package first of all.
But there is also a CLI tool available.

# Python Package

```python 
from podsearch import Media
from podsearch.podsearch import PodSearch

# Create your own individual search object
PodSearch('accidental tech podcast').search()
PodSearch('Tim', media=Media.PODCAST).search()

# Access directly a podcast search object
PodSearch.podcast_author('Tim').search()
PodSearch.podcast('Freakshow').search()
```

# CLI Tool 

```bash
podsearch-cli.py -t freakshow 
podsearch-cli.py -t freakshow -m podcast
podsearch-cli.py -t freakshow -m music
podsearch-cli.py -t freakshow -m ebook
```

## Help

```bash
Usage: podsearch-cli.py [OPTIONS]

Options:
  -t, --term TEXT                 Enter your search term!  [required]
  -m, --media [movie|podcast|music|musicVideo|audiobook|shortFilm|tvShow|software|ebook|all]
                                  Media category  [default: podcast]
  --help                          Show this message and exit.
```


## Example 

```bash
$ python podsearch-cli.py -t freakshow -l 3

Podcasts (3):

# Item 1/3: Freakshow [CLEAN]
    podcast - Podplay - Comedy - USA

# Item 2/3: Freak Show [CLEAN]
    podcast - Metaebene Personal Media - Tim Pritlove - Technology - USA

# Item 3/3: Internet Freakshow - Stories of Internet Mysteries, Trolls, Weirdos, and Freaks [EXPLICIT]
    podcast - GNPN - Technology - USA
```