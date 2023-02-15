# Porting 4.2 recent updates into DCM

In order to use XIOS3_beta that has been released in 2022, we need to take a more recent version of NEMO than 4.2 branch.
We are going to port the DRAKKAR customs to NEMO version commit=389a917643f84804f6c7c6cb61c33007bc9a7b20.

## List of the differences between 4.2 NEMOREF & DRAKKAR to port :

| routine | difference | porting |
|--|--|--|
| makenemo | how to make the list of CPPkeys | not ported |
| icedia.F90 |--|--|
| icerst.F90 |--|--|
| icestp.F90 |--|--|
| diaar5.F90 |--|--|
| diaprod.F90 |--|--|
| domain.F90 |--|--|
| dommsk.F90 |--|--|
| dtatsd.F90 |--|--|
| icb_oce.F90 |--|--|
| icbclv.F90 |--|--|
| icbini.F90 |--|--|
| icbrst.F90 |--|--|
| icbstp.F90 |--|--|
| icbtrj.F90 |--|--|
| in_out_manager.F90 |--|--|
| iom.F90 |--|--|
| restart.F90 |--|--|
| isf_oce.F90 |--|--|
| isfpar.F90 |--|--|
| isfparmit.F90 |--|--|
| isfstp.F90 |--|--|
| lib_mpp.F90 |--|--|
| diaobs.F90 |--|--|
| obs_profiles_def.F90 |--|--|
| obs_readmdt.F90 |--|--|
| obs_surf_def.F90 |--|--|
| obs_write.F90 |--|--|
| sbcblk.F90 |--|--|
| sbcfwb.F90 |--|--|
| sbcrnf.F90 |--|--|
| sbcssr.F90 |--|--|
| shapiro.F90 |--|--|
| trabbl.F90  |--|--|
| usrdef_fmask.F90 |--|--|
| zdfdrg.F90 |--|--|
| nemogcm.F90 |--|--|
| step.F90 |--|--|
| step_oce.F90 |--|--|
| stpmlf.F90 |--|--|
| timing.F90 |--|--|
|-- |--|--|

