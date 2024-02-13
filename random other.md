# Module table:
id text
name text
iconLocation text


# Topic table:
id text
modId text - foreign
name text
desc text
iconLocation text
isExercised text
isfinished text


# Content/Pages table:
pageNum text
topicId text - foreign
title text
desc text
code text
output text
isFinished text


# Exercise table:
topicId text - foreign
problem text
codePattern text
outputPattern text
isAvailable text


# ModAndTopTracking:
currentModule text
currentTopic text



# History table:
modId  text - foreign
topicName text
dateStarted  text
dateCompleted text

# LastVisited Table:
modId text
topicId text
pageNum  text- foreign 
lastDateVisited text