===========
rustdoc-rst
===========

A RST version of the rustdoc tool for the Rust Language (www.rust-lang.org)

It is tool deliberately based on the ``rustdoc`` tools but adapted for the `restructedText markup <http://en.wikipedia.org/wiki/ReStructuredText/>`_ language.

The main advantages of this tool over ``rustdoc`` are:

- easier to read: I personnally find RST files much clearer to read than Markdown
- enforce structuration. It's not just a markup extraction tool, it will also fail it the documentation if badly shaped.
- RST suffers less from the different implementation. The de facto standard for RST code documentation is the 
  shinx documentation builder (sphinx-doc.org). This tool is also deliberately made to integerate itself with
  sphinx and reuse this wonderful tool.
- RST has build in support for tables and extension.
- doxygen-like syntax to structure ``method``, ``struct`` and ``trait`` documentations:
   - ``@param``
   - ``@return``
   - ``@see``


Example
=======

::

   /*
    * Brief summary of the method
    * 
    * Returns a \ref vec of \ref T, containing everything from \ref v 
    * whose index is in the range [\ref start, \ref end).
    *
    * \param v     input vector
    * \param start start index (0-based)
    * \param end   end index (0-based)
    * \returns a new vector with the modified value
    * \see otherMethod
    * 
    */
    fn slice[T](array[T] v, uint start, uint end) -> vec[T] {
        assert (start <= end);
        assert (end <= len[T](v));
