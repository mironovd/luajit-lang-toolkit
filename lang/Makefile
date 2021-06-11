
LANG_LUA_FILES = ast_boolean_const_eval.lua ast_const_eval.lua bcread.lua bcsave.lua \
	bytecode.lua compile.lua generator.lua lexer.lua id_generator.lua lua_ast.lua operator.lua \
	parser.lua reader.lua

LANG_H_FILES = $(LANG_LUA_FILES:%.lua=%.h)

all: $(LANG_H_FILES)

clean:
	rm -fr $(LANG_H_FILES)

%.h: %.lua
	luajit -b $< $@

.PHONY: all clean