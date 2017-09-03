# Data for PARCS example RCBMs ranging from 10 to 30 for the control and 20 to 50 for the treatment group
# If start creating functions I only have to change the names once at the end.
# I want half 
dataFunction = function(x){
  set.seed(12345)
  x = as.data.frame(matrix(sample(x, 75, replace = TRUE),15,5))
}
control = c(10:30)
controlData = dataFunction(control); controlData
names(controlData) = paste0("Participant",1:5); controlData

intervention= c(20:50)
interventionData = dataFunction(intervention); interventionData
names(interventionData) = paste0("Participant",1:5); interventionData

scdBrainData = rbind(controlData, interventionData)
