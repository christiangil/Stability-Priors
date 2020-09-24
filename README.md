## Generating Systems
### K23_make_sims.pbs
A PBS job script to call make_systems.py for Kepler 23.
### make_systems.py
Generating systems and testing for 10^5 orbit stability (with some parallelization).
A PBS job script to call test_stability.py is created for any systems that last 10^5 orbits.
Simulation archives are saved for systems lasting >= 10^4 orbits.

## Estimating Stability
### K23_loge_SPOCK.pbs
A PBS job script to call estimate_stability.py for Kepler 23 systems generated with a uniform prior in eccentricity and a loguniform prior in planet mass.
### K23_logm_SPOCK.pbs
A PBS job script to call estimate_stability.py for Kepler 23 systems generated with a loguniform prior in eccentricity and a uniform prior in planet mass.
### estimate_stability.py
Using SPOCK to estimate stability probabilities for the systems with saved simulation archives (with some parallelization).

## Testing N-body 10^9 Orbit Stability
### test_stability.py
Trying to integrate systems for 10^9 orbits for the systems with saved simulation archives.

## Utilities
### stability_functions.py
Holds functions that create REBOUND simulations of our desired systems and various (mostly deprecated/unused) helper functions.
### submit_jobs.py
Submits up to max_submissions PBS jobs to the CyberLAMP computing cluster

## I believe these can be deleted
### generate_systems.py
### plot_stability.py

*NOTE: The PBS jobs cripts are written to be used on Penn State's CyberLAMP computing cluster
