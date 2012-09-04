BackwardsReaderIter
====================

I have used [BackwardsReader](http://code.activestate.com/recipes/439045-read-a-text-file-backwards-yet-another-implementat/) before. It's really good but I think if a iter is available, it will be better.

So I enhanced it on iteration part. 

Before when you use BackwardsReader:

	br = BackwardsReader(open('bar'))

	while 1:
    	line = br.readline()
    	if not line:
    	    break
    	print repr(line)`
    
Now use BackwardsReaderIter:

	bri = BackwardsReaderIter(file_name)
	for line in bri.backread():
		print line