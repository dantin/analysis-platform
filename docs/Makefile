
SOURCE_DIR   := $(shell pwd)
DOT_FILES    := $(basename $(notdir $(shell find $(SOURCE_DIR) -name '*.dot')))

DEFAULT: png

.PHONY: png
png: $(DOT_FILES)
$(DOT_FILES): %: %.dot
	@dot $^ -Tpng -o figures/$@.png

.PHONY: clean
clean:
	@rm -rf *.png
