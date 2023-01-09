## Automatically Summarizing Evidence from Clinical Trials: A Prototype Highlighting Current Challenges 
[Sanjana Ramprasad](https://www.khoury.northeastern.edu/people/sanjana-ramprasad/), [Denis Jered McInerney](https://www.khoury.northeastern.edu/people/denis-jered-mcinerney/), [Iain Marshall](https://kclpure.kcl.ac.uk/portal/iain.marshall.html), [Byron Wallace](https://www.byronwallace.com/)

### Overview 
We present TrialsSummarizer, a prototype for summarizing reports of randomized controlled trials of medical interventions, which are the gold standard for evidence-based care.  This is work builds on prior work by Ian Marshall[^1].

Realizing the aim of evidence-based care has become increasingly difficult owing to the rapid growth of medical literature. The use of summarization methods to provide concise overviews of all evidence relevant to a clinical question can be used to alleviate this difficulty.

However, current neural summarization methods are prone to factual errors rendering them of little use in generating summaries of comparative treatment efficacy. Improving the factuality of neural summarization methods is unlikely to be solved in the near future. In the interim, we present TrialsSummarizer an interactive tool that allows users the means to to assess the validity of outputs. We also provide some degree of controllability that gives users the opportunity to obtain corrected versions of summaries in real time.

### Demonstration
<div style="padding:56.25% 0 0 0;position:relative;"><iframe src="https://player.vimeo.com/video/735605060?h=05e122b091&amp;badge=0&amp;autopause=0&amp;player_id=0&amp;app_id=58479" frameborder="0" allow="autoplay; fullscreen; picture-in-picture" allowfullscreen style="position:absolute;top:0;left:0;width:100%;height:100%;" title="Automatically Summarizing Evidence from Clinical Trials: A Prototype Highlighting Current Challenges"></iframe></div><script src="https://player.vimeo.com/api/player.js"></script>

### Interfaces
 We consider two implementations of the summarization module
1. A vanilla interface based on seq2seq bart model 
2. An exploratory interface based on our proposed model providing transperancy and controllability can be found [here](http://ec2-54-221-130-248.compute-1.amazonaws.com:8080)

### Example Queries
#### 1) Does chloroquine or hydroxychloroquine improve outcomes in COVID-19 infection?

  [View result on the exploratory interface](http://ec2-54-221-130-248.compute-1.amazonaws.com:8080/?q=~%28~%28field~%27population~text~%27COVID-19%2a20%2a5bpopulation%2a5d~cui~%27TS-COV19%29~%28field~%27interventions~text~%27Chloroquine%2a20%2a5binterventions%2a5d~cui~%27C0008269%29%29)
  
#### 2) What is the effect of clopidogrel on mortality rate in patients with acute myocardial infarction? 
  
  [View result on the exploratory interface](http://ec2-54-221-130-248.compute-1.amazonaws.com:8080/?q=~%28~%28field~%27population~text~%27Acute%2a20myocardial%2a20infarction%2a20%2a5bpopulation%2a5d~cui~%27C0155626%29~%28field~%27interventions~text~%27clopidogrel%2a20%2a5binterventions%2a5d~cui~%27C0070166%29~%28field~%27outcomes~text~%27Mortality%2a20rate%2a20%2a5boutcomes%2a5d~cui~%27C0026565%29%29)


### Source Code 
[https://github.com/sanjanaramprasad/RRnlp](https://github.com/sanjanaramprasad/RRnlp)

[https://github.com/sanjanaramprasad/trialstreamer-demo](https://github.com/sanjanaramprasad/trialstreamer-demo)

### References 
[^1]: Marshall, Iain J., et al. "Trialstreamer: A living, automatically updated database of clinical trial reports." Journal of the American Medical Informatics Association 27.12 (2020): 1903-1912.
