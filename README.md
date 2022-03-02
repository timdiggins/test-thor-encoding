Reproduction for: https://github.com/rails/thor/issues/776

Expected that thorfiles like ruby (since 2.0) would have default encoding of UTF-8

But actually they have ASCII-8BIT.

`thor test_with:encoding`

    "Some λέξεις 一些词 🎉": UTF-8:
    ok


but 

`thor test_without:encoding`

    "Some \xCE\xBB\xCE\xAD\xCE\xBE\xCE\xB5\xCE\xB9\xCF\x82 \xE4\xB8\x80\xE4\xBA\x9B\xE8\xAF\x8D \xF0\x9F\x8E\x89": ASCII-8BIT:
    expected ASCII-8BIT to equal UTF-8

