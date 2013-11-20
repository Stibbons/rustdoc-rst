===========
rustdoc-rst
===========

A RST version of the rustdoc tool for the Rust Language (www.rust-lang.org)

It is tool deliberately based on the ``rustdoc`` tools but adapted for the restructedText markup language.

The main advantages of this tool are:

- easier to read: I personnally find RST files much clearer to read than Markdown
- RST suffers less from the different implementation. The de facto standard for RST code documentation is the 
  shinx documentation builder (sphinx-doc.org). This tool is also deliberately made to integerate itself with
  sphinx and reuse this wonderful tool.
- doxygen-like syntax:
   - @param
   - @return
