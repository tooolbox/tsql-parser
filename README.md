The tsql-parser is a parser for T-SQL. It is based on the [ANTLR4](https://github.com/antlr/antlr4) and use the grammar from [antlr4-grammars-plsql](https://github.com/antlr/grammars-v4/tree/master/sql/tsql).

## Build

Before build, you need to install the ANTLR4.

requirements:

- https://github.com/antlr/antlr4/blob/master/doc/getting-started.md
- https://github.com/antlr/antlr4/blob/master/doc/go-target.md

```bash
./build.sh
```

## Update grammar

### Manually change the grammar file in this project

1. run `./build.sh` to generate the parser code.

### From antlr4-grammars-tsql

1. Clone the `TSqlLexer.g4` and `TSqlParser.g4` grammar files from https://github.com/antlr/grammars-v4/tree/master/sql/snowflake.
2. Clone the examples[https://github.com/antlr/grammars-v4/tree/master/sql/tsql/examples], and use it for test.
3. run `./build.sh` to generate the parser code.

## Test the parser

Run `TestTSQLParser` in `parser_test.go` to test the parser.

```bash
go test -v
```

## References

- ANTLR4 Getting Started https://github.com/antlr/antlr4/blob/master/doc/getting-started.md
- ANTLR4 Go Garget https://github.com/antlr/antlr4/blob/master/doc/go-target.md

## Port

Port folder contains the ported code in another language.
