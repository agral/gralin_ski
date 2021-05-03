INTERMEDIATES_DIR=build
SOURCE_FILENAME=CV.tex
PDF_FILENAME=cv.pdf
PUBLISH_DIR="../../../out/cv/tex"

.PHONY: build publish

build: $(SOURCE_FILENAME)
	@mkdir -p "$(INTERMEDIATES_DIR)"
	@>/dev/null 2>&1 pdflatex -output-directory "$(INTERMEDIATES_DIR)" "$(SOURCE_FILENAME)"
	@mv "$(INTERMEDIATES_DIR)/CV.pdf" "./$(PDF_FILENAME)"
	@echo "successfully built $(PDF_FILENAME)"

$(PDF_FILENAME): build

publish: $(PDF_FILENAME)
	@mkdir -p "$(PUBLISH_DIR)"
	@cp "$(PDF_FILENAME)" "$(PUBLISH_DIR)/"
	@echo "published $(PDF_FILENAME)"
