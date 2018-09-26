# Registration Call
```
#!/bin/bash
AntsExecutable="path_to_ants_excecutable"


DATA_PATH=$1
OutputDirectory=$2
fixedImage=$3
dim=$4
gradientStep=$5
updateFieldVariance=$6
totalFieldVariance=$7

####################################################
# Find max number of files to reconstruct filename
numberOfFiles=($(find $DATA_PATH/* | wc -l))


# ITERATE THROUGH EVERY PHASE
for (( i = 0; i < $numberOfFiles; i++ ))
do
  movingImage=$DATA_PATH"FLUSSPHANTOM_V3_t00"$i".nii"
  echo $movingImage

####################################################
  # Execute ants
  echo "---"
  echo "Executing ants"
  echo "---"

  Ants_Reg_Call="${AntsExecutable} --dimensionality $dim \
  --output [$OutputDirectory/fixedImage_to_${i}_] \
  --metric MI[$fixedImage,$movingImage,1,32,Regular,0.25] \
  --transform SyN[$gradientStep,$updateFieldVariance,$totalFieldVariance] \
  --convergence [250x250x250x250,1e-6,10] \
  --shrink-factors 8x4x2x1 \
  --smoothing-sigmas 3x2x1x0vox \
  "

  echo $Ants_Reg_Call
  $Ants_Reg_Call
  ####################################################
done


echo "registration finished"

exit
```

# Parameter variation

Three parameters were varied as described below:

- gradient step: 0.5 or 1.0
- update field variance: 0
- total field variance: varied between 1.5 and 3.0.
