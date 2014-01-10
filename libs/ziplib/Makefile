all:
	ocamlopt -g -I ../extlib -I ../extc -a -o zip.cmxa zlib.mli zlib.ml zip.mli zip.ml
	
bytecode:
	ocamlc -g -I ../extlib -I ../extc -a -o zip.cma zlib.mli zlib.ml zip.mli zip.ml
	
clean:
	rm -rf zip.cmxa zip.lib zip.a $(wildcard *.cmx) $(wildcard *.obj) $(wildcard *.o) $(wildcard *.cmi)
	rm -rf zip.cma zip.lib zip.a $(wildcard *.cmo) $(wildcard *.obj) $(wildcard *.o) $(wildcard *.cmi)