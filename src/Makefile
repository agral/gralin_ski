DIR_OUTPUT=../out

CSS_SOURCE=scss/style.scss
CSS_TARGET=$(DIR_OUTPUT)/style.css

.PHONY: all clean publish debug

all: publish

clean:
	@rm -rf "${DIR_OUTPUT}"

publish: css_compressed copy_static_files

debug: css_pretty copy_static_files

.PHONY: css_compressed css_pretty copy_static_files
css_compressed:
	@mkdir -p $(@D)
	sassc -t compressed "$(CSS_SOURCE)" "$(CSS_TARGET)"

css_pretty:
	@mkdir -p $(@D)
	sassc -t expanded "$(CSS_SOURCE)" "$(CSS_TARGET)"

copy_static_files:
	@cp -rv "images/" "${DIR_OUTPUT}/"
	@cp -v "./index.html" "${DIR_OUTPUT}/"

print-%:
	@echo $* = ${$*}
