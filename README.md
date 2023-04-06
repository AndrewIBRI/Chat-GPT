# Chat-GPT
Send chat GPT code btween sources


| chart sum(valor) over campo1 by campo2 span=500000 
| rex field=volume "(?<min>\d+)-(?<max>\d+)" 
| eval min=min/1000, max=max/1000 
| eval volume=if(max>=1000, tostring(round(max/1000,1))."M", if(min>=1, tostring(round(min,1))."K", tostring(volume)))
