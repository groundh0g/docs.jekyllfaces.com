# Comments

Start typing here...

## Usage

Blah, blah, blah ...

### Configuration

Blah, blah, blah ...

```
comments:
  provider: utterances # one of: false | facebook | utterances | disqus | intensedebate | ## UNSUPPORTED: duoshuo
  include:
    posts: true  # one of: true | false 
    pages: false # one of: true | false 
    books: false # one of: true | false 
    docs:  false # one of: true | false 
  facebook:
    siteid:   9999999999999999
    theme:    dark # one of: light | dark
    numposts: 10
    nonce:    # optional nonce, see Facebook Comment widget docs
  utterances:
    siteid: user/repo # ex: username/project-comments-repo
    theme: gruvbox-dark # one of: github-light | github-dark | github-dark-orange | icy-dark | dark-blue | photon-dark | boxy-light | gruvbox-dark
  disqus:
    siteid: site-name 
  intensedebate:
    siteid: ff999999999999999999999999999999
```