VERSION := 1.1
TARGET := $(notdir $(patsubst %/,%,$(dir $(abspath $(lastword $(MAKEFILE_LIST))))))
BUILD_DIR ?= build

.PHONY: all $(TARGET)

all: $(TARGET)

$(TARGET): %: %.tex
	@mkdir -p $(BUILD_DIR)
	xelatex -output-directory=$(BUILD_DIR) -jobname=$@-$(VERSION) $<
	rm -f $(BUILD_DIR)/$@-$(VERSION).{aux,log,out}
