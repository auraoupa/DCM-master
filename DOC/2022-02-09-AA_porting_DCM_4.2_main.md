# Porting 4.2 recent updates into DCM

In order to use XIOS3_beta that has been released in 2022, we need to take a more recent version of NEMO than 4.2 branch.
We are going to port the DRAKKAR customs to NEMO version commit=389a917643f84804f6c7c6cb61c33007bc9a7b20.

## List of the differences between 4.2 NEMOREF & DRAKKAR to port :

| routine | difference | porting |
|--|--|--|
| makenemo | how to make the list of CPPkeys | not ported |
| icedia.F90 | set trends to 0 if not found in restart file | yes |
| icerst.F90 | change in name of restart/output (path) | yes |
| icestp.F90 | change in name of restart/output (path) | yes |
| diaar5.F90 | halosteric ssh | yes |
| diaprod.F90 | product diagnostics (uT, vS etc.) | yes |
| domain.F90 | change in name of restart (path) | yes |
| dommsk.F90 | partial steps mask | yes |
| dtatsd.F90 | modify damping init from TS files| yes |
| icb_oce.F90 | add iceberg calving restarts ?| yes |
| icbclv.F90 | add iceberg calving restarts ?| yes |
| icbini.F90 | add iceberg calving restarts ?| yes |
| icbrst.F90 | add iceberg calving restarts ?| yes |
| icbstp.F90 | add iceberg calving restarts ?| yes |
| icbtrj.F90 | add iceberg calving restarts ?| yes |
| in_out_manager.F90 | change in name of restart/output (path) | yes |
| iom.F90 | change in name of restart/output (path) | yes |
| restart.F90 | change in name of restart/output (path) | yes |
| isf_oce.F90 | allow for multiple ice shelf input files with different frequency | yes |
| isfpar.F90 | allow for multiple ice shelf input files with different frequency | yes |
| isfparmit.F90 | allow for multiple ice shelf input files with different frequency | yes |
| isfstp.F90 | allow for multiple ice shelf input files with different frequency | yes |
| lib_mpp.F90 | change in name of restart/output (path) | yes |
| diaobs.F90 | change in name of restart/output (path) | yes |
| obs_profiles_def.F90 | change in name of restart/output (path) | yes |
| obs_readmdt.F90 | modify reference level | yes |
| obs_surf_def.F90 | change in name of restart/output (path) | yes |
| obs_write.F90 | change in name of restart/output (path) | yes |
| sbcblk.F90 | allow climatological forcings | yes |
| sbcfwb.F90 | output fwprv ? | yes |
| sbcrnf.F90 | runoffs from multiple files | yes |
| sbcssr.F90 | add shapiro filter on SSS restoring | yes |
| shapiro.F90 | add shapiro filter on SSS restoring | yes |
| trabbl.F90  | use k- criteria instead of depth criteria | yes |
| usrdef_fmask.F90 | config dependant local enhancement of viscosity | yes |
| zdfdrg.F90 | boost of top bottom friction from file ? | yes |
| nemogcm.F90 | timing and error/warnings | yes |
| step.F90 | product diagnostics (uT, vS etc.) | yes |
| step_oce.F90 | product diagnostics (uT, vS etc.) | yes |
| stpmlf.F90 | product diagnostics (uT, vS etc.) | yes |
| timing.F90 | allow for longer times | yes |


