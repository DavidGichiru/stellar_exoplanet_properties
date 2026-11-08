Stellar and Exoplanet Properties:
Exploratory Data Analysis

An exploratory data analysis project investigating relationships between stellar properties and patterns in exoplanet systems using python.

Overview:
Stars vary in mass, radius, temperature, surface gravity and chemical composition. Exploring how these properties relate to another helps to better understand stellar populations and the environments in which exoplanets are discovered.
The project uses exploratory data analysis or EDA to investigate stellar measurements, examine relationships between numerical variables, identify unusual observations and explore selected properties of exoplanet systems.

Why is the investigation useful?
The correlations and observed results provide a data driven window into the history, architecture and potential habitability of planetary systems. These observations can help understand phenomena such as:

    1.Planet formation mechanisms
    2.Planetary migration and dynamical evolution
    3.Stellar tidal dampening
    4.Habitable zones and atmospheric survival
Research Questions:

-The distribution of exoplanet discoveries across the years listed in the dataset.
-How did mass and radius relate for stars, both those that were in the evolutionary stage and those that had exited the main sequence?
-How did planet discovery vary across different discovery methods and different stellar architectures?
-The relationship between the eccentricity and semi-major axis of exoplanets.
-How did Semi-Major Axis influence Orbital Period Days?

Tools and libraries used:
Python - data analysis and programming
Pandas - data and manipulation and cleaning
Numpy - numerical operations
Matplotlib - data visualization
seaborn - statistical visualization
Scipy - correlations calculation
Logging - trace code execution and handle errors and exceptions
Jupyter Notebook - analysis and documentation

Workflow:
1. Loading and inspection of the dataset.
2. Examine data types, missing values and data quality.
3. Get summary of missing values and clean the respective columns, missing too much data and those irrelevant to the analysis.
4. Explore distributions and correlations using visualizations; calculate and interpret correlations.
5. Investigate potential outliers and unusual astronomical objects.
6. Discuss findings, limitations and possible sources of bias.

Limitations of the dataset:
This specific dataset did not contain the planet radius data, therefore doing any analysis on any relationships concerning planet radii was impossible; the various analysis that could be done using the radius data would be the correlation between planet radius and mass, aiming to understand whether radius has any causation on the mass of a planet, either linearly or non-linearly.

Reproducing the analysis:
1. clone this repository:
   git clone
   https://github.com/DavidGichiru/stellar_exoplanet_properties
2. Navigate to project directory:
   cd stellar_exoplanet_properties
3. Install the dependencies:
   pip install -r requirements.txt
4.Download the dataset from NASA exoplanet archive:
   https://exoplanetarchive.ipac.caltech.edu/
5. Open the jupyter notebook
6. Open Stellar&Exoplanet_properties.ipynb and run the cells sequentially
   

Findings:

1. Distribution of exoplanet discoveries in the years listed in the dataset:

The dataset had planets that were recorded as early as 1995. The most number of planets were reported in 2016. This was a result of mass verifications of exoplanets discovered by the Kepler Space Telescope. 2014 also shows a big spike and this also due to mass verifications of exoplanets also discovered by the Kepler Space Telescope. This does not mean that astronomers found these in those specific years, planet detection took repeated pattern recognition such as dips in brightness of stars as planets orbit and in order to filter from noise they had to make sure a signal repeated over a period of time, thus the years 2014 and 2016 were when most of the signals discovered were dubbed as valid.

2. How did mass and radius relate for stars, both that were in the main sequence and those that had evolved?

