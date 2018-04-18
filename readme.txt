============ Run Instructions ===========

Simply open a Terminal at the project directory, run, for example:
	# Example for IIT Campus
	$ python3 main.py 41.839341 -87.629504 41.831092 -87.623239
or
	# Example for Chicago Loop
	$ python3 main.py 41.888438 -87.644858 41.848298 -87.614988

The output desired image is then saved as 'result.jpg', one at a time.

Note:
	1. The four parameters represents lat1, lon1, lat2, lon2, respectively.


============ Required Environment ===========
Python 3.6
Pillow (PIL Fork) 5.1.x

Note:
	1. Installation of PIL:  $ pip install Pillow
	2. Make sure the 'null.jpeg' file is in the current running directory.



=========== Project files ===========
main.py
TileSystem.py



=========== Algorithm Introduction ==========

1. Determine the lowest acceptable level by all bounding box area within one tile.
2. Determine the final best level by filtering out from fine to coarse iteratively.
3. Query each tile image and paste.
		Convert lat/lon to pixel coordinates.
		Convert pixel coordinates to tile coordinates.
		Query tile image from Bing Server.
4. Refine and crop the generated image by pixel granularity.




