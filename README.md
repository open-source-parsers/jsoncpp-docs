Documentation for [jsoncpp](https://github.com/cdunn2001/jsoncpp)
-------------
* http://open-source-parsers.github.io/json-cpp/
  * hosted by GitHub Pages

## Build and deploy
Here is how to generate Doxygen documention.

1. Clone `jsoncpp`.
1. Clone `json-cpp`.
1. Build docs in `jsoncpp`.
1. Copy docs to `json-cpp`.
1. Push `json-cpp` to `gh-pages` branch.
```bash
git clone https://github.com/open-source-parsers/jsoncpp.git
git clone https://github.com/open-source-parsers/json-cpp.git
cd jsoncpp; python doxybuild.py --doxygen=$(which oxygen)
cd ../json-cpp
rsync -av ../jsoncpp/dist/doxygen/jsoncpp*/ doxygen/
git commit -a doxygen/
git push
```

## `jsoncpp` v. `json-cpp`
We store the static HTML in a different repo, `jsonp-cpp` instead of `jsoncpp`, in order to reduce the total size of the jsoncpp project. The main project page is at:
* https://github.com/open-source-parsers/jsoncpp
