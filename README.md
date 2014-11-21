Pelican Visualizations

These code visualizations are for https://github.com/getpelican/pelican/issues/1272

call_graph.png must be opened in a large-image-capable viewer, such as feh or gimp, see http://unix.stackexchange.com/questions/77968/viewing-large-image-on-linux

feh's manfile is http://man.finalrewind.org/1/feh/
most important notes are to use CTRL and ALT + Arrows for navigation

to generate this call graph, I used pycallgraph, graphviz, and imagemagick

pycallgraph graphviz -- /usr/local/bin/pelican -s settingsfile.py
mv tmp.filename call_graph.txt
dot -Tpdf call_graph.txt > call_graph.pdf
convert call_graph.pdf call_graph.png
