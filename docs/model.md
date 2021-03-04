---
layout: default
title: Model
nav_order: 4
parent: HowTo
---

To add a transaction, add a file called transactionx.md in the _transactions folder

The content can be in the yaml file directly, or added as .md files. See the examples

This file has some front matter (delimited by the `---` lines) and this front matter is some YAML with the following structure:
```yaml
  transaction: 
     id (1..1): string
     name (1..1): string
     version (0..1): string
     lastUpdated (0..1): date
     scope (1..1): # the textual description of the content semantics
        fileName (0..1): string # the markdown (.md) filename where the content for this section is. This .md file will also be in the _transactions folder
        text (0..1): # the actual content, instead of an external file
     overview  (0..1): # the textual description of the transaction:
        text (0..1): 
        fileName (0..1): 
     participants (1..*): a list of participants : actors and their role.
        - 
          actor (0..1): string
          role (0..1): string
     standards (0..*): # a list of standards used
        -  
           name (0..1): string
           version (0..1): string
           url (0..1): string(url)
     interactions (1..*): # a list of interactions that define the transaction
        - 
           id (1..1): string #  the id of the interaction
           title (1..1): string # the title / header for the interaction
           diagram (0..1): # the filename where the svg with the diagram is
             fileName (0..1): string
             description (0..1): string
          description (0..1): # the text description of the interaction
             text (0..1): string
             fileName (0..1): string
          triggerEvents (0..1): # the text describing the trigger events
             fileName (0..1): string
             text (0..1): string
          messageSemantics (0..1): # the textual description of the content semantics
             description (0..1): # the text content 
                fileName (0..1): string
                description (0..1): string
          subsections (0..*): a list of optional subsections to describe the interaction
             -
                title (0..1): string # the title of the subsection
                content (0..1): # the actual text of the subsection
                   fileName (0..1): string
                   text (0..1): string
          expectedActions (0..1): # the textual description of the expected actions
             description (0..1): # the text content
                fileName (0..1): string
                text (0..1): string
```