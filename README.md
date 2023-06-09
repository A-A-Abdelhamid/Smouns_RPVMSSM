# Smouns_RPVMSSM
Input and output files for generating p p > mul- mul+ events under the RPVMSSM model

# Update

**Using the same configuration and input cards, I generated right-handed smuons with no issue. It does not produce any unexpected or strange Feynman diagrams. I re-ran it again for the left-handed smuons, and it is still producing vertices where a quark goes directly to a smuon and an anti-smoun**

# Left-handed Smouns
Feynman diagrams are under  [/Diagrams/](/Diagrams/)
Cross section makes sense (0.01471 +- 4.024e-05 pb) after I fixed the helicity (For this process the output is two left-handed smouns), but there are wierd Feynman diagrams like u u~ > d > mul- mul+ as in [here](/Diagrams/diagrams_1_uux_mulmmulp.pdf) in diagrams 3-5, and in [u c~ > d > mul- mul+](/Diagrams/diagrams_1_ucx_mulmmulp.pdf)
 

Downloaded the entire "/RPVSSM_UFO" directory from https://github.com/lawrenceleejr/DVMuReint/tree/86e167ff72ac462aac583ac5751d72f889a18a63/RPVMSSM_UFO

Installed the lhapdf library (lhapdf get NNPDF23_lo_as_0130_qed)

I used the default paramters generarted by the model ([param_card.dat](Cards/param_card.dat)), each beam was 6500 GeV, mass of left handed smoun= 2.029157e+02 GeV

<code>mg5> import model RPVMSSM_UFO/RPVMSSM_UFO</code> 

<code>mg5> display coupling_order</code>

    QCD : weight = 1
    QED : weight = 1
    RPV : weight = 1
  
<code>mg5> generate p p > mul- mul+ </code>

    INFO: Some T-channel width have been set to zero [new since 2.8.0]
    if you want to keep this width please set "zerowidth_tchannel" to False
    save configuration file to Cards/me5_configuration.txt
 
<code>mg5> display diagrams
mg5> launch</code>
 
    INFO: load configuration from Cards/me5_configuration.txt  
    INFO: load configuration from input/mg5_configuration.txt  
    INFO: load configuration from Cards/me5_configuration.txt  
  
    INFO: Update the dependent parameter of the param_card.dat 
    WARNING: update the strong coupling value (alpha_s) to the value from the pdf selected: 0.13 

    Generating 10000 events with run name run_01
    
 === Results Summary for run: run_01 tag: tag_1 ===

     Cross-section :   0.01471 +- 4.024e-05 pb
     Nb of events :  10000
 
INFO: No version of lhapdf. Can not run systematics computation 
store_events
INFO: Storing parton level results 
INFO: End Parton 
reweight -from_cards
decay_events -from_cards
INFO: storing files of previous run 
INFO: Done 
quit

<code>mg5> display processes</code>

    Process: u u~ > mul- mul+ WEIGHTED<=2 @1
    Process: u c~ > mul- mul+ WEIGHTED<=2 @1
    Process: c u~ > mul- mul+ WEIGHTED<=2 @1
    Process: c c~ > mul- mul+ WEIGHTED<=2 @1
    Process: d d~ > mul- mul+ WEIGHTED<=2 @1
    Process: d s~ > mul- mul+ WEIGHTED<=2 @1
    Process: s d~ > mul- mul+ WEIGHTED<=2 @1
    Process: s s~ > mul- mul+ WEIGHTED<=2 @1




  

