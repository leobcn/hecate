# hecate
The Hex Editor From Hell!

Usage:

    go get -u github.com/evanmiller/hecate
    $GOPATH/bin/hecate /path/to/binary/file

Hecate is not actually a hex editor, only a viewer. It is a terminal program
(written in Go) with tabs, binary searching, mmap support, and Vim-like controls.
Place the cursor over some bytes and choose a mode (**t** for text, **p** for a
bit pattern, **i** for an integer, **f** for a floating point) to see what
those bytes represent. Toggle endianness with **e** and signedness with **u**.

Screenshot:
![Hecate screenshot](http://www.evanmiller.org/images/hecate-screenshot1.png)

Full list of commands:

<table>
<tr><td>h</td><td>left</td> <td>t</td><td>text mode</td></tr>
<tr><td>j</td><td>down</td> <td>p</td><td>bit pattern mode</td></tr>
<tr><td>k</td><td>up</td> <td>i</td><td>integer mode</td></tr>
<tr><td>l</td><td>right</td> <td>f</td><td>floating-point mode</td></tr>

<tr><td>b</td><td>left 4 bytes</td> <td>e</td><td>toggle endianness</td></tr>
<tr><td>w</td><td>right 4 bytes</td> <td>u</td><td>toggle signedness</td></tr>

<tr><td>g</td><td>first byte</td> <td>H</td><td>shrink cursor</td></tr>
<tr><td>G</td><td>last byte</td> <td>L</td><td>grow cursor</td></tr>

<tr><td>/</td><td>search file</td> <td>D</td><td>date decoding</td></tr>
<tr><td>n</td><td>next match</td> <td>@</td><td>set date epoch</td></tr>

<tr><td>T</td><td>show tabs</td> <td>ctrl-t</td><td>new tab</td></tr>
<tr><td>tab</td><td>cycle tabs</td> <td>ctrl-w</td><td>close tab</td></tr>

<tr><td>ctrl-f</td><td>page down</td> <td>:</td><td>jump to offset</td></tr>
<tr><td>ctrl-b</td><td>page up</td> <td>x</td><td>toggle hex offset</td></tr>

<tr><td>ctrl-e</td><td>scroll down</td> <td>q</td><td>quit program</td></tr>
<tr><td>ctrl-y</td><td>scroll up</td> <td>?</td><td>help screen</td></tr> 
</table>
