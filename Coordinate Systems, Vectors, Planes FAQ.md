 * [document source](http://www.j3d.org/matrix_faq/)

 ---

<pre>
<span class="c1">Coordinate Systems, Vectors, Planes FAQ
=======================================</span>

Version 1.4  28th December 2001
-------------------------------

This FAQ is now maintained by "<a href=
"mailto:andreas@%28no-spam%29cs.ualberta.ca">andreas@(no-spam)cs.ualberta.ca</a>".
Any additional suggestions or related questions are welcome.
Just send E-mail to the above address.

The latest copy of this FAQ can be found at the following web page:

    <a href=
"http://web.archive.org/web/20041011193859/http://www.cs.ualberta.ca/%7Eandreas/math/vectfaq_latest.html">
http://www.cs.ualberta.ca/~andreas/math/vectfaq_latest.html</a>

Feel free to distribute or copy this FAQ as you please.

Contributions
-------------

  Appearance: Cleaned out some of the empty lines, made the header like the
matrfaq:  <a href="mailto:andreas@%28no-spam%29cs.ualberta.ca">Andreas Junghanns</a>


History
-------

I (Andreas) received this FAQ from "<a href=
"mailto:sylvainc@%28no-spam%29total.net">Sylvain Carette</a>" by email.
I tried to find "<a href=
"mailto:hexapod@%28no-spam%29netcom.com">hexapod@(no-spam)netcom.com</a>" who seemed to have maintained
this (as others) for a while, but the site at netcom.com doesn't exist anymore,
emails bounce.  Since I (and colleques) wasted quite some time figuring out
what was wrong with some of the algorithms given in the earlier versions of
this document, I decided to correct it and put it back on the web.

The formerly given sites for the location of these documents do
not exist anymore:
  ftp://ftp.netcom.com/pub/he/hexapod/index.html
  http://www.glue.umd.edu/~rsrodger


Versions, dates and links to local copies (so you can compare):
<a href=
"http://web.archive.org/web/20041011193859/http://www.j3d.org/matrix_faq/vectfaq_1.03.html">vectfaq_1.03.html: Version 1.3  17th March 1998</a>
<a href=
"http://web.archive.org/web/20041011193859/http://www.j3d.org/matrix_faq/vectfaq_1.04.html">vectfaq_1.04.html: Version 1.4  28th December 2001</a>

Please refrain from asking me math questions. I am only maintaining this FAQ
and have very little knowledge about the subject. But, if you have a
question that is not answered by this FAQ and later happen to find the
answer and believe it to be relevant for this FAQ (or its readers), please
send all relevant information, hopefully in a pre-digested form, to me to
be included here. Thanks!
If you prefer to appear as "anonymous" in the contributions list, let me
know, otherwise I'll just put you down with whatever name I can gather from
your email header.



Questions
---------


COORDINATE SYSTEMS
==================

<a href=
"#Q1">Q1.  What is a coordinate system?</a>
<a href=
"#Q2">Q2.  What is a point?</a>
<a href=
"#Q3">Q3.  What is a origin?</a>
<a href=
"#Q4">Q4.  What is a vector?</a>
<a href=
"#Q5">Q5.  What is a column vector?</a>
<a href=
"#Q6">Q6.  What is a row vector?</a>
<a href=
"#Q7">Q7.  What is a vertex?</a>
<a href=
"#Q8">Q8.  What are homogeneous coordinates?</a>
<a href=
"#Q9">Q9.  What is the Euclidean coordinate system?</a>
<a href=
"#Q10">Q10. What is the Polar coordinate system?</a>
<a href=
"#Q11">Q11. How do I display Polar coordinates?</a>
<a href=
"#Q12">Q12. What are right-handed and left-handed coordinate systems?</a>
<a href=
"#Q13">Q13. Which is the best coordinate system to use?</a>
<a href=
"#Q14">Q14. How do rotation angles relate to coordinate systems?</a>
<a href=
"#Q15">Q15. What is a global coordinate system?</a>
<a href=
"#Q16">Q16. What is a local coordinate system?</a>
<a href=
"#Q17">Q17. How do I convert Euclidean to Polar coordinates?</a>
<a href=
"#Q18">Q18. How do I convert Polar to Euclidean coordinates?</a>
<a href=
"#Q19">Q19. How do I convert between rotation systems?</a>


VECTORS
=======

<a href=
"#Q20">Q20. How do I represent a vector using the C/C++ programming languages?</a>
<a href=
"#Q21">Q21. How do I calculate the length of a vector?</a>
<a href=
"#Q22">Q22. What is the magnitude of a vector?</a>
<a href=
"#Q23">Q23. What is a normalised vector?</a>
<a href=
"#Q24">Q24. How do I normalise a vector?</a>
<a href=
"#Q25">Q25. What is an unit vector?</a>
<a href=
"#Q26">Q26. What is a direction vector?</a>
<a href=
"#Q27">Q27. What is an outward normal?</a>
<a href=
"#Q28">Q28. What is a dot product?</a>
<a href=
"#Q29">Q29. How do I determine the angle between two vectors?</a>
<a href=
"#Q30">Q30. What is a cross product?</a>
<a href=
"#Q31">Q31. How do I add two vectors?</a>
<a href=
"#Q32">Q32. How do I subtract two vectors?</a>
<a href=
"#Q33">Q33. How do I scale a vector?</a>
<a href=
"#Q34">Q34. How do I perform linear interpolation between two vectors?</a>
<a href=
"#Q35">Q35. How do I perform cubic interpolation between four vectors?</a>


PLANES
======

<a href=
"#Q36">Q36. What is a plane equation?</a>
<a href=
"#Q37">Q37. How do I evaluate a point relative to a plane?</a>
<a href=
"#Q38">Q38. How do I find the point of intersection with a between and a plane?</a>
<a href=
"#Q39">Q39. How do I calculate the reflection of a vector from a plane equation?</a>
<a href=
"#Q40">Q40. How is the reflection of a vector equation derived?</a>
<a href=
"#Q41">Q41. How do I calculate the acceleration of an object on a sloping surface?</a>


DEFORMATION PATCHES
===================

<a href=
"#Q42">Q42. What are deformation patches?</a>
<a href=
"#Q43">Q43. What are linear deformation patches?</a>
<a href=
"#Q44">Q44. How do I perform linear deformation?</a>
<a href=
"#Q45">Q45. How do I implement a linear deformation system?</a>
<a href=
"#Q46">Q46. How do I define a cubic deformation patch?</a>
<a href=
"#Q47">Q47. How do I evaluate a deformation patch?</a>
<a href=
"#Q48">Q48. How do I implement a deformation patch system?</a>
<a href=
"#Q47">Q49. How can I use keyframe animation with deformation patches?</a>


Answers
-------

COORDINATE SYSTEMS
==================

<a name="Q1" id="Q1">Q1</a>.  What is a coordinate system?
---------------------------------

  A coordinate system is a way of defining multi-dimensional space so that
  every individual point in space can be referenced uniquely.

  Several types of coordinate systems exist. These include the following:

    o Euclidean coordinate system

    o Polar coordinate system

  A coordinate system may exist in one, two, three or more dimensions.

  A one dimensional coordinate system defines a set of coordinates along
  a single straight line.

  A two dimensional coordinate system defines a flat rectangular space.
  This requires a pair of coordinates.

  A three dimensional coordinate system defines a solid box. This requires
  a triplet of coordinates.

  A coordinate system using four or more dimensions requires some
  imagination in order to be visualised. Several method exist to handle
  this situation.

  With four to six dimensions, the first three coordinates can be used to
  define standard 3D Euclidean space. The remaining three coordinates
  can be converted into a set of RGB color values. This system is used
  in CAT or NMR scanners. The first three dimensions are the position of
  the patients body. The fourth dimension defines the signal intensity
  for an individual voxel or point in the patients body.


<a name="Q2" id="Q2">Q2</a>.  What is a point?
---------------------

  A point is an absolute position in space. It measures the displacement
  of the point along each axis or dimension of the coordinate system.


<a name="Q3" id="Q3">Q3</a>.  What is a origin?
----------------------

  The origin is the point within the coordinate system, where the
  displacement along each axis or dimension is equal to zero.

  For example, with the Euclidean coordinate system, the point (0,0,0)
  is the origin.


<a name="Q4" id="Q4">Q4</a>.  What is a vector?
----------------------

  Mathematically speaking, a vector differs from a point in that it
  defines the displacement between two points rather than the
  physical location of an actual point in space.

  A point does not define a direction, while a vector does.

  However, a vector between the origin and a point in space, has exactly
  the same coordinates.


<a name="Q5" id="Q5">Q5</a>.  What is a column vector?
------------------------------

  By convention, two dimensional and three dimensional vectors are
  represented as a single vertical column of numeric values ie:


        | x |                   | x |
    V = |   |               V = | y |
        | y |                   | z |

  Two dimensions            Three dimensions

  A list of vectors (eg. the geometry of a 3D model) is represented
  simply by adding additional columns ie.

        | x1 x2 x3 ... xN |
    V = | y1 y2 y4 ... yN |
        | z1 z2 z4 ... zN |

<a name="Q6" id="Q6">Q6</a>.  What is row vector?
------------------------

  For problem-solving, a vector may be described as V = (x,y,z) during
  the specification of a problem.

  This is a row vector. However, row-vectors should not really be used
  with any mathematical descriptions.


<a name="Q7" id="Q7">Q7</a>.  What is a vertex?
----------------------

  A vertex is another name for a point. However, it used specifically
  when referring to a group of points arranged into a geometric shape.


<a name="Q8" id="Q8">Q8</a>.  What are homogeneous coordinates?
--------------------------------------

  Homogenous coordinates are used in order to implement perspective depth
  projection operations using matrices. With ordinary matrix multiplication
  it is not possible to divide columns of a matrix by the value of a
  particular element ie. Dividing X and Y by Z.

  Homogeneous coordinates get around this problem by defining an additional
  coordinate W. When vectors are normally defined, this value is always
  set to 1.0. Because, of this, it is not usually necessary to store this
  value with 3D coordinates and vectors.

  The use of this coordinate is the reason why all projection matrices are
  4x4 in size.

  When a 3D vector is multiplied with a projection matrix, the W
  coordinate gets multiplied alongside XYZ. The resulting value is
  then used to divide each of X,Y and Z.

  A simple perspective matrix will set the value of W to Z.


<a name="Q9" id="Q9">Q9</a>.  What is the Euclidean coordinate system?
---------------------------------------------

  Euclidean coordinates can range from 1 to N dimension. Each dimension
  is always perpendicular to all the others. Two and three dimensions
  are most commonly used by game systems.

  In a two dimensional system, each position is defined by two coordinates
  X and Y. A two-dimensional system is as follows:

    +-------------------+
    |                   |
    |       +Y          |
    |                   |
    |        o          |
    |        |          |
    |        |          |
    |        |          |
    |        |          |
    |    ....o----o +X  |
    |        .          |
    |        .          |
    |        .          |
    |        .          |
    |                   |
    +-------------------+

  In a three dimensional system, an additional Z coordinate is added.

    +-------------------+
    |                   |
    |       +Y          |
    |                   |
    |        o          |
    |        |          |
    |        |          |
    |        |          |
    |        |          |
    |    ....o----o +X  |
    |       /.          |
    |      / .          |
    |     /  .          |
    | +Z o   .          |
    |                   |
    +-------------------+

  For example, a football field can be represented as a coordinate system.
  The  centre point is the origin. The X axis is the centre line, the Z
  axis is the direction from one goal to another and the Y axis is the
  height of the football from the ground.

  The Euclidean coordinate system can also be extended into four or more
  dimensions.

  For example, in a flight simulator game, it may be useful to keep track
  of the flight path of an aeroplane. In this case, the fourth dimension
  actually defines time.


<a name="Q10" id="Q10">Q10</a>. What is the Polar coordinate system?
-----------------------------------------

  The Polar coordinate system differs from the Euclidean coordinate system
  in that each point in space is defined in terms of its position and
  distance from a sphere with unit radius.

  The centre of the sphere is the origin . The first two coordinates
  define longitude and latitude on the sphere. In effect they wrap a two
  dimensional coordinate system onto the surface of the sphere.

  The third coordinate defines the distance of the point from the centre
  of the sphere.

  Each point defines a triplet of values (latitude, longitude and height).
  Latitude ranges from +90 to -90. Longitude ranges from  -180 to +180, and
  height range from 0 to infinity. Height can be negative.

  ie. ( +90, --, +r ) defines the North Pole.

      ( -90, --, -r ) defines the South Pole.

      (   0,  0,  r ) is a point on the equator.


<a name="Q11" id="Q11">Q11</a>. How do I display Polar coordinates?
----------------------------------------

  Longitude and Latitude can be displayed as floating point values or
  as degrees, minutes and seconds (and even arc-seconds).

  These angles are represented in the format

       o
     dd  mm' ss"

  where dd ranges from -180 to 180,
        mm ranges from 0 to 59,
    and ss ranges from 0 to 59.

  dd defines the integer number of degrees, while mm and ss take the
  fractional part and scale it into two other integers ie:

    ----------------------------------

    frac = modf( angle, &amp;dd ) * 3600.0

    ss   = frac % 60

    mm   = frac - ss

    ----------------------------------


<a name="Q12" id=
"Q12">Q12</a>.  What are right-handed and left-handed coordinate systems?
---------------------------------------------------------------

  When working with coordinates in the Euclidean coordinate system
  there are two possible ways of arranging the three XYZ coordinate
  axii.

  One way is to have the positive Z-axis point outwards of the screen.
  This is referred to as the "right-handed coordinate system" and is
  the system preferred by mathematicians.

  The more negative a coordinate is, the further back into the screen it
  appears. Coordinates with positive values are behind the observer.

  Alternatively, the positive Z-axis can be made to point into the
  screen. This is referred to as the "left-handed coordinate system".

  This is opposite to the right-handed coordinate system. The more
  positive a coordinate is, the further back into the screen it appears.
  Coordinates with positive values are behind the observer.

   Left-handed coordinate system    Right-handed coordinate system
  +-----------------------------+   +------------------------------+
  |                             |   |                              |
  |             +Y              |   |           +Y                 |
  |              ^              |   |            ^                 |
  |              |      +Z      |   |            |                 |
  |              |   -o         |   |            |    .            |
  |              |   /|         |   |            |   .             |
  |              |  /           |   |            |  .              |
  |              | /            |   |            | .               |
  |              |/             |   |            |.                |
  |       .......o-------&gt; +X   |   |     .......o-------&gt; +X      |
  |             ..              |   |           /.                 |
  |            . .              |   |          / .                 |
  |           .  .              |   |         /  .                 |
  |          .   .              |   |       |/   .                 |
  |         .    .              |   |       o-   .                 |
  |              .              |   |            .                 |
  |              .              |   |     +Z     .                 |
  |                             |   |                              |
  +-----------------------------+   +------------------------------+

  If the direction of the Y-axis is reversed, then whichever coordinate
  system is currently in use becomes the direct opposite.

  OpenGl and XGL use the right-handed coordinate system. Direct3D uses
  the left-handed coordinate system.

  The terms "left-handed" and "right-handed" are
  derived from the way you can use your thumb, index and middle fingers
  to model the
  selected coordinate systems.

  If you point the index finger of your right hand in the direction of
  the Z-axis, then your right thumb points in the direction of the Y-axis
  and your right middle finger points in the direction of the X-axis.

  If the direction of the Z-axis is reversed (ie. pointing into the
  screen) then this is defined as a "left-handed" coordinate system.
  This is because your left thumb now points in the direction of the
  Y-axis and your left middle finger nows points in the direction of
  the X-axis.


<a name="Q13" id="Q13">Q13</a>. Which is the best coordinate system to use?
------------------------------------------------

  In practical use, there is no particular advantage that either the
  left-handed or right-hand coordinatee systems has over the other.
  The main reason for choosing one system over the other is purely
  a matter of convenience.

  Such reasons might include maintaining compatability with the
  underlying 3D API or geographical coordinate system. For example
  OpenGL uses a right-handed coordinate system, while Direct 3D uses
  a left-handed coordinate system.

  For an aircraft simulator, it is convenient to "map" the geographical
  longitude with the X-axis, geographical latitude with the Y-axis and
  height (or depth) with the Z-axis. When combined together, all three
  coordinate axii form the right-handed coordinate system, albeit rotated
  -90 degrees in the X-axis.

      Right-handed coordinate system
      for aircraft simulator
     +------------------------------+
     |                              |
     |           +Z                 |
     |            ^      +Y         |
     |            |    -o           |
     |            |    /|           |
     |            |   /             |
     |            |  /              |
     |            | /               |
     |            |/                |
     |     .......o-------&gt; +X      |
     |           ..                 |
     |          . .                 |
     |         .  .                 |
     |        .   .                 |
     |       .    .                 |
     |            .                 |
     |            .                 |
     |                              |
     +------------------------------+

  In the case of a submarine simulator, the Z-axis actually has polarity
  reversed, so that positive values of Z represents increasing depth,
  while the X and Y still represent longitude and latitude respectively.
  Thus, all three coordinate axii form the left-handed coordinate system,
  albeit rotated +90 degrees in the X-axis.


      Left-handed coordinate system
      for submarine simulator
     +-----------------------------+
     |                             |
     |              .              |
     |              .      +Y      |
     |              .   -o         |
     |              .   /|         |
     |              .  /           |
     |              . /            |
     |              ./             |
     |       .......o-------&gt; +X   |
     |             .|              |
     |            . |              |
     |           .  |              |
     |          .   |              |
     |         .    |              |
     |              |              |
     |              V              |
     |             +Z              |
     |                             |
     +-----------------------------+

  For the aircraft simulator, converting coordinates to OpenGL is simply
  a matter of performing a +90 degree rotation in the X-axis.

  Likewise, for the submatine simulator, the conversion to OpeGL is
  simply a matter of performing a -90 degree rotation in the X-axis.



<a name="Q14" id="Q14">Q14</a>. How do rotation angles relate to coordinate systems?
---------------------------------------------------------

  By mathematical convention, a positive rotation angle generates a
  clockwise rotation when looking from the origin towards the positive
  end of the selected rotation axis.

  Given this relationship between rotation angles and coordinate
  systems, it is possible to derive the rotation matrices for each
  rotation axis.


<a name="Q15" id="Q15">Q15</a>. What is a global coordinate system?
----------------------------------------

  Global coordinate system are used to assign the coordinates of all
  points relative to a single common origin.

  For example, when tracking the positions of players in a 3D maze, it
  is convenient to have all players and obstacles assign coordinates
  relative to a single common origin eg. The entrance/exit of the maze.


<a name="Q16" id="Q16">Q16</a>. What is a local coordinate system?
---------------------------------------

  Local coordinate systems are used to assign the coordinates of all
  points relative to one or more origins.

  For example, using the Euclidean coordinate system to animate the
  movement of a multi-jointed robot arm, it is convenient to assign
  each joint separate local coordinate systems.

  The point of rotation of each joint actually becomes the origin of
  the related geometry.

  This allows for the surface geometry of each joint to be transformed
  by the current position of that joint.

  The coordinate system need not always Euclidean. In the case of
  astronomy and tracking the positions of features on the moon or
  other planets, it is necessary to give each planet its own local
  polar coordinates system.

  However, the position of all planets can be defined using a global
  coordinate system, with the Sun being placed at the origin.


<a name="Q17" id="Q17">Q17</a>. How do I convert Euclidean to Polar coordinates?
-----------------------------------------------------

  With a Euclidean coordinate (x y z), the goal is to convert it into a
  Polar coordinate (latitude, longitude, distance).

  The conversion is as follows:

    -----------------------------------------
    distance  = sqrt( x*x + y*y + z*z )

    x        /= distance;
    y        /= distance;
    z        /= distance;

    xz_dist   = sqrt( x*x + z*z )
    latitude  = atan2( xz_dist, y ) * RADIANS
    longitude = atan2( x,       z ) * RADIANS
    -----------------------------------------


<a name="Q18" id="Q18">Q18</a>. How do I convert Polar to Euclidean coordinates?
-----------------------------------------------------

  With a Polar coordinate (latitude, longitude, distance), the goal is to
  convert it into a Euclidean coordinate (x y z).

  The conversion is as follows:

    -----------------------------------------
    x = cos( latitude ) . sin( longitude )
    y = sin( latitude )
    z = cos( latitude ) . cos( longitude )
    -----------------------------------------


<a name="Q19" id="Q19">Q19</a>. How do I convert between rotation systems?
-----------------------------------------------

  Altogether, there are around five different ways in which a rotation
  in three dimensions can be represented:

  These include:

    Euler angles
    Matrices
    Quaternions
    Rotation Axis/Angle
    Spherical Rotation Angles

  Euler angles define each rotation as a combination of rotations in
  each of the three main X, Y and Z axii. Euler angles must be converted
  to matrices before any vertex transformations can be performed.

  Matrices define each rotation as an 2D array of values which are
  multiplied with an array of vertices. They can either be 3x3 or 4x4
  in size.

  Quaternions define each rotation in 4 dimension instead of three. As a
  result they require four floating point values. Quaternions must be
  connverted to matrices before any vertex transformation can be
  performed.

  Rotation Axis/Angles define each rotation as a unit vector along with
  a specifiede rotation angle along that axis. Rotation Axis/Angle pairs
  must be converted into Quaternions before finally being converted into
  a rotation matrix.

  Spherical angles define each rotation in terms of latitude/longitude
  and a rotation angle. They must be converted into a rotation matrix
  through the use of AxisAngle and Quaternion coordinates.


  The conversion paths are as follows:

         +--------------+     +--------------+     +--------------+
         |    Matrix    |&lt;===&gt;|  Quaternion  |&lt;===&gt;|   AxisAngle  |
         +--------------+     +--------------+     +--------------+
                /\                                        /\
                ||                                        ||
                \/                                        \/
         +--------------+                          +--------------+
         | Euler angles |                          |  Spherical   |
         +--------------+                          +--------------+

  A comparision of the various representations is presented below:

    +--------------+------------+---------------------------------------+
    | Data type    | Size       | Usage                                 |
    +--------------+------------+---------------------------------------+
    | Euler Angles | FLOAT * 3  | Must be converted to a matrix         |
    |              |            | Gimbal lock can occur                 |
    +--------------+------------+---------------------------------------+
    | Matrix       | FLOAT * 9  | Can be used directly for vertex       |
    |              | FLOAT * 16 | transformation                        |
    |              |            | 3x3 matrices can be used for rotation |
    |              |            | and scaling only.                     |
    |              |            | 4x4 matrices can be used for both     |
    |              |            | translation and perspective           |
    +--------------+------------+---------------------------------------+
    | Quaternion   | FLOAT * 4  | Must be converted to a matrix         |
    |              |            | No danger of Gimbal lock              |
    +--------------+------------+---------------------------------------+
    | Axis Angle   | FLOAT * 4  | Must be converted to a matrix through |
    |              |            | the use of Quaternions.               |
    |              |            | No danger of Gimbal lock              |
    +--------------+------------+---------------------------------------+
    | Spherical    | FLOAT * 3  | Must be converted to a matrix through |
    |              |            | the use of AxisAngle and Quaternion   |
    |              |            | representations.                      |
    |              |            | No danger of Gimbal lock              |
    +--------------+------------+---------------------------------------+


VECTORS
=======

<a name="Q20" id=
"Q20">Q20</a>. How do I represent a vector using the C/C++ programming languages?
-----------------------------------------------------------------------

  The most convenient way of representing a vector using the C/C++
  programming languages is through the use of a data structure:

    typedef float VFLOAT;

    typedef vector3_st
      {
      VFLOAT vx;
      VFLOAT vy;
      VFLOAT vz;
      } VECTOR3;

  or through the use of arrays:

    typedef VFLOAT VECTOR3[3];


  For convenience and modularity, it is always a good idea to define
  labels for commonly used data types that may vary from system to system.
  Thus floating point values are given the label "VFLOAT".


<a name="Q21" id="Q21">Q21</a>. How do I calculate the length of a vector?
-----------------------------------------------

  The length of a vector is calculated by taking the square root of
  the sum of the squares of each coordinate ie.

  If the vector is defined as (x,y,z) then the length of the vector is
  calculated from:


           ----------------
          /  2    2    2
    L = \/  x  + y  + z


<a name="Q22" id="Q22">Q22</a>. What is the magnitude of a vector?
---------------------------------------

  This is equivalent to the length of a vector.

  Placing a pair of vertical lines around a vector indicates the
  magnitude of the vector.

  eg. If the variable V is used to represent a vector, then the
  expression |V| indicates the magnitude of a vector.


<a name="Q23" id="Q23">Q23</a>. What is a normalised vector?
---------------------------------

  A normalised vector is a vector where the sum of the squares of all
  coordinates is equal to one.

  For example, the vector ( 2, 2, 0 ) is not normalised, while the
  vectors ( 0.707, 0.707, 0.0) and ( 1.0, 0.0, 0.0 ) are normalised.


<a name="Q24" id="Q24">Q24</a>. How do I normalise a vector?
---------------------------------

  A vector can be normalised by calculating the magnitude or length of
  the vector and dividing each coordinate by this value.

  For example, consider the vector

        | 3.0 |
    V = | 4.0 |
        | 0.0 |

  The length of this vector is 5.0

    |V| = 5.0

  Then the value of the normalised vector is given by:

     V    | 3.0 |   1   | 0.6 |
    --- = | 4.0 | . - = | 0.8 |
    |V|   | 0.0 |   5   | 0.0 |


  If the vector is already normalised, then the value of |V| will be
  equal to one, and after division, the vector will remain as before.


<a name="Q25" id="Q25">Q25</a>. What is an unit vector?
----------------------------

  A unit vector is another name for a normalised vector. The sum of the
  squares of all coordinates is equal to one.


<a name="Q26" id="Q26">Q26</a>. What is a direction vector?
--------------------------------

  A direction vector is another name for a vector, but which is
  specifically used for the purpose of determining the direction that
  a polygon surface or vertex is facing.

  However, direction vectors are not necessarily always normalised.

  For example, a direction vector may be used to represent wind direction
  of points within a landscape. The magnitude of the vector is used to
  represent wind speed combined with the direction of the wind.


<a name="Q27" id="Q27">Q27</a>. What is an outward normal?
-------------------------------

  An outward normal is another name for a normalised vector. Similar
  in purpose to a direction vector, an outward normal are used
  specifically for representing the direction that a polygon surface or
  vertex is facing.


<a name="Q28" id="Q28">Q28</a>. What is a dot product?
---------------------------

  The dot product is used to calculate the angle between two vectors.

  If v1 and v2 are two normalised vectors, then the dot product is given
  by the expression:

    v1.v2

  For a pair of three dimension vectors this expression is evaluated
  using the equation:

    d =     v1 . v2

        | x1 |   | x2 |
    d = | y1 | . | y2 |
        | z1 |   | z2 |

    d = x1.x2 + y1.y2 + z1.z2


  This can be represented using the C/C++ programming languages as:

    d = v1.x * v2.x + v1.y * v2.y + v1.z * v2.z

  where * is the standard multiplication operation.

  For efficiency, this function can represented as C #define macros or
  C++ inline class functions.


<a name="Q29" id="Q29">Q29</a>. How do I determine the angle between two vectors?
------------------------------------------------------

  The angle between two normalised vectors can be calculated from the
  mathematical expression:

    cos A = v1.v2

            | x1 |   | x2 |
          = | y1 | . | y2 |
            | z1 |   | z2 |

  where cos is the cosine function,
          A is the angle between the two vectors,
         v1 is the first vector and
         v2 is the second vector

  The expression v1.v2 is the actual dot product

  If the two vectors are not normalised, then the following expression
  can be used:

              v1.v2
    cos A = ---------
             v1 . v2
             --   --

  where -- is the magnitude or length of the vector.

  This takes the dot product of the two vectors, and divides the result
  by the product of the lengths of both vectors.


<a name="Q30" id="Q30">Q30</a>. What is a cross product?
-----------------------------

  The cross product between two normalised vectors is used to determine
  the vector which perpendicular to both the vectors. This is expressed
  as the mathematical expression:

    v3 = v1 x v2

         | x1 |   | x2 |
    v3 = | y1 | x | y2 |
         | z1 |   | z2 |

         | y1.z2 + z1.y2 |
    v3 = | z1.x2 + x1.z2 |
         | x1.y2 + y1.x2 |

  This can be represented using the C/C++ programming languages as:

    v3.vx = v1.y * v2.z + v1.z * v2.y
    v3.vy = v1.z * v2.x + v1.x * v2.z
    v3.vz = v1.x * v2.y + v1.y * v2.x

  For efficiency, this function can represented as C #define macros or
  C++ inline class functions.


<a name="Q31" id="Q31">Q31</a>. How do I add two vectors?
------------------------------

  Adding two vectors together is very simple to perform. This is achieved
  by adding together the individual coordinates of each vector. The
  operation is defined by the following mathematical expression:

    v3 = v1 + v2

         | x1 |   | x2 |
    v3 = | y1 | + | y2 |
         | z1 |   | z2 |

         | x1 + x2 |
    v3 = | y1 + y2 |
         | z1 + z2 |

  This can be represented using the C/C++ programming languages as:

    v3.vx = v1.vx + v2.vx
    v3.vy = v1.vy + v2.vy
    v3.vz = v1.vz + v2.vz

  For efficiency, this function can represented as C #define macros or
  C++ inline class functions.


<a name="Q32" id="Q32">Q32</a>. How do I subtract two vectors?
-----------------------------------

  Subtraction is performed in the same way as addition. This is achieved
  by subtracting the individual coordinates of each vector. The
  operation is defined by the following mathematical expression:

    v3 = v1 - v2

         | x1 |   | x2 |
    v3 = | y1 | - | y2 |
         | z1 |   | z2 |

         | x1 - x2 |
    v3 = | y1 - y2 |
         | z1 - z2 |

  This can be represented using the C/C++ programming languages as:

    v3.vx = v1.vx - v2.vx
    v3.vy = v1.vy - v2.vy
    v3.vz = v1.vz - v2.vz

  For efficiency, this function can represented as C #define macros or
  C++ inline class functions.


<a name="Q33" id="Q33">Q33</a>. How do I scale a vector?
-----------------------------

  A vector can be scaled (enlarged or reduced) in a way similar to
  multiplication. This is achieved by multiplying each coordinate by the
  same scaling factor. The mathematical expression for this is as follows:

    v2 = v1 . S

         | x1 |
    v3 = | y1 | . S
         | z1 |

         | x1.S |
    v3 = | y1.S |
         | z1.S |

  This can be represented using the C/C++ programming languages as:

    v3.vx = v1.vx * S
    v3.vy = v1.vy * S
    v3.vz = v1.vz * S

  For efficiency, this function can represented as C #define macros or
  C++ inline class functions.


<a name="Q34" id=
"Q34">Q34</a>. How do I perform linear interpolation between two vectors?
---------------------------------------------------------------

  For many 3D applications, it is sometimes necessary to perform linear
  interpolation between two vectors. Such applications can include view
  frustum clipping and morphing.

  Linear interpolation is implemented by taking the coordinates of two
  known points and scaling them in such a way as to generate a series
  of points that forms a straight line between them.

  This equation is sometimes referred to as a blending function. For
  linear interpolation this equations is as follows:

    V' = (1-t).Va + t.Vb

    V' = Va + t.(Vb-Va)

  The second form is more commonly used as it only requires a single
  multiplication operation.

  This is implemented using the following set of vector operations:

  Using the C programming language:

  void v3_linear( VECTOR3 *vr, VECTOR3 *va, VECTOR3 *vb, VFLOAT t )
    {
    v3_sub(    &amp;vtemp,   vb, va    );
    v3_scalef( &amp;vtemp,  &amp;vtemp, t  );
    v3_add(    &amp;vr,     &amp;vtemp, va );
    }

<a name="Q35" id=
"Q35">Q35</a>. How do I perform cubic interpolation between four vectors?
---------------------------------------------------------------

  Given four vectors, the problem is to find a way  of determining
  intermediate positions specified by a parametric variable t.

  This can be achieved by making use of cubic interpolation. The set
  of four vectors is combined into a single geometry vector G.
  Through the use of spline mathematics, this geometry vector is
  converted into an interpolation matrix M.

  If the geometry vector is defined as:

         | x1 x2 x3 x4 |
     G = | y1 y2 y3 y4 |
         | z1 z2 z3 z4 |

  Then multiplication by the base matrix:

         |  -4.5    9.0  -5.5  1.0  |
    Mb = |  13.5  -22.5   9.0  0.0  |
         | -13.5   18.0  -4.5  0.0  |
         |   4.5   -4.5   1.0  0.0  |

  will generate the 3x4 interpolation matrix Mi:

    Mi = G .Mb

  This can be implemented through a modified matrix-vector multiplication:

    m4_multspline( m_cubic, v_geom, v_source );

  Interpolation can then be performed by the use of the parametric
  variable t:

        R  = Mi . t

                           |t^3|
    | xr |   | A B C D |   |t^2|
    | yr | = | E F G H | . |t  |
    | zr |   | I J K L |   |1  |

  This can be implemented through a modified cubic interpolation
  algorithm:

    v3_cubic( vr, v_geom, t );

  The resulting vector can then be used as required.

  The function m4_multspline is implemented as follows:

    -------------------------

    void m4_multspline( MATRIX4 mat, VECTOR3 *vsrc, VECTOR3 *vdst )
      {
      VFLOAT tx, ty, tz;
      int    n;

      for ( n = 0; n &lt; 4; n++ )
        {
        vdst[n].vx = vsrc[0].vx * mat[n]
                   + vsrc[1].vx * mat[n+4]
                   + vsrc[2].vx * mat[n+8]
                   + vsrc[3].vx * mat[n+12];

        vdst[n].vy = vsrc[0].vy * mat[n]
                   + vsrc[1].vy * mat[n+4]
                   + vsrc[2].vy * mat[n+8]
                   + vsrc[3].vy * mat[n+12];

        vdst[n].vz = vsrc[0].vz * mat[n]
                   + vsrc[1].vz * mat[n+4]
                   + vsrc[2].vz * mat[n+8]
                   + vsrc[3].vz * mat[n+12];
        }
      }

    -------------------------

  The function v3_cubic is implemented as follows:

    -------------------------

    void v3_cubic( VECTOR3 *vpos, VECTOR3 *vdst, VFLOAT t )
      {
      vpos -&gt; vx = ((vdst[0].vx*t+vdst[1].vx)*t+vdst[2].vx)*t+vdst[3].vx;
      vpos -&gt; vy = ((vdst[0].vy*t+vdst[1].vy)*t+vdst[2].vy)*t+vdst[3].vy;
      vpos -&gt; vz = ((vdst[0].vz*t+vdst[1].vz)*t+vdst[2].vz)*t+vdst[3].vz;
      }

    -------------------------

  In fact, a cubic spline surface can be generated from the combination
  of these two algorithms:

    -------------------------

    void cubic_patch( VECTOR3 *vlist, VECTOR3 *vsurf, int hdiv, int vdiv )
      {
      MATRIX4 mh_geom[4];
      VECTOR3 mv_geom[4], mv_interp[4];
      VFLOAT  du, dv;
      int     n, u, v;

      if ( hdiv &lt; 1 || vdiv &lt; 1 )             /* Not enough subdivisions? */
        return;                               /* No, so return            */

      for ( n = 0; n &lt; 4; n++ )                        /* Horiz. interp   */
        m4_multspline( m_cubic, vsurf+n*4,mh_geom[n]); /* Make I-matrix   */

      for ( u = 0; u &lt;= hdiv; u++ )                    /* For each column */
        {
        for ( n = 0; n &lt; 4; n++ )
          v3_cubic( mv_geom+n, mh_geom[n], (VFLOAT) u/hdiv );

        m4_multspline( m_cubic, mv_geom, mv_interp );  /* Make I-matrix   */

        for ( v = 0; v &lt;= vdiv; v++, vlist++ )         /* For each row    */
          v3_cubic( vlist,mv_interp,(VFLOAT) v/vdiv ); /* Save vertex     */
        }
      }

    -------------------------


PLANES
======

<a name="Q36" id="Q36">Q36</a>. What is a plane equation?
------------------------------

  Plane equations are widely used in the field of 3D animation to
  define and manipulate polygon surfaces. Plane equations are used to
  implement back face culling, view frustum culling, clipping and
  collision detection.

  The plane equation or "equation of the plane" is a mathematical
  expression as follows:

    Ax + By + Cz + D = 0

  where A, B, C and D are known constants and (x,y,z) specifies any
  point in three-dimensional space.


<a name="Q37" id="Q37">Q37</a>. How do I evaluate a point relative to a plane?
---------------------------------------------------

  The position of a point relative to a plane is determined by
  evaluating the plane equation ie. Multiplying each coordinate (x,y,z)
  with the associated parameters (A,B,C) and adding D.

  If the evaluation of a point with the plane equation generates a
  positive value then the point is said to be "in front of the plane".

  If the evaluation generates a result which is negative, then the point
  is said to be "behind the plane".

  Otherwise, if the evaluation generates a result which is exactly
  zero, then the point is said to be "on the plane".

  The values of A,B and C actually define the outward normal of the
  surface. As such, the sum of the squares of these values will always
  add up to one ie.

     2    2    2
    A  + B  + C  - 1 = 0

  In fact, the evaluation of a point relative to the plane is actually
  a dot product calculation.


<a name="Q38" id=
"Q38">Q38</a>. How do I find the point of intersection with a line and a plane?
------------------------------------------------------------------------

  For computer animation purpose, it is often convenient to determine
  where a straight 3D line intersects a polygon surface. The polygon
  surface is represented as a plane equation.


  The 3D line may be specified in two possible ways:

    o starting and finishing points ( Vs, Vf )

    o starting point and direction vector ( Vs, Vd )

  If only a starting point and a direction vector are known, then
  a dummy end point is calculated by adding the direction vector to
  the starting point ie:

    Vf = Vs + Vd

  This parameter can then be used in the algorithm defined as follows:

  In the case that both starting and finishing points are known, it is
  possible to determine the point of intersection by evaluating both
  points relative to the plane equation and interpolating ie.

    Es = P( Vs )
    Ef = P( Vf )

  Using these two values as weighting factors, it is possible to
  interpolate between the two endpoints.

  The weighting factor for the two points is evaluated as follows:

          Es             Ef
    Ws = -----     Wf = -----
         Ef-Es          Ef-Es


  Then the point of intersection is calculated as follows:

    Vp = Ws.Vs + Wf.Vf


<a name="Q39" id=
"Q39">Q39</a>. How do I calculate the reflection of a vector from a plane equation?
-------------------------------------------------------------------------

  In order to perform calculations such as a light reflecting off a
  reflective surface, it is necessary to be able to calculate the
  reflection of a vector off a plane.

  The plane is represented as an outward normal.

  The mathematical expression for the reflection of a vector is
  given by:

    V' = 2N.(V.N) - V

  where the known (and unknown) parameters are as follows:

    N  = outward normal for the plane
    V  = unit vector of light ray
    V' = unknown unit vector of reflected light ray


<a name="Q40" id="Q40">Q40</a>. How is the reflection of a vector equation derived?
--------------------------------------------------------

  The reflection of a vector is visualised by the following drawing:

               N
               ^
          V    |    V'
           |-  |  -|
           |\  |  /|
             \ | /
              \|/
         ------o-------

  where:

    V  is the original direction vector

    V' is the reflection direction vector, and

    N  is the outward normal of the plane

  The angle between the vector V and N is given by the dot product ie.

    cos(angle) = V.N

  So the expression must have a component V.N within it

  Then the following angles are known:

    At V.N =  0, V' = -V

    At V.N =  1, V' =  N

    At V.N = -1, V' = -N

  Since V.N = 1 gives N and V.N = -1, gives -N, this indicates that the
  component V.N is multiplied by N, ie.

    V' = f( N.(V.N) )

  where f() is the evalation function (not completely known).

  However, if V.N=0 then a result of -V is given.
  Therefore, there must also be a -V component ie.

    V' = f( N.(V.N) - V )

  But, since at V=N, V.N=1, this equation would cancel out completely.
  Thus, one of the parameters must be scaled by a factor of two.

  Then, the final equation is given by:

    V' = 2N.(V.N) - V

  This can be implemented using the vector library as follows:

    ----------------------

    void v3_reflect( VECTOR3 *vreflect, VECTOR3 *vdir, VECTOR3 *vnormal )
      {
      VFLOAT  angle;
      VECTOR3 vtemp;

      angle = v3_dot( vreflect, vnormal ) * 2;

      v3_scale( &amp;vreflect,  vnormal,  angle   );
      v3_sub(   &amp;vreflect, &amp;vreflect, vnormal );
      }

    ----------------------


<a name="Q41" id=
"Q41">Q41</a>. How do I calculate the acceleration of an object on a sloping surface?
---------------------------------------------------------------------------

  In the real world, when an object moves onto a sloping surface, it
  experiences acceleration forces due to gravity. However, because of the
  existence of the sloping surface, the acceleration will not be directly
  in the direction towards the gravitational source. Examples include a
  football rolling down a hill and a person sliding down a mudslide.

  In a virtual 3D environment, the position of an object is represented
  as a vector coordinate, the sloping surface as a plane equation and
  gravity is as a direction vector.

  The problem can then be defined as combining these parameters together
  in order to determine the acceleration force, which is represented as a
  direction vector.

  The following parameters are known:

    Vo = Position vector of the object

    Vg = Direction vector of gravity

    Vp = Outward normal of the current slope polygon


  Only the following parameter is unknown:

    Va = Direction vector of acceleration forces


  This can be visualised as follows:

    -----------------------------------------------

                    Vp = Outward normal of polygon
                 --
          \      /|
           \    /
            \  /
             \O
              |\
              |\\
              | \\| Va = Acceleration force
              |  \-
              V   \

       Vg = Gravity

    -----------------------------------------------

  Then the calculation is as follows:

    Axis of rotation of a rolling object is given by:

      Vt = Vg x Vp

    Then the direction vector representing the acceleration force is
    given by:

      Va = Vt x Vp


  This can be implemented using the 3D vector library as follows:

    -------------------------------

     void v3_slope( VECTOR3 *va, VECTOR3 *vr, VECTOR3 *vg, VECTOR3 *vp )
       {
       v3_cross( &amp;vr, vg, vp );
       v3_cross( &amp;va, vt, vp );
       }

    -------------------------------


DEFORMATION PATCHES
===================

<a name="Q42" id="Q42">Q42</a>. What are deformation patches?
----------------------------------

  Deformation patches are a means of modifying the shape of an object
  while preserving the connectivity of all the geometry. They attempt
  to warp the local coordinate system of an object so that straight
  lines can become curved lines and vice versa.

  Applications of deformation patches includes special effects and
  character animation. An inanimate object can be made to twist around,
  shrink away from a threatening object and even shuffle or tip-toe
  about. For a really trippy effect, a camera can be made to move
  through an architectural model, while the geometry of the model is
  warped using a deformation patch.

  In the real world (using stop-go animation and clay), deformation of
  an object can be implemented through the use of reshaping, adding or
  removing clay.

  However, when animating by computer, using clay is not an option.
  Instead, surface are modelled using either polygons defined from
  vertices or surfaces defined using spline curves and control points.

  By warping the positions of these vertices and control points, it is
  possible to deform the shape of the object by modifying the local
  coordinate system, while still preserving the connectivity of the
  geometry.

  Warping or "deforming" of the geometry can be implemented using either
  linear or cubic interpolation. Linear interpolation offers considerable
  performance advantages over cubic interpolation, at the sacrifice of
  control over the way the geometry deforms.


<a name="Q43" id="Q43">Q43</a>. What are linear deformation patches?
-----------------------------------------

  Linear deformation patches are a low-budget version of cubic
  deformation patches. Instead of using cubic interpolation, linear
  interpolation only makes use of linear interpolation of vectors.

  As a result, only eight control points are required, instead of the
  full complement of sixty-four. However, the control points are still
  arranged in the shape of a cube.


<a name="Q44" id="Q44">Q44</a>. How do I perform linear deformation?
-----------------------------------------

  Once the bounding volume and control points have been defined, the
  next stage is to evaluate the new coordinates of each vertex.

  Each coordinate of the original object is converted into a parametric
  form based on the limits of the bounding volume.

  If the limits of the bounding volume are defined by:

          | Xlo |                 | Xhi |
    Min = | Ylo |    and    Max = | Yhi |
          | Zlo |                 | Zhi |

  Then a point P can be converted to parametric form:

        | X |
    P = | Y |
        | Z |

  Then the parameteric version of P can be calculated from:

         |  X - Xlo  |
         | --------- |
         | Xhi - Xlo |
         |           |
         |  Y - Ylo  |
    P' = | --------- |
         | Yhi - Ylo |
         |           |
         |  Z - Zlo  |
         | --------- |
         | Zhi - Zlo |

  This parametric coordinate can then be used as input to the evaluation
  stage.

  Because the deformation patch exists in three dimensions, this requires
  interpolation through three levels of spline curves:

  +---------------------------------------------------------------------+
  |                                                                     |
  |     Level 1              Level 2             Level 3                |
  |                                                                     |
  |   O------O               ..O..                                      |
  |   ..     ..                |.                                       |
  |   . .    . .               | .                .                     |
  |   .  .   .  .              |  .               .              .      |
  |   .   O------O   P'.X      | ..O..  P'.Y      O     P'.Z      .     |
  |   .   .  .   .   =====&gt;    |   |    =====&gt;    .\    =====&gt;     O    |
  |   .   .  .   .             |   |              . \ .             .   |
  |   .   .  .   .             |   |                 \.              .  |
  |   O---.--O   .           ..O.. |                  O                 |
  |    .  .   .  .              .  |                  .                 |
  |     . .    . .               . |                  .                 |
  |      ..     ..                .|                                    |
  |       O------O               ..O..                                  |
  |                                                                     |
  +---------------------------------------------------------------------+

  The first level is defined from four interpolation lines, each of
  which is defined from pair of control points in the X-axis.

  Substituting in the X-axis parametric coordinate from P' generates
  a new set of 4 control points.

  These are used to generate two interpolation lines in the Y-axis.

  Substituting in the Y-axis parameteric coordinate from P' generates
  a new set of 2 control points.

  These are used to generate a single interpolation line in the Z-axis.

  Substituting in the Z-axis parametric coordinate from P' generates
  a single coordinate.

  This coordinate is in fact the final warped position of the point P.

  Each vertex or control point of the model is processed in this manner
  until all every coordinate has been processed.


<a name="Q45" id="Q45">Q45</a>. How do I implement a linear deformation system?
----------------------------------------------------

  Implementation of a deformation patch system requires three sets of
  input parameters. These include the following:

    o Model geometry

    o Original bounding cube

    o Deformation patch (8 control points)

  The evaluation function, must then accept a set of vertex data as
  input (these might even be control points of a NURBS mesh!), and
  produce a modified set of vertex data as output.

  For efficiency, the default ordering of the control points of the
  deformation patch is X-minor, Z-major, ie. Vertices on the same
  X-axis row are placed next to each other in memory ie.

              | X1 X2 X1 X2 X1 X2 X1 X2 |
    Mdeform = | Y1 Y1 Y2 Y2 Y1 Y1 Y2 Y2 |
              | Z1 Z1 Z1 Z1 Z2 Z2 Z2 Z2 |

  The first stage of linear interpolation will convert each pair of
  control points into a single coordinate.

  By substituting in the parametric X coordinate and evaluating, a set
  of four coordinates are generated:

          | Xp Xp Xp Xp |
    Mdx = | Y1 Y2 Y1 Y2 |
          | Z1 Z1 Z2 Z2 |

  As with the first stage, the parametric Y coordinate is substituted
  and evaluated. This generates a pair of coordinates.

          | Xp Xp |
    Mdy = | Yp Yp |
          | Z1 Z2 |

  Finally, these are converted into a interpolation matrix, and the
  parametric Z coordinate is substituted and evaluated. This generates
  a single coordinate

          | Xp |
    Mdz = | Yp |
          | Zp |

  This is the final processed coordinate.

  A complete routine to perform this is as follows:

  The following parameters are used:

    vnum    - number of vertices to be processed
    vsrc    - source vertex data
    vdst    - processed vertex data
    vlimits - bounding volume for deformation patch
    vdeform - control points for deformation patch (64)

  ------------------------------------------------------

  void lpatch_evaluate( VECTOR3 *vdst, int vnum, VECTOR3 *vsrc,
                        VECTOR3 *vlimits,        VECTOR3 *vdeform )
    {
    VECTOR3  v_diff, vparam, v_ymesh[4], v_zmesh[2];
    int      n, m;

    v3_sub( &amp;v_diff, vlimits+1, vlimits );             /* Scale for box   */

    for ( n = 0; n &lt; vnum; n++ )                       /* For each vertex */
      {
      v3_sub( &amp;vparam,  vsrc+n, vlimits );             /* Get parametric  */
      v3_div( &amp;vparam, &amp;vparam, &amp;v_diff  );            /* coordinates     */

      for ( m = 0; m &lt; 4; m++ )                        /* Get Y-axis mesh */
        v3_linear( v_ymesh+m, vdeform+m*2, vdeform+m*2+1, vparam.vx );

      for ( m = 0; m &lt; 2; m++ )                        /* Get Z-axis mesh */
        v3_linear( v_zmesh+m, v_ymesh+m*2, v_ymesh+m*2+1, vparam.vy );

      v3_linear( vdst+n, v_zmesh, v_zmesh+1, vparam.vz ); /* Final coord. */
      }
    }

  ------------------------------------------------------

<a name="Q46" id="Q46">Q46</a>. How do I define a cubic deformation patch?
-----------------------------------------------

  A cubic deformation patch is defined as a set of spline curve control
  points arranged in the shape of a cube. Modification of the cubic
  deformation patch is performed by repositioning groups of control points.

  Since a minimum of four points are required to define a spline curve,
  a cubic deformation patch requires at least sixty-four control points.
  Each control point is represented as a single 3D vector.

  It is also necessary to define a bounding volume which contains the
  area of coordinate space which is to be deformed.

  Thus, a single deformation patch can be defined from less than 70 3D
  vectors or less than 1K of memory.


<a name="Q47" id="Q47">Q47</a>. How do I evaluate a cubic deformation patch?
-------------------------------------------------

  Once the bounding volume and control points have been defined, the
  next stage is to evaluate the new coordinates of each vertex.

  Each coordinate of the original object is converted into a
  parametric form based on the limits of the original bounding volume.

  If the limits of the bounding volume are defined by:

          | Xlo |                 | Xhi |
    Min = | Ylo |    and    Max = | Yhi |
          | Zlo |                 | Zhi |

  Then a point P can be converted to parametric form:

        | X |
    P = | Y |
        | Z |

  Then the parameteric version of P can be calculated from:

         |  X - Xlo  |
         | --------- |
         | Xhi - Xlo |
         |           |
         |  Y - Ylo  |
    P' = | --------- |
         | Yhi - Ylo |
         |           |
         |  Z - Zlo  |
         | --------- |
         | Zhi - Zlo |

  This parametric coordinate can then be used as input to the evaluation
  stage.

  Because the deformation patch exists in three dimensions, this requires
  interpolation through three levels of spline curves:

  +--------------------------------------------------------------------+
  |                                                                    |
  |        Level 1               Level 2      Level 3                  |
  |                                                                    |
  |   o---o---o---o                                                    |
  |   ..   .   .  ..                                                   |
  |   . o---o---o---o                                                  |
  |   .  .   .   ..  .           o                                     |
  |   .   o---o---o---o          |.                                    |
  |   .    .   .  ..   .         | o                                   |
  |   .     o---o---o---o        o |.          o            .          |
  |   .     .     .     .        |.| o          \            .         |
  |   o---o---o---o     .  P'.X  | o |.   P'.Y   o      P'.Z  .        |
  |   ..   ..  .  ..    .        o |.| o          \            .       |
  |   . o---o---o---o   .        |.| o |           o            o      |
  |   .  .  ..   ..  .  .  ===&gt;  | o |.|  ===&gt;      \   ===&gt;     .     |
  |   .   o---o---o---o .        o |.| o             o            .    |
  |   .    ..  .  ..   ..         .| o |                               |
  |   .     o---o---o---o          o |.|                               |
  |   .     .     .     .           .| o                               |
  |   o---o---o---o     .            o |                               |
  |    .   ..  .   .    .             .|                               |
  |     o---o---o---o   .              o                               |
  |      .  ..   .   .  .                                              |
  |       o---o---o---o .                                              |
  |        ..  .   .   ..                                              |
  |         o---o---o---o                                              |
  |                                                                    |
  +--------------------------------------------------------------------+

  The first level is defined from sixteen spline curves, each of which
  is defined from a row of control points in the X-axis.

  Substituting in the X-axis parametric coordinate from P' generates
  a new set of 16 control points.

  These are used to generate four spline curves in the Y-axis.

  Substituting in the Y-axis parameteric coordinate from P' generates
  a new set of 4 control points.

  These are used to generate a single spline path in the Z-axis.

  Substituting in the Z-axis parametric coordinate from P' generates
  a single coordinate.

  This coordinate is in fact the final warped position of the point P.

  Each vertex or control point of the model is processed in this manner
  until all every coordinate has been processed.


<a name="Q48" id="Q48">Q48</a>. How do I implement a cubic deformation patch system?
---------------------------------------------------------

  Implementation of a deformation patch system requires three sets of
  input parameters. These include the following:

    o Model geometry

    o Original bounding cube

    o Deformation patch (64 control points)

  The evaluation function, must then accept a set of vertex data as
  input (these might even be control points of a NURBS mesh!), and
  produce a modified set of vertex data as output.

  For efficiency, the default ordering of the control points of the
  deformation patch is X-minor, Z-major, ie. Vertices on the same
  X-axis row are placed next to each other in memory ie.

              | X1 X2 X3 X4 X1 X2 X3 X4 ... X4 |
    Mdeform = | Y1 Y1 Y1 Y1 Y2 Y2 Y2 Y2 ... Y4 |
              | Z1 Z1 Z1 Z1 Z1 Z1 Z1 Z1 ... Z4 |

  The first stage of cubic interpolation will convert each set of four
  control points into a cubic interpolation matrix.

  By substituting in the parametric X coordinate and evaluating, a set
  of 16 coordinates are generated:

          | X1 X1 X1 X1  X1 X1 X1 X1  X1 X1 X1 X1  X1 X1 X1 X1 |
    Mdx = | Y1 Y2 Y3 Y4  Y1 Y2 Y3 Y4  Y1 Y2 Y3 Y4  Y1 Y2 Y3 Y4 |
          | Z1 Z1 Z1 Z1  Z2 Z2 Z2 Z2  Z3 Z3 Z3 Z3  Z4 Z4 Z4 Z4 |

  As with the first stage, the parametric Y coordinate is substituted
  and evaluated. This generates a set of four coordinates:

          | X1 X1 X1 X1 |
    Mdy = | Y1 Y1 Y1 Y1 |
          | Z1 Z2 Z3 Z4 |

  Finally, these are converted into a interpolation matrix, and the
  parametric Z coordinate is substituted and evaluated. This generates
  a single coordinate

          | X1 |
    Mdz = | Y1 |
          | Z1 |

  This is the final processed coordinate.

  A complete routine to perform this is as follows:

  The following parameters are used:

    vnum    - number of vertices to be processed
    vsrc    - source vertex data
    vdst    - processed vertex data
    vlimits - bounding volume for deformation patch
    vdeform - control points for deformation patch (64)

  ------------------------------------------------------

  typedef VECTOR3 GVECTOR3[4];

  void dpatch_evaluate( VECTOR3 *vdst, int vnum, VECTOR3 *vsrc,
                        VECTOR3 *vlimits,        VECTOR3 *vdeform )
    {
    GVECTOR3 m_xgeom[16],    m_ygeom[4],  m_zgeom;
    VECTOR3  v_diff, vparam, v_ymesh[16], v_zmesh[4];
    int      n, m;

    v3_sub( &amp;v_diff, vlimits+1, vlimits );               /* Scale for box   */

    for ( m = 0; m &lt; 16; m++ )                           /* I-matrix X-axis */
      m4_multspline( m_cubic, vdeform+m*4, m_xgeom[m] );

    for ( n = 0; n &lt; vnum; n++ )                         /* For each vertex */
      {
      v3_sub( &amp;vparam,  vsrc+n, vlimits );               /* Get parametric  */
      v3_div( &amp;vparam, &amp;vparam, &amp;v_diff  );              /* coordinates     */

      for ( m = 0; m &lt; 16; m++ )                         /* Get Y-axis mesh */
        v3_cubic( v_ymesh+m, m_xgeom[m], vparam.vx );

      for ( m = 0; m &lt; 4; m++ )
        {                                                /* I-matrix Y axis */
        m4_multspline( m_cubic, v_ymesh+m*4, m_ygeom[m] );

        v3_cubic( v_zmesh+m, m_ygeom[m], vparam.vy );    /* Get Z-axis mesh */
        }

      m4_multspline(    m_cubic, v_zmesh, m_zgeom );     /* I-matrix Z axis */

      v3_cubic( vdst+n, m_zgeom, vparam.vz );            /* New coordinate  */
      }
    }

  ------------------------------------------------------


<a name="Q49" id="Q49">Q49</a>. How do I use keyframe animation with deformation patches?
--------------------------------------------------------------

  Using the algorithm described above, it is only possible to render
  a single rendered frame.

  In order to implement smooth and continuous animation, it is necessary
  to define more than one deformation patch.

  However, defining and positioning a single deformation patch for every
  keyframe is very time-consuming. The solution is to add another
  dimension to the deformation patch ie. time.

  For every two keyframes, it is possible to perform linear interpolation
  to generate each frame between the two keyframes.

  For every four keyframes, it is possible to perform cubic interpolation
  to generate each frame between the four keyframes.

  This allows for smooth animation along with efficient use of memory
  space.
</pre>
