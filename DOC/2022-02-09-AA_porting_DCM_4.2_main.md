# Porting 4.2 recent updates into DCM

In order to use XIOS3_beta that has been released in 2022, we need to take a more recent version of NEMO than 4.2 branch.
We are going to port the DRAKKAR customs to NEMO version commit=389a917643f84804f6c7c6cb61c33007bc9a7b20.

## List of the differences between 4.2 NEMOREF & DRAKKAR  :

| routine | difference | to be ported |
|--|--|--|
| makenemo | how to make the list of CPPkeys | no |
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
| isfparmlt.F90 | allow for multiple ice shelf input files with different frequency | yes |
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

## Port the changes

In the eORCA05.L121-JZAA015 experiment, we import from nemoref all the files to be ported with dcm_getfile command.
Then with dcm_cmpfile -d we extract from DRAKKAR the changes we want to port and modify them if needed.


| routine | ported ? |
|--|--|
| icedia.F90 | done |
| icerst.F90 | done |
| icestp.F90 |done |
| diaar5.F90 | done |
| diaprod.F90 | copied entirely |
| domain.F90 | done |
| dommsk.F90 | done |
| dtatsd.F90 | done |
| icb_oce.F90 | done |
| icbclv.F90 | done |
| icbini.F90 | done |
| icbrst.F90 | done |
| icbstp.F90 | done |
| icbtrj.F90 |done  |
| in_out_manager.F90 | done |
| iom.F90 | done |
| restart.F90 | done |
| isf_oce.F90 | done |
| isfpar.F90 | another name for the dummy variable ji ? (already used) |
| isfparmlt.F90 | adapted to enter the DO loop and change of variable name |
| isfstp.F90 | done |
| lib_mpp.F90 | done |
| diaobs.F90 | done |
| obs_profiles_def.F90 | done |
| obs_readmdt.F90 | done |
| obs_surf_def.F90 | done |
| obs_write.F90 | done |
| sbcblk.F90 | replace nn_hls by 0 in DO_2D( nn_hls, nn_hls, nn_hls, nn_hls ) like in the rest ? |
| sbcfwb.F90 | done |
| sbcrnf.F90 | done |
| sbcssr.F90 | done |
| shapiro.F90 | copied entirely |
| trabbl.F90  | replace mi0(ii0) par mi0(ii0,nn_hls) like in the rest ?|
| usrdef_fmask.F90 |  |
| zdfdrg.F90 |  |
| nemogcm.F90 |  |
| step.F90 |  |
| step_oce.F90 |  |
| stpmlf.F90 |  |
| timing.F90 |  |


| routine | ported ? |
|--|--|
| icedia.F90 |  |
| icerst.F90 |  |
| icestp.F90 | |
| diaar5.F90 |  |
| diaprod.F90 |  |
| domain.F90 |  |
| dommsk.F90 |  |
| dtatsd.F90 |  |
| icb_oce.F90 |  |
| icbclv.F90 |  |
| icbini.F90 |  |
| icbrst.F90 |  |
| icbstp.F90 |  |
| icbtrj.F90 |  |
| in_out_manager.F90 |  |
| iom.F90 |  |
| restart.F90 |  |
| isf_oce.F90 |  |
| isfpar.F90 |  |
| isfparmlt.F90 |  |
| isfstp.F90 |  |
| lib_mpp.F90 |  |
| diaobs.F90 |  |
| obs_profiles_def.F90 |  |
| obs_readmdt.F90 |  |
| obs_surf_def.F90 |  |
| obs_write.F90 |  |
| sbcblk.F90 |  |
| sbcfwb.F90 |  |
| sbcrnf.F90 |  |
| sbcssr.F90 |  |
| shapiro.F90 |  |
| trabbl.F90  |  |
| usrdef_fmask.F90 |  |
| zdfdrg.F90 |  |
| nemogcm.F90 |  |
| step.F90 |  |
| step_oce.F90 |  |
| stpmlf.F90 |  |
| timing.F90 |  |