The two variables showed a correlation of 0.61, which is a positive. However, it is imperative to note that the dataset contained stars that had evolved out of the main sequence. These represented the red giants or the Asymptotic giant branch. They are those that had ran out of hydrogen fuel, their cores contracted and the outer envelope expanded massively. An example of a star that had evolved out of the main sequence in the dataset was HD 81817, located about 900 light years away from earth. This star demonstrates how a star can bloat without gaining any additional weight. The star listed to have roughly 4 solar masses, started its evolutionary path as a relatively heavy star of the blue/white category in the main sequence. In the dataset it's radius is listed as 83.8 solar radii meaning it has expanded very massively. It has an effective temperature of about 4140K, hence shows a red/orange color. However it shines with a luminosity approximated to be of 2000 suns, due to it's enormous size and surface area therefore way bigger energy output than the sun. The star's age is listed as relatively young and approximated to be about 150 million years old. It has evolved faster because high mass stars burn hydrogen faster than low mass stars. This star is also deemed a hybrid star. Usually, old cool giant stars have slow, cool stellar winds whereas hot active stars have intense UV and X-ray emissions. The star HD 81817 does both and therefore termed as hybrid. The emissions are said to be caused by a white dwarf orbiting the giant. This white dwarf is believed to be the dead core of what used to be the most massive star in the system. 
How mass and radius relate therefore depends on the evolutionary stage of a star. During the main sequence, the dataset shows a predictable, mathematical relationship where mass increases with increase in radius and this is because more radius increases the surface area to pack more matter and therefore more mass.
During post main-sequence stage, core collapses due to lack of fuel; gravity wins and the core becomes very hot and dense. Intense heat from the core will ignite a layer of hydrogen just outside the core, causing the shell to burn. The explosive new energy dumps heat onto the outer layers and for these layers to dump the heat, they balloon out and expand to scales of 100x to 1000x. During this stage, the mass stays nearly constant or drops a little stellar winds, but the radius explodes massively. This occurrence destroys the mass-radius mathematical relationship. 
When a star is completely dead then the mass-radius relationship gets inverted. For stars that collapse into white dwarfs, more massive dwarfs have a smaller radius meaning they are physically smaller than lesser massive ones. This is because increasing mass increases gravity hence crushing the electron degenerate gas into a tighter, denser ball.
More massive stars might collapse into neutron stars, where the mass could range from 1.4-2.1 solar masses but the radius is incredibly small, strengthening the inverted mass-radius relationship.
Very massive stars collapse into blackholes. Here, the radius (size of the event horizon) scales linearly with mass, thus the more massive a star was before collapse, the bigger the event horizon will be after collapse.
In conclusion, how mass and radius relate depends entirely on the evolutionary stage of the star. The relationship for main sequence stars can therefore be termed linear, in that bigger radius means more mass. After exiting the main sequence then the relationship gets significantly distorted.

3. Variations of exoplanet discovery across different detection methods and stellar architectures.

The analysis compared Transit, Radial velocity, Imaging and Microlensing methods of detection, examining whether exoplanets orbited single stars, binaries or higher order multiple star systems. The data shows a strong predominance of exoplanets detected around single star systems, while planets around binaries and higher order multiple star star systems are considerably less in the dataset. However, this does not mean that planets around binaries and multiple star systems are intrinsically rare. The observed distribution is likely influenced by observational selection effects and the limitations of each detection technique. The transit method for instance requires, the orbital plane of an exoplanet to be aligned such that the planet crosses it's host star from the telescope's line of sight. Multiple star systems also make interpretation of stellar brightness variations more complicated. The transit method essentially detects exoplanets by making out dips in a star's brightness as the exoplanet orbits it. Repeated patterns of the dips over periods of times can confirm an orbiting body large enough to block a significant amount of the star's light as it passes in front.
This method has found the most number of planets in this catalogue because it can monitor alot of stars' brightness simultaneously, detects relatively small planets because even an earth-sized planet could cause a significant dip in the brightness of it ' s star if the instrument is sensitive enough and the star is suitable. Also space telescope avoid atmospheric interference therefore can measure tiny brightness changes without the earth's atmosphere distorting the observations. Radial velocity on the other hand detects a star's wobble. This is because the planet doesn't just orbit it's star, they both orbit their shared mass center known as the barycenter. This is because a planet's gravity pulls on its star too hence the star moves on a small orbit of it' s own, sometimes described as a wobble. When the star wobbles towards the telescope's field of view the spectral lines shift slightly towards the shorter wavelengths and when it moves away, they shift towards longer wavelengths. It finds many planets because it doesn't require a transit, is sensitive to massive planets as they cause bigger wobbles and works well for close orbiting planets. Radial velocity faces another type of challenge; the gravitational interactions between stars in binary or multiple star systems can produce much larger stellar velocity signals as compared to a planet. This makes the detection of a planet induced wobble more difficult to isolate. The analysis therefore highlights an important distinction; The number of planets detected around a particular type of stellar system is not the same as the number of planets that actually exist there. The catalogue represents the exoplanets that current observational methods have been able to detect.

