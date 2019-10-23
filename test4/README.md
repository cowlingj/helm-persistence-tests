# Test 4 - Using PV's and PVC's in StatefulSets

- if a volume claim template is used,
  then the assume the volume has already been mounted to pods
  (and it can be mounted to containers by using the templates name)
- any volumes declaired in the volumes block are used verbatm,
  so if the volume is created backed by a pvc,
  then the exact pvc will be used muktiple times
- pvc's will outlast helm delete
- pv are destroied as expected with helm delete
- a pvc will keep a pv from being destroied by helm
  (but deleting the pvc will result in the pv being deleted if
  the helm deployment has previously been deleted)