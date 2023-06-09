# Smouns_RPVMSSM
Input and output files for generating p p > mul- mul+ events under the RPVMSSM model

# Downloaded the entire "/RPVSSM_UFO" directory from https://github.com/lawrenceleejr/DVMuReint/tree/86e167ff72ac462aac583ac5751d72f889a18a63/RPVMSSM_UFO
<code>
mg5> import model RPVMSSM_UFO/RPVMSSM_UFO</code> 
  
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





  

