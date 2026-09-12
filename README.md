# GMT psmeca — Earthquake Focal Mechanism and Seismotectonic Mapping Scripts

GMT (Generic Mapping Tools) shell scripts for mapping earthquake source parameters and crustal deformation over relief and sediment basemaps. The scripts plot focal-mechanism beachballs, first-motion polarities and geodetic velocity vectors, characterising the seismotectonics of ocean trenches and basins. They have been used to generate figures in the author's geophysical and cartographic publications.

## What the scripts do

- build a shaded-relief or sediment-thickness basemap (grdimage, grdcontour, makecpt)
- plot double-couple / moment-tensor focal mechanisms as beachballs (psmeca) from GCMT-format catalogues, scaled and coloured by mechanism
- plot first-motion polarity data for individual events (pspolar)
- plot GPS / crustal velocity vectors with error ellipses (psvelo)
- add colour scale bars, grids, scale bars, roses, annotations and the GMT logo (psscale, psbasemap, pstext, logo)
- export to raster (psconvert) at high resolution

## Data sources

- Earthquake focal mechanisms: Global Centroid Moment Tensor (GCMT) catalogue (CMT format)
- Polarity and velocity data: first-motion picks and geodetic velocity fields
- Basemaps: ETOPO1 relief and GlobSed sediment thickness
- Coastlines: GSHHG via GMT

## Files

- GMT-26-JT-AS.sh: focal mechanisms (psmeca) over the Arabian Sea
- GMT-26-JY-PSB psmeca.sh: focal mechanisms, Philippine Sea Basin
- GMT-26-JY-PSB pspolar.sh: first-motion polarities, Philippine Sea Basin
- GMT-26-JY-PSB psvelo.sh: crustal velocity vectors, Philippine Sea Basin
- meca_08.sh: the GMT focal-mechanism example the workflow is based on

## Requirements

- GMT 6.x (Generic Mapping Tools): https://www.generic-mapping-tools.org
- A POSIX shell (bash/sh)
- The relevant relief / sediment grid and the focal-mechanism / polarity / velocity data files available locally

## Usage

Place the required grid and source-parameter data in the working directory, adjust the -R region and -J projection at the top of the chosen script, then run:

    bash GMT-26-JT-AS.sh

The script writes a PostScript file and converts it to a raster image (JPG/PNG) via psconvert.

## Author and citation

Polina Lemenkova
ORCID: https://orcid.org/0000-0002-5759-1089

These scripts support figures in the author's geophysical and cartographic papers; please cite the specific article a given figure appears in. The full publication list is available via the ORCID record above.

## License

See the LICENSE file in this repository.
