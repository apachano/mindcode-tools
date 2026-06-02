# mindcode-tools

Mindcode language support for VS Code.

## Features (0.1)

* Mindcode file association for `.mnd`
* Syntax highlighting via TextMate grammar
* Language configuration for comments, brackets, auto-closing pairs, indentation, and folding markers
* Basic autocomplete snippets

### Available snippets

Use these snippet prefixes in Mindcode files:

* `if` -> if/else block
* `for` -> for-in loop
* `while` -> while loop
* `fun` -> function definition template
* `unit` -> basic `ubind` + `ucontrol move`
* `print` -> print + printflush template

## Requirements

No additional runtime requirements for language features in 0.1.

Compiler integration is planned in 0.3.

## Developer Docs

Contributor and release workflow documentation is in [DEVELOPMENT.md](DEVELOPMENT.md).

## Known Issues

* No semantic language features yet (hover, go-to-definition, diagnostics)
* Snippets are intentionally basic and will expand over time

## Roadmap

### 0.1 - Language Basics

* [x] TextMate grammar
* [x] File extension registration (.mnd)
* [x] Basic autocomplete
* [x] Bracket matching, comments, indentation rules

### 0.2 - Intermediate Language

* [ ] Doc hovers
* [ ] Basic auto formatter
* [ ] Go to definition
* [ ] Signature help

### 0.3 - Compiler Integration

* [ ] Compiler path
* [ ] Command palette to compile current file
* [ ] Output path
* [ ] Problem matcher diagnostics in Problems panel
* [ ] Build task and status notifications
* [ ] Configurable compiler path/args in extension settings
* [ ] Safe pre-flight checks

### 0.4 - Deployment Integration

* [ ] Command palette: compile and deploy to Mlog Watcher

### 0.5 - Advanced Language Features

* [ ] Symbol renaming
* [ ] Linting
* [ ] Quick fixes
* [ ] Code actions
* [ ] Debug story
