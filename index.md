# [elliotthuge.dev](https://www.elliotthuge.dev/)

## Computer Scientist turned UX Designer.

I use this website primarily for blogging thoughts and ideas.  
elliotthuge.dev is inspired by:
* [NoBoilerPlate](https://www.youtube.com/@NoBoilerplate) / [0atman](https://www.0atman.com/) / Tristram Oaten
* The [Cult of Done '*manifesto*'](https://medium.com/@bre/the-cult-of-done-manifesto-724ca1c2ff13) - especially item 12
* [gwern.net](https://gwern.net/)
* A general obsession with [Markdown](https://en.wikipedia.org/wiki/Markdown)

### Disclaimers:

* Not advocating for anyone or anything mentioned here by their presence or omission thereof in this site.
* Opinions here are not reflective of those of my employer, associates, peers etc.
* Content on this website may not reflect my true or current beliefs or opinions, e.g. satire.
* Content on this website may sustain for archival reasons.
* I will make no obligations or promises regarding the existence, future, content or purpose of this website.
* Everything on this site, including the site itself, is a draft.

### AI content declaration:

This site, and some of its content*, was built with the assistance of generative AI.

*_I intend to make a post about an AI declaration 'standard', e.g. marking pure-human origin content with `Hu`._

## Posts:  

{% for post in site.posts %}
  <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
  <p>{{ post.excerpt | truncatewords: 50 }}</p>
{% endfor %}