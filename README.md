# The Morphing Map Project

Links (see below for short description):

- <a href="world_map.html">World Map in Different Projection</a>
- <a href="world_map_tissot.html">World Map with The Tissot's Indicatrix</a>
- <a href="robinson_refline.html">Robinson Projection</a>
- <a href="azeq_refpts.html">Azimuthal Equidistant Projection</a>

Note: The maps may look strange on Firefox. If it did not show something similar to the screenshot belows, please use Chrome or Chromium-based browser. 

## Intro
This website aims to use the SVG morphing function to show how the map is projected from the earth, and the distortion of maps with various projection approaches. 

The projections were setup with different crs (coordinate reference system) in proj4 string format. The crs were obtained from the [proj.org](https://proj.org/en/9.3/operations/projections/index.html) website. The data, including the world map shapefile and the grids, is obtained from [Natural Earth Data](https://www.naturalearthdata.com/) website. 

Some data manipulation/cleaning is done, including to add equal spacing point at 90S (Antartica) so that it acts more naturally when doing projection, and do some cutting at the opposite point/line of the referencing point/line to avoid strange situation when projecting. 

As of now (2024/01/25), the webpages listed below are for the global projections. 

# The Map Pages
## The morphing global map projections
About 44 projections were listed for the observation on how the world is morphing from one projection to another.  
<a href="world_map.html">The page url</a>.  
<a href="world_map.html"><img src="images/proj_map.png" width="90%" /></a>  


## The Tissot's Indicatrix
The same as the previous map projections, with the [Tissot's Indicatrix](https://en.wikipedia.org/wiki/Tissot%27s_indicatrix). Tissot's Indicatrix is a series of circle shapes with a fixed radius. The circles are projected along with the world map that cause them to morph to ellipses, so the change of the shapes can show the distortion in sizes, shapes, and directions.  
<a href="world_map_tissot.html">The page url</a>. 
<a href="world_map_tissot.html"><img src="images/proj_map_tissot_indicatrix.png" width="90%" /></a>


## The Robinson Projection
The [Robinson projection](https://en.wikipedia.org/wiki/Robinson_projection) is one of the popular world projection method to show the entire world at once. It was specifically created in an attempt to find a good compromise to the problem of readily showing the whole globe as a flat image. The Robinson projection is neither equal-area nor conformal, abandoning both for a compromise. The distortion close to the poles is severe, but quickly declines to moderate levels moving away from them. The webpage shows how the changing reference line (longitude) would affect the resulting world map.  
<a href="robinson_refline.html">The page url</a>.  
<a href="robinson_refline.html"><img src="images/robinson_refline.png" width="90%" /></a>


## The Azimuthal Equidistant Projection
The [azimuthal equidistant projection](https://en.wikipedia.org/wiki/Azimuthal_equidistant_projection) has the useful properties that all points on the map are at proportionally correct distances from the center point (reference point), and that all points on the map are at the correct azimuth (direction) from the center point. The flag of the United Nations and World Health Organization contains an example of a polar azimuthal equidistant projection (reference point: N90-EW0). The webpage below shows how the azimuthal equidistant projection with changing reference points.  
<a href="azeq_refpts.html">The page url</a>.  
<a href="azeq_refpts.html"><img src="images/azimuthal_eqdist_ref_points.png" width="90%" /></a>


# The Tools
- [vmapper](https://github.com/wcchin/vmapper/): a Python tool I wrote long long time ago (about 7-8 years) for converting geopandas geodataframe to svg format. 
- [skeleton.css](http://getskeleton.com/): the frontend framework for webpage
- [Montserrat font](https://fonts.google.com/specimen/Montserrat): the font
- [Github Pages](https://pages.github.com/): for hosting
- [carlae](https://wcchin.github.io/carlae/minimal/index.html): for generating this page
- [Minimal](https://github.com/orderedlist/minimal): template for this page

## Some background
The thought to build a webpage of the morphing projection sparkled when I saw how people use SVG morphing to show the changing of the [Batman logo](http://tavmjong.free.fr/blog/?p=741). Map projections are similar with and different from each other in some ways. So, it would be interesting to see how they change from one to another, just like the Batman logo. 

Therefore, I started the Vmapper project and have done creating the SVG for maps from the shapefile, using GeoPandas in Python. It was based on Python 2.xx back then, about 7-8 years ago (based on Github commit history). Then, it seems to be a long way to do and some JS tool to be used to achieve the objective. And I have some other stuff to busy on, so it stopped at that point. Until last week when I was preparing for a cartography course, this a-decade-old idea pop-up again in my mind, so I decided to see if I can finish it quickly. This took longer than I expected. I was planning to finish it in 2-3 days but it took me about 1 week now. I am quite satisfy with the current form. I may want to add more local projection example later when I have time. 


