SOURCE=scss/style.scss
TARGET=style.css

.PHONY: all clean compressed pretty

all: pretty

clean:
	@rm -v $(TARGET)

compressed:
	sassc -t compressed $(SOURCE) $(TARGET)

pretty:
	sassc -t expanded $(SOURCE) $(TARGET)
