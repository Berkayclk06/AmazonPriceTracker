Hey guys! 

You can find code in main.py file. Code can be buggy.

If you look closely I encode and decode the product_title again.

``` Python
product_title = soup.find(id="productTitle").getText().strip().encode("ascii", "ignore")
product_title = product_title.decode()
```
That is because when I try to run the code. It gave this error:

```
"UnicodeEncodeError: 'ASCII' codec can't encode character '\u2011' in position 88: ordinal not in range(128)"
```


So I had to encode it. After the encoding, product_title is printed as " b'2021 Apple MacBook Pro ".
"b" at the beginning of the string means it's a byte object. So, to remove b from the beginning I had to decode it again.

I hope you like it!