# Setup
qmk setup

# Cheapis
qmk compile -kb cheapis/cheapis -km ohri-anurag
qmk flash -kb cheapis/cheapis -km ohri-anurag

# Cheapis with RP2040
qmk compile -kb cheapis/cheapis2040 -km ohri-anurag
