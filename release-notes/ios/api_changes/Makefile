all: index.html meta.json

index.html:
	erb -T - index.html.erb > index.html

meta.json:
	erb -T - meta.json.erb > meta.json

clean:
	rm index.html meta.json

