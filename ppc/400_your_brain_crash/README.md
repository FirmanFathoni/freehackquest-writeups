Name:

	your_brain_crash

Score:

	400

Subject:
	
	PPC

Description:

	char *ptr = array;

	lol 		=	--*ptr; 
	lool 		=	++*ptr; 
	loool 		=	--ptr; 
	looool 		=	++ptr; 
	loooool 	=	putchar(*ptr); 
	looooool 	=	*ptr=getchar(); 
	loooooool 	=	while (*ptr) { 
	looooooool 	=	}
	https://drive.google.com/open?id=0BzfPP2u0U3CsT2dlT2M1enFqaGc

Answer:

	YourFlag

Author:

	[life] by_sm

Solution:

* Replacing all `lo..l` to the code:
       
```
#include<iostream>
#include<cstdio>

char *ptr = new char[1024];

int main() {
	// your code here
	....
}
```

* `g++ your_brain.cpp -o your_brain`
* `./your_brain`
* Now we have this python code:

```
iMporT Zlib, baSe64

s = "eJzLzC3ILypRqMrJTNJRSEosTjUzUeDlKijKzCtRUI/MLy1yy0lMVwcA/4YMuQ=="
c = bAsE64.b64dEcoDe(s)
d = ZliB.dEcoMpReSS(c)
```

* Fixing the python script:

```
#!/usr/bin/python

import zlib, base64

s = "eJzLzC3ILypRqMrJTNJRSEosTjUzUeDlKijKzCtRUI/MLy1yy0lMVwcA/4YMuQ=="
c = base64.b64decode(s)
d = zlib.decompress(c)

print(d)
```

* Running the code:

```
./your_brain_step2.py 
import zlib, base64 
print('YourFlag')
```
