INTERMEDIATES_DIR=build
SOURCE_FILENAME=CV.tex
.PHONY: build

build: $(SOURCE_FILENAME)
	@mkdir -p "$(INTERMEDIATES_DIR)"
	pdflatex -output-directory "$(INTERMEDIATES_DIR)" "$(SOURCE_FILENAME)"
	@mv "$(INTERMEDIATES_DIR)/CV.pdf" "./cv.pdf"
