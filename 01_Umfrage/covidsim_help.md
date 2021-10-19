- ## For whom is CovidSIM?

  *CovidSIM* is a planning tool for public health departments, local governments, companies and other parties who are concerned about the spread of the new corona virus SARS-CoV-2 which causes the disease called COVID-19.

  ## What is CovidSIM?

  CovidSIM is a deterministic simulation tool which is based on differential equations. This means that it does not work with random numbers. All predictions must, therefore, be understood as average values.

  CovidSIM is not a tool to predict the exact course of an epidemic. It is a tool to explore different possible scenarios which will help decision makers to adjust their pandemic preparedness plans and to assess possible results of interventions.

  The pre-set parameter values try to capture the current state of knowledge, but many of the parameters which determine the spread of an outbreak are still not well known. Furthermore, these values differ between communities. The rate at which the infection spreads depends for example on the density of the population, on the frequency at which people have contact with each other and even on the intensity of these contacts.

  You are free to change the parameter values on the user interface of CovidSIM to adjust them to the rapidly evolving state of knowledge and to explore best-case and worst-case scenarios.

  ------

  # User interface

  ## Using the sliders

  You can easily change the parameter values on the user interface by moving any one of the sliders. As it may be difficult to get exactly the right value by moving the sliders, you can also select one of the sliders (just click on it; the button in the middle will grow larger to indicate that it is chosen) and then use the "cursor up" or "cursor down" buttons on your keyboard to increase or decrease the value.

  ## Modifying the output curves

  The curves on the right hand side should quickly respond to parameter changes. The labels over the curves show which ones of the output curves are currently displayed. To remove (or add) one of the curves, you only have to click on these labels. A double-click on any of these labels will hide all other curves and only show the selected one.

  ------

  ## Explanation of parameters

  ### Population

  

  - **Population size [mio]** gives the total size of the population. As CovidSIM is a rather simple tool, the whole population is assumed to be homogenously mixing.
  - **Initial infections** determines the number of individuals who are infected at the beginning of the simulation. The remaining population is assumed to be non-immune.
    We recommend that you do not change this value. It is not a good idea to set it to the number of cases who have already been identified and isolated, because they should not be able to spread the infection in the population. It may be more relevant to assume that at some unknown time point one person (or a few persons) have brought in the infection into a population, but have remained undetected, and to see how the infection is spreading in such a scenario. The detection probability (see below) can then be used to see how far this infetion has spread before it actually is detected by a random SARS-CoV-2 test.

  ### Durations (advanced settings)

  *Please only change the parameters in this section if you know what you are doing.*
  Changing the durations or the number of stages frequently does not have the effect that people expect who are not familiar with mathematical modeling concepts.

  - **Latency period [days]** determines the average duration of the latency period. This is the initial period of an infection during which the infected individual cannot spread the infection to others.
  - **Number or latency stages** determines the variability of the duration of the latency period (assuming an Erlang distribution). Using 16 stages, the standard deviation of the latency period is 25% of its mean duration.
  - **Prodromal period [days]** determines the average duration of the period which immediately follows the latency period. During this period, some patients may show mild and untypical symptoms. CovidSIM also allows to assume that infected individuals can spread the virus to others during the prodromal period (see Contagiousness parameters below).
  - **Number or prodromal stages** determines the variability of the duration of the prodromal period (assuming an Erlang distribution). Using 16 stages, the standard deviation of the prodromal period is 25% of its mean duration.
  - **Symptomatic period [days]** determines the period which follows the prodromal period. This is typically the period during which clear symptoms occur and during which cases infect others, but we use the same duration for the infectiousness for individuals who do not develop symptoms. At the end of this period, the vast majority of cases acquires a full immunity, but a small fraction of them will die.
  - **Number or symptomatic stages** determines the variability of the duration of the symptomatic period (assuming an Erlang distribution). Using 16 stages, the standard deviation of the symptomatic period is 25% of its mean duration.

  ### Severity

  

  - **Infections which lead to sickness [%]** determines the fraction of infected individuals who eventually become sick. The remaining ones will not have any symptoms, but can infect others in the same way and for the same duration as sick ones. If more information will become available, we can extend the model to give them a different contagiousness, but at this early stage of knowledge, we assume that people who are not sick (although they may spread fewer virus particles) infect the same number of people as sick patients (who spread more virus particles), because they are able to leave home and meet many others.
  - **Sick patients seek medical help [%]** determines what fraction of sick cases go to the doctor to seek medical help.
  - **Sick patients are hospitalized [per 1,000]** determines the fraction of sick cases who are hospitalized.
    This parameter is based on the German report on cases with influenza-like illness from 2017/18: with 40% of cases seeking medical help, 9 million medical consultations refer to about 22.5 million symptomatic cases; the estimated number of 45,000 hospitalizations are 0.2% of the symptomatic cases.
  - **Hospitalized cases need intensive care (ICU) [%]** determines the fraction of hospitalized cases who will be admitted to an intensive care unit (ICU).
  - **Sick patients die from the disease [per 1,000]** determines the fraction of sick cases who die from the disease.

  ### Contagiousness

  

  - **Basic reproduction number R0** determines the average number of infections which are caused by a single infected individual in a population where nobody is immune and where nobody takes any preventive measures (no contact reduction, no isolation, no treatment etc.). It is important to note that this only refers to people who are infected by the "index case", but it does not include infections which are caused by the infected people themselves. Other parameters like the duration of the infective period (see above) are already factored in the basic reproduction number.
    As a consequence of this, if the value 4 is chosen, one infected individual infects on average 4 others; if the duration of the infectious period is doubled, the infected individual still infects 4 others (not 8 as one may assume), but then it takes about twice as long until these 4 are infected; thus doubling the infective period does not double the number of secondary infections, but only slows down the spread of the infection. If the user wants to obtain a higher duration of infectiveness and also a higher number of secondary cases, both parameters have to be changed.
  - **Relative contagiousness in prodromal period [%]** determines how contagious cases are during their prodromal period (see above).
    The contagiousness during the symptomatic period (which follows the prodromal period) is basically calculated from the basic reproduction number and from the average duration of the symptomatic period. This contagiousness is then used as the 100% reference to calculate the contagiousness during the prodromal period. If a value of 50% is used here, this means that individuals in their early infective period (which we call "prodromal period") are only half as contagious as in their late infective period (which we call "symptomatic period").

  ### Interventions

  

  - **General contact reduction [%]** determines what percentage of contacts are prevented in the general population. This summarizes a wide variety of different interventions: people may generally have fewer contacts; they may enforce personal hygiene measures (hand washing etc.) or wear face masks to effectively reduce their contacts; schools may be closed and mass gatherings may be stopped.
  - **Contact reduction begin [day]** determines when the contact reduction starts.
  - **Contact reduction duration [days]** determines how long the contact reduction lasts. After the end of this period, contacts are set back to the original 100% value.
  - **Max. number of cases to be isolated [per 10,000]** determines how many cases can be isolated in a population. Only sick cases who seek medical help can be isolated in our simulation. For the time during which this intervention is switched on, severe cases are immediately isolated when they show symptoms (i.e. at the end of their prodromal period and the beginning of their symptomatic period). They will be isolated until the end of their symptomatic period. Isolated cases are completely prevented from spreading the infection.
    Please note that these are rather optimistic assumptions; in reality, isolation may frequently occur at a later stage of the infection, and cases will occupy the isolation units much longer than their infective period.
    If the number of sick cases exceeds the the isolation capacity which is determined by this parameter, the surplus number of them cannot be isolated, but remains in the population where they may spread the infection.
  - **Begin of case isolation measures [day]** determines when the isolation measures start.
  - **Duration of case isolation measures [days]** determines how long the isolation measures are performed.
    This does not determine how long a single case is isolated. As stated above, cases are always isolated until the end of their symptomatic period.

  ### Detection (advanced settings)

  *Please only change the parameters in this section if you know what you are doing.*

  These parameters allow to calculate the probability of early detection of hidden COVID-19 cases in a population which is apparently free from the disease. The formula is assumes that random SARS-CoV-2 tests in patients with influenza-like illness (ILI) are performed.

  **Background:** In a population where no COVID-19 cases have been detected before or where apparently only travel-associated cases have occurred and were isolated, ongoing transmission of SARS-CoV-2 may remain unnoticed for quite a while, because COVID-19 cases may frequently be mistaken for influenza or ILI cases. Performing laboratory tests for SARS-CoV-2 in such patients would reveal the true reason of their sickness, but such tests may initially be rather rare random events. The following three parameter values determine the probability that a medical doctor who is consulted by a sick patient, or a hospital actually orders a laboratory test for what seems to be an ordinary influenza patient. Even if these probabilities are low, the increasing number of COVID-19 cases will sooner or later lead to the detection of the local transmission of the infection.

  - Random SARS-CoV-2 tests in patients with Influenza-Like Illness (ILI)

  - **In ILI patients who seek medical help [per 10.000]** determines the fraction of randomly picked ILI patients who seek medical help for whom a SARS-CoV-2 test is performed.
  - **In hospitalized ILI patients [per 10.000]** determines the fraction of randomly picked ILI patients who are admitted to a hospital for whom a SARS-CoV-2 test is performed.
  - **In patients who died from ILI [per 10.000]** determines the fraction of randomly picked ILI patients who have died from the disease and for whom a SARS-CoV-2 test is performed.

  ------

  ## Output curves

  ### Infection and Immunity Status (Prevalence)

  

  - **Susceptible:** People who are neither immune nor infected; in the beginning, the whole population is assumed to be susceptible.
  - **Infected:** People who have been infected with SARS-CoV-2 and who have not yet recovered (or died).
  - **Recovered:** People who have recovered from their infection and who are now immune.
  - **Dead:** People who have died from the infection since the beginning of the simulation.
  - **Detection Probability:** Probability that a the spread of the infection has already been detected by random SARS-CoV-2 tests on ILI patients.

  ### Infection and Disease (Prevalence)

  

  - **Latent:** Recently infected individuals who cannot yet spread the infection.
  - **Prodromal:** Infected people who already may have some untypical symptoms and who already may be able to spread the infection.
  - **Symptomless Infections:** Infected people who are already in their late stage of infection (which we ususally call "symptomatic period"), but who never show any symptoms.
  - **Sick:** Infected people who are sick.
  - **Hospitalized:** Sick patients who have been hospitalized because of their disease.
    This does not count in infected individuals who have been hospitalized because of other reasons nor people who were infected in a hospital.
  - **ICU:** Sick patients who have been admitted to an intensive care unit.

  ### New Events per Day [or per Week] (Incidence)

  

  - **Infections:** Number of individuals who are newly infected on that day [or in that week].
  - **Sick:** Number of individuals who become sick on that day [or in that week].
  - **Hospitalized:** Sick patients who are hospitalized because of their disease on that day [or in that week].
  - **ICU Admissions:** Sick patients who are admitted to an intensive care unit on that day [or in that week].