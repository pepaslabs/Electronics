# Electronics
A central place to organize and publish all of my hobbyist electronics knowledge and projects.

## Wiki

My first attempt at curating this clump of electronics knowledge was this [wiki](https://github.com/pepaslabs/Electronics/wiki).

## EEVBlog threads of interest

- [UT61E drift and recalibration](https://www.eevblog.com/forum/testgear/ut61e-drift-and-recalibration/)
  - [This post](https://www.eevblog.com/forum/testgear/ut61e-drift-and-recalibration/msg345532/#msg345532) describes replacing the built-in vref (75ppm/C) with the LT1790 (5ppm/C).

## Fluid baths for electronics (for volt-nuts, resistance-nuts, etc)

Immersing electronics in oil is a tempting idea to stablize the temperature of the components, which helps combat the temperature coefficient of the components in a precision circuit (i.e. a voltage or resistance transfer standard).

But what fluid should you use?

### Mineral oil

This seems to be the first idea people come across -- minearl oil is non-conductive, so you can immerse electronics in it.  Searching YouTube for "[raspberry pi minearl oil](https://www.youtube.com/results?search_query=raspberry+pi+minearl+oil)" shows lots of cool project ideas.

However, it turns out that over time, minearl oil breaks down and becomes acidic [[1]](http://www.eevblog.com/forum/metrology/ultra-precision-reference-ltz1000/msg410930/#msg410930) [[2]](https://www.eevblog.com/forum/projects/suggestions-for-a-temperature-sensor/msg75547/#msg75547).  It could be used, but for best results you may need to monitor the pH and change the oil when (or before!) it becomes acidic.

### Silicone oil

It appears silicone oil does not suffer from the same problems as mineral oil, and it appears this is the oil used in the Vishay hermetically sealed resistors [[1]](http://www.eevblog.com/forum/metrology/ultra-precision-reference-ltz1000/msg410930/#msg410930).

If you search amazon.com for "[silicone oil high purity](https://www.amazon.com/s/ref=nb_sb_noss?url=search-alias%3Daps&field-keywords=silicone+oil+high+purity&rh=i%3Aaps%2Ck%3Asilicone+oil+high+purity)", you'll find 16oz bottles from CCS (Consolidated Chemical & Solvents LLC) from $18 to $25.  These are available in viscosities from 0.65cSt to 100,000cSt.  Here's a helpful [video](https://www.youtube.com/watch?v=g1c4E1ze0Vo) comparing the viscosities of silicone oil.

## Communication checksums

For communication between a microcontroller and a PC, checksums can provide greater confidence of data integrity.

A default choice might be a CRC8 implementation.

A somewhat more obscure checksum called Fletcher16 has the benefit of being simpler / cheaper, while offering "good enough" integrity [[1]](https://en.wikipedia.org/wiki/Fletcher%27s_checksum) [[2]](https://gist.github.com/globby/9337839).

## "Awesome" lists

Github users have started an awesome tradition of curating lists of "awesome" links.

- https://github.com/monostable/awesome-electronics
  - Mentioned in the "meta awesome" list: https://github.com/sindresorhus/awesome#hardware
- A similar gist: https://gist.github.com/rgaidot/9132b50cdcdb455fccbe
- https://github.com/intajay/open-electronics
