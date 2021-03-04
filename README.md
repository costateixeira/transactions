# Transactions overview

This is a repo for structuring the creation of artifacts such as transactions. The content created here will be used in a "proper" ImplementationGuide. This repository is a scaffold to structure the content (and the mechanisms in this repo will be used in the "final" infrastructure.

Besides transactions, other types of content can be supported. Transactions is the current scope.

To add a transaction, add a transactionXXX.md file in the [_transactions folder](https://github.com/costateixeira/gendocs/tree/gh-pages/_transactions), where XXX is any differentiator for the transaction.
Transactions are structured in YAML frontmatter; the text attributes can be added in the MD directly, or refer to external md files. See the examples to see how this works.
The transaction also contains the diagrams (in svg format for now).

![IG Templates](http://www.plantuml.com/plantuml/proxy?cache=no&src=https://raw.githubusercontent.com/costateixeira/gendocs/gh-pages/docs/transaction_model.plantuml)
