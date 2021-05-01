DIR_OUTPUT=.

CSS_SOURCE=scss/style.scss
CSS_TARGET=$(DIR_OUTPUT)/style.css

.PHONY: all clean compressed pretty

all: pretty

clean:
	@rm "${CSS_TARGET}"

compressed:
	@mkdir -p $(@D)
	sassc -t compressed "$(CSS_SOURCE)" "$(CSS_TARGET)"

pretty:
	@mkdir -p $(@D)
	sassc -t expanded "$(CSS_SOURCE)" "$(CSS_TARGET)"

print-%:
	@echo $* = ${$*}
