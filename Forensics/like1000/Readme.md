Challenge
```
This .tar file got tarred a lot.
```

They gave me a tar archive named 1000.tar. So I decompressed it and it gave me 999.tar so that means it is compressed 1000 times
So to decompress it I wrote a simple python script.

```
#!/usr/bin/env python3

import tarfile 
import sys
from PIL import Image

for i in range(1000,0,-1):
	
	filename = str(i) + ".tar"
	sys.stdout.write("\rGetting Flag " + filename)

	with tarfile.open(filename) as file:
		file.extractall()

im = Image.open('flag.png')
im.show()
```

Running this script will give you the flag

flag: ```picoCTF{l0t5_0f_TAR5}```
