# IEMOCAP-Dataloader
IEMOCAP Preprocessed Data (ComParE_2016, eGeMAPSv02, Functionals, LLD) Loader Package

## IEMOCAP 
    Paper:
        https://ecs.utdallas.edu/research/researchlabs/msp-lab/publications/Busso_2008_5.pdf
 

## What is this package
    This is IEMOCAP-DataLoader for research purpose
    We preprocessed sentences data using opensmile.
    This Dataloader Package will return actual preprocessed data and sentences' label
    We made it to return data by session and emotion label using parameters.
    
 

## How To Use
    from IEMOCAP import processed_loader
    X, y = processed_loader.get_by_session(
                                    fset="ege", 
                                    flevel="fun", 
                                    session=[1,3], 
                                    only_label=["all"]
                                    )

## Parameters
    fset = 
        "comp" #ComParE_2016 : Opensmile parameters
        "ege"  #eGeMAPSv02 : Opensmile parameters
        
    flevel = 
        "fun"  #Functionals : Opensmile parameters
        "lld"  #LowLevelDescriptors : Opensmile parameters
        
    session = 
        [1,2,3,4,5] # list of the sessions you want to load
        
    only_labels = 
        ["all"] # for loading all emtion labels
        ["ang", "exc"] # for loading only "ang", "exc" emotion
        
## Emotion Labels
    "ang",
    "exc",
    "dis",
    "fea",
    "fru",
    "neu",
    "hap",
    "oth",
    "sad",
    "sur",
    "xxx",
