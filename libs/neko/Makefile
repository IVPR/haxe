all:
	ocamlopt -g -I ../extlib -a -o neko.cmxa nast.ml nxml.ml binast.ml nbytecode.ml ncompile.ml
	
bytecode:
	ocamlc -g -I ../extlib -a -o neko.cma nast.ml nxml.ml binast.ml nbytecode.ml ncompile.ml

clean:
	rm -rf neko.cmxa neko.lib neko.a $(wilcard *.cmx) $(wildcard *.obj) $(wildcard *.o) $(wildcard *.cmi)
	rm -rf neko.cma neko.lib neko.a $(wilcard *.cmo) $(wildcard *.obj) $(wildcard *.o) $(wildcard *.cmi)