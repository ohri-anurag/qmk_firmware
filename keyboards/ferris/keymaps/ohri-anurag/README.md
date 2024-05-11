# Setup
qmk setup

# Cheapis
qmk compile -kb ferris/sweep -km ohri-anurag
qmk flash -kb ferris/sweep -km ohri-anurag -bl avrdude-split-left
qmk flash -kb ferris/sweep -km ohri-anurag -bl avrdude-split-right
