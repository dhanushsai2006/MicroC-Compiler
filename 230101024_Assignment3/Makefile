# Makefile for a3_230101024 – nanoC Lexer
# Roll: 230101024

ROLL     = 230101024
LEX_FILE = a3_$(ROLL).l
TEST_FILE= a3_$(ROLL)_test.nc
TOK_OUT  = a3_$(ROLL)_token.txt
ST_OUT   = a3_$(ROLL)_st.txt
LEXER    = lexer

.PHONY: all clean run

all: $(LEXER)

$(LEXER): $(LEX_FILE)
	flex $(LEX_FILE)
	gcc lex.yy.c -o $(LEXER)

run: $(LEXER)
	./$(LEXER) $(TEST_FILE)
	@echo ""
	@echo "=== Token Output ==="
	@cat $(TOK_OUT)
	@echo ""
	@echo "=== Symbol Table ==="
	@cat $(ST_OUT)

clean:
	rm -f lex.yy.c $(LEXER) $(TOK_OUT) $(ST_OUT)
