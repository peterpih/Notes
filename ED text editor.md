###[GNU ed manual](http://www.gnu.org/software/ed/manual/ed_manual.html)

<b>files</b>
<pre>
<b>w</b> <em>file_name</em>             <em># write file</em>
<b>q</b>                       <em># quit editor</em>
</pre>
<b>print (show)</b>
<pre>
<em>n</em>                       <em># print line n</em>
<b>1</b>                       <em># print first line in buffer</em>
<b>$</b>                       <em># print last line in buffer</em>
<b>1,$p</b>                    <em># print entire buffer</em>
<b>,p</b>                      <em># print all the lines</em>
</pre>
<b>Positioning</b>
<pre>
<b>+</b>                       <em># next line</em>
<b>+</b><em>n</em>                      <em># next n line</em>
<b>-</b>                       <em># previous line</em>
<b>-</b><em>n</em>                      <em># previous n line</em>
<b>;</b>                       <em># current through last line of buffer</em>

<b>/</b><em>re</em><b>/</b>                    <em># next line containing 're'</em>
<b>?</b><em>re</em><b>?</b>                    <em># previous line containing 're'</em>
</pre>
<pre>
<b>a</b>                       <em># append to buffer</em>
<b>0a</b>                      <em># append to beginning of buffer</em>
</pre>

<b>Searching</b>
<pre>
<b>s/</b><em>find-string</em><b>/</b><em>replace-string</em><b>/</b>
</pre>
