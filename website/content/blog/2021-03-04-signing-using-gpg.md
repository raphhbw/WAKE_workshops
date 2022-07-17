+++
title = "Signing files using GPG"
date = 2021-03-04
[taxonomies]
tags = ["gpg"]
+++

### Signing a pdf document

To sign a pdf document:

```gpg --output doc.pdf.sig --detach-sig doc.pdf```

When sending the document send both doc.pdf and doc.pdf.sig

People can then verify the digital signature with

```gpg --verify doc.pdf.sig doc.pdf```
