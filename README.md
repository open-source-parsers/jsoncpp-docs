Documentation for [jsoncpp](https://github.com/cdunn2001/jsoncpp)
-------------
* http://open-source-parsers.github.io/jsoncpp-docs/
  * hosted by GitHub Pages

## Build and deploy
Here is how to generate Doxygen documention.

1. Clone `jsoncpp`.
1. Clone `jsoncpp-docs`.
1. Build docs in `jsoncpp`.
1. Copy docs to `jsoncpp-docs`.
1. Push `json-cpp` to `gh-pages` branch.
```bash
git clone https://github.com/open-source-parsers/jsoncpp.git
git clone https://github.com/open-source-parsers/jsoncpp-docs.git
cd jsoncpp; python doxybuild.py --doxygen=$(which doxygen)
cd ../json-cpp
rsync -av ../jsoncpp/dist/doxygen/jsoncpp*/ doxygen/
git commit -a doxygen/
git push
```

## `jsoncpp` v. `json-cpp`
We store the static HTML in a different repo, `jsonp-docs` instead of `jsoncpp`, in order to reduce the total size of the jsoncpp project. The main project page is at:
* https://github.com/open-source-parsers/jsoncpp
