# Chat-GPT
Send chat GPT code btween sources


| rex field=volume "(?<min>\d+)[-](?<max>\d+)"
| eval min=if(min=0, min, min/1000."k"), max=if(max>=1000000, round(max/1000000, 1)."M", round(max/1000, 1)."k")

