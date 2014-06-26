python-tagcloud
===============
A tag cloud image generator in python. Inspired from [jqcloud](https://github.com/lucaong/jQCloud).

Requirements
============
You will need PIL to run this code. To install pil simply run `pip install pil`

How to use
==========
    t = TagCloud()
    words = [{"text": "coffee", "weight": 20296.0},{"text": "love", "weight": 15320.0}]
    print t.draw(words)`

The list `words` should be sorted on weight before using, and the given format should be used.

How it works
============
It takes the list as input and normalizes the weights. Then it calculates the size of the word that will be drawn based on the weight. It then places the word on the center of the photo and then keeps moving it in a circle and gradually increasing the radius till it finds a place where it does not collide with any other word.

Once all the positions are calculated, the photo is written to a file.

You can confiure the font, color schemes and font size.

Sample
======
![](https://raw.githubusercontent.com/roshansingh/python-tagcloud/master/sample/a73c8493-a270-4ab9-a3a4-647803dc968c.jpg)