4. How does eccentricity of a planet's orbit affect it's semi major axis?

Eccentricity is how stretched or elliptical a planet orbit is; the ideal orbit would be circular but planet orbits tend to get stretched over time. Semi-major axis on the other hand means half of the longest diameter of an elliptical orbit.
Analysis showed that there was no strong relationship between eccentricity and semi-major axis. Some planet's very close to their star, (small semi-major axis) had high eccentricity while others had low eccentricity; similarly, planets far from their parent star / stars, could have either a low or high eccentricity. This means that having a high eccentricity does not necessarily mean that a planet has a big or a small semi-major axis. This also applies for low eccentricity. Thus, the two variables are independent to each other. A good example from our own solar system is; mercury's and    Earth's orbit. Despite mercury having a smaller semi-major axis, it follows a way more elliptic path than Earth. This confirms that a planet can have a smaller yet, more elliptic orbit. Similarly planets in the outer solar system like Jupiter, Saturn and Uranus have more eccentric orbits than earth also meaning that a bigger semi-major axis does not mean low eccentricity. 
In an edge case where two planets in two different systems; system A has a planet orbiting it ' s star in an almost circular orbit and system B has a planet orbiting it ' s star with a very elliptical orbit. One might wonder what effect this could have on the semi-major axis as well as the orbital period days (time taken for a planet to make a full orbit around it's star). The size of the orbit remains the semi despite one being more circular. The period days also remain the same. Assuming the masses of both of the stars in those systems are identical, then in system A, the planet orbits with uniform velocity throughout the orbit since the gravitational pull on the planet by the star is uniform; the planet in system B however, experiences a stronger gravitational pull at the perihelion (closest point to it ' s star) and this makes the planet to accelerate. When it is moving towards the aphelion(farthest point from it ' s star) it experiences weaker gravitational pull and therefore slows down. The difference between these two velocities cancel out perfectly, and therefore it's Orbital period matches that one of the planet in system A. In conclusion, the investigation shows that Eccentricity and Semi-Major axis have no significant relationship to one another; distance is the one that influences the size of a planet's semi-major axis.

How did Orbit Semi-Major Axis influence Orbital Period Days?

The analysis showed a positive slope and the correlation value was a 0.93, which indicated a strong positive. The farther away a planet is from it ' s parent star, the longer the planet will take to orbit the star. This means that as Orbit Semi-major axis increases, the orbital period of that particular planet increases too. The period in which a planet takes to orbit a star is also dependent on the mass of the star apart from it ' s distance from the star. A more massive star will have a bigger gravitational acceleration and this means that the planet will orbit faster compared to a planet at the same distance from it ' s star but the star is less massive. A question that might arise is whether the planet' s mass matters. A planet' s mass is basically negligible as compared to a star' s mass. Therefore, the mass of the star will completely overshadow the mass of the planet; An asteroid and a planet at the same distance from the star would essentially have the same orbital period. However, if it was a gas giant orbiting a brown dwarf, then the planet's mass becomes relevant. Brown dwarfs are typically failed stars with masses approximated to be 13 Jupiter masses up to 80 Jupiter masses. When two bodies are of comparable masses, none orbits the other; they both orbit their shared mass center which is known as the barycenter, the distance between the two bodies decides how fast they complete a single orbital loop. A good example of how stellar mass affects the orbital period of a planet in the dataset is a planet named v Ophiuchi or nu Oph c. This planet (debated to be a brown dwarf as it is extremely heavy with roughly 21 - 24 Jupiter masses which is well within brown dwarf' s territory) is roughly 5.9 Astronomical Units from it ' s parent star and has an orbital period of roughly 8.7 years. Comparing this to Jupiter in our solar system; Jupiter is roughly 5.2 Astronomical Units from the sun and takes about 11.9 years to make a complete orbit around the sun. Therefore, V Ophiuchi sits further from it ' s star but takes less to orbit. This essentially comes down to how massive the parent star is. The star V Oph is estimated to be 1.5 - 3 times more massive than the sun and this explains the Orbital period of it ' s planet. Therefore, we can conclude from the dataset that the distnace of a planet from it ' s host star influences heavily how long it takes to complete a full orbit, with mass of the star being a considerable factor too.


