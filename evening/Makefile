VERSION := 0.1
TARGET := $(notdir $(patsubst %/,%,$(dir $(abspath $(lastword $(MAKEFILE_LIST))))))
BUILD_DIR ?= build

.PHONY: prayers

prayers: %: %.tex
	@mkdir -p $(BUILD_DIR)
	xelatex -output-directory=$(BUILD_DIR) -jobname=$(TARGET)-$@-$(VERSION) $<
	rm -f $(BUILD_DIR)/$(TARGET)-$@-$(VERSION).{aux,log,out}
