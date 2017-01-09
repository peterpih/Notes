You can figure out the last commit IDs using   

$ <b>git reflog show remotes/origin/</b><em>branch-name</em>  

<pre>
<b>165c01a</b> remotes/curl/spelling@{0}: update by push
<b>5c3ad5b</b> remotes/curl/spelling@{1}: update by push
95fd3e3 remotes/curl/spelling@{2}: update by push
5a0175c remotes/curl/spelling@{3}: update by push
7cc5282 remotes/curl/spelling@{4}: update by push
cdb0ef3 remotes/curl/spelling@{5}: update by push
c9e8cb5 remotes/curl/spelling@{6}: update by push
123129a remotes/curl/spelling@{7}: update by push
ac69c30 remotes/curl/spelling@{8}: update by push
</pre>

(confirmed through **git log**)  

$ <b>git log --oneline</b>   

<pre>
<b>165c01a</b> Proofreading FAQ MAIL-ETIQUETTE
<b>a41e859</b> examples: make the C++ examples follow our code style too
ed2fcd5 asiohiper: improved socket handling
8805be2 lib506: fix build for Open Watcom
5df25fd ROADMAP: 2017 cleanup
7fc0e1d COPYING: update the generic copyright year range
acd29dc docs/silent: mention --show-error in --silent description
e8404ad docs/page-header: mention how to disable the progress meter
ba19feb wolfssl: display negotiated SSL version and cipher
</pre>
