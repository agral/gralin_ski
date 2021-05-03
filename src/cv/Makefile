DIR_OUTPUT=../../out/cv

CSS_SOURCE=scss/style.scss
CSS_TARGET=$(DIR_OUTPUT)/style.css

.PHONY: publish clean

publish: css_compressed copy_static_files publish_pdf

clean:
	@rm -rfv "$(DIR_OUTPUT)"

.PHONY: css_compressed css_pretty copy_static_files pdf
css_compressed:
	@mkdir -p "$(DIR_OUTPUT)"
	sassc -t compressed "$(CSS_SOURCE)" "$(CSS_TARGET)"

css_pretty:
	@mkdir -p "$(DIR_OUTPUT)"
	sassc -t expanded "$(CSS_SOURCE)" "$(CSS_TARGET)"

copy_static_files:
	@mkdir -p "$(DIR_OUTPUT)"
	@cp -rv "images/" "$(DIR_OUTPUT)/"
	@cp -v "index.html" "$(DIR_OUTPUT)/"

publish_pdf:
	@$(MAKE) -C tex publish
