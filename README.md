# Firebase Docset

Firebase Docset for [Dash.app](https://kapeli.com/dash) work offline and quick explore.

I build the docset to help me to work with firebase web SDK. This time only firebase web SDK reference included.

If you want more, please follow the [HOWTO](#how-to-build-firebase-docset) section to build your own.

## How to build firebase docset

Follow example I demonstrate how I build the docset, I wish that will help you to build your own.

Before getting start, make sure `wget` and [`dashing`](https://github.com/technosophos/dashing) installed. *(There're some issues while I working with dashing prebuilt version, I use alternative `go get` to install.)*

First to download the entire firebase web SDK reference from `https://firebase.google.com/docs/reference/js/` *(Replace the URL to what your want)*

`wget -r -l 0 -k -p -np <SDK reference URL>`

And go to folder place the downladed files.

`$GOPATH/bin/dashing create`

to create `dashing.json` that define the rules of how [Dash.app](https://kapeli.com/dash) index docset. *(More details about define index rules, please visit [Dash.app](https://kapeli.com/docsets#dashDocset) and [dashing](https://github.com/technosophos/dashing/blob/master/README.md#dashing-generate-dash-documentation-from-html) document)*.

After define the rules

`$GOPATH/bin/dashing build`

will auto-generate doceset.


