VERSION := 1.1
TARGET := $(notdir $(patsubst %/,%,$(dir $(abspath $(lastword $(MAKEFILE_LIST))))))
BUILD_DIR ?= build

.PHONY: all songs prayer

all: songs prayer

songs prayer: %: %.tex
	@mkdir -p $(BUILD_DIR)
	xelatex -output-directory=$(BUILD_DIR) -jobname=$(TARGET)-$@-$(VERSION) $<
	rm -f $(BUILD_DIR)/$(TARGET)-$@-$(VERSION).{aux,log,out}
