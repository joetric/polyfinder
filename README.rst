**polyfinder**

Given a single-line address, ``polyfinder`` returns geoenabled
data from ESRI ArcGIS REST services. In its default configuration,
it uses geocoding services hosted by ESRI (primary)
and MapQuest (fallback).

Currently the only useful method available is to get ward districts
in Philadelphia. However, this could be easily adapted to work
with other endpoints.

Formal documentation has not yet been developed, so check
the docstrings and comments in the source.

Here's a simple example:

	>>> from polyfinder import PolyFinder
	>>> pf = PolyFinder('226 Ripka St, 19127')
	>>> pf.ward_div()
	{u'ADDRESS': u'201 FOUNTAIN ST',
	 u'CENTROID_X': -75.23040009,
	 u'CENTROID_Y': 40.03039932,
	 u'DIVISION': u'08',
	 u'ID': u'2108',
	 u'LOCATION': u'Y',
	 u'MATCH_ADDR': u'201 FOUNTAIN ST',
	 u'OBJECTID': 438,
	 u'OBJECTID_1': 1253,
	 u'OBJECTID_12': 1253,
	 u'PERIMETER': 1.0217016,
	 u'POLLING_PL': u'HILLSIDE RECREATION CENTER',
	 u'POLLING_X': -75.229599,
	 u'POLLING_Y': 40.03350067,
	 u'SHAPE.AREA': 1501706.65864654,
	 u'SHAPE.LEN': 5394.584423083521,
	 u'SHAPE_LENG': 5394.5844231,
	 u'WARD': u'21'}