CFLAGS = -I zlib
LIBS = -I ../extlib

all: bytecode native

bytecode: extc_stubs.obj
	ocamlc -g $(LIBS) $(CFLAGS) $(NATIVE_LIBS) -a -o extc.cma extc.ml

native: extc_stubs.obj
	ocamlopt -a -o extc.cmxa $(LIBS) extc.ml
	
	

extc_stubs.obj: extc_stubs.c
	ocamlc -ccopt "$(CFLAGS)" -c  -o $@ $<
	
extc.cmo: extc.ml
	ocamlc -g $(LIBS) -c $<
	
extc.cma: extc.cmo extc_stubs.obj
	ocamlc -a -o $@  extc.cmo 

clean:
	rm -f *.obj *.lib *.so *.cmo *.cmi *.cma *.cmx *.cmxa 
