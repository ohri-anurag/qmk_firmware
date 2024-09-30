qmk compile -kb lily58 -km default
qmk flash -kb lily58 -km default -bl avrdude-split-left
qmk flash -kb lily58 -km default -bl avrdude-split-right
