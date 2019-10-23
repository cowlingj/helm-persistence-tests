# Test 6 - Dynamic Provisioning

- This is what i want
- helm creates the release but not the PVCs (so helm won't delete anything)
- since helm hasn't created volumes, it won't try to delete or recreate them
- since pvs and volumes are 1-1 kubernetes must create a new pv for each pvc
- kubernetes best practice says pvc storage class should be parameterised

> works with hostpath-provisioner, which is installed on minikube
