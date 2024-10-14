### 2.3.1 Absorption

The parameter value for  `Specific intestinal permeability` and `Intestinal Paracellular permeability` were optimized based on clinical oral data, see [Section 2.3.4](#234-automated-parameter-identification). The measured solubility in FaSSIF was used in the model (see [Section 2.2.1](#221-in-vitro-and-physicochemical-data))

The dissolution of tablets was implemented via empirical Weibull dissolution. 

### 2.3.2 Distribution

Furosemide is highly bound to plasma proteins (fu = 2.20 %) (see [Section 2.2.1](#221-in-vitro-and-physicochemical-data)). A value of 11.5% was used in this PBPK model for `Fraction unbound (plasma, reference value)`. The major binding partner was set to albumin (see [Section 2.2.1](#221-in-vitro-and-physicochemical-data)).

An important parameter influencing the resulting volume of distribution is lipophilicity. The reported experimental logP ranged from -0.24 to 2.56, and a value of -0.24 was used in this model (see [Section 2.2.1](#221-in-vitro-and-physicochemical-data)). 

After testing the available organ-plasma partition coefficient and cell permeability calculation methods built in PK-Sim®, observed clinical data was best described by choosing the partition coefficient calculation by `Schmitt` and cellular permeability calculation by `Charged dependent Schmitt`.

### 2.3.3 Metabolism and Elimination

One metabolic pathway was implement into the model via Michaelis-Menten kinetics 

* UGT1A9

The UGT1A9 expression profiles are based on high-sensitive real-time RT-PCR ([Nishimura 2003](#5-references)). Metabolic enzyme activity was described as saturable process following Michaelis-Menten kinetics, were the `Km` was taken from literature and the `kcat` was optimized based on clinical data (see [Section 2.3.4](#234-automated-parameter-identification)).

And several transport protein was implemented into the model via Michaelis-Menten kinetics 

* OAT3

The OAT3 expression profiles are based on high-sensitive real-time RT-PCR ([Nishimura 2005](#5-references)). Transporter activity was described as saturable process following Michaelis-Menten kinetics, were the `Km` was set to 1 µmol/l and `kcat` was optimized based on clinical data (see [Section 2.3.4](#234-automated-parameter-identification)).

* MRP4

The MRP4 expression profiles are based on whole genome expression arrays from ArrayExpress ([Nishimura 2005](#5-references)). Transporter activity was described as saturable process following Michaelis-Menten kinetics, were the `Km` was taken from literature and `kcat` was optimized based on clinical data (see [Section 2.3.4](#234-automated-parameter-identification)).

Additionally, passive renal clearance by glomerular filtration was implemented and the `GFR fraction` was set to 1. In addition, fraction of bile that was continuously released was set to 1 (`EHC continuous fraction`)


### 2.3.4 Automated Parameter Identification

The following parameters have been estimated in the model:

| Model Parameter                |
| ------------------------------ | 
| `kcat` (UGT1A9)             | 
| `kcat` (OAT3)            |
| `kcat` (MRP4)                    | 
| `Specific intestinal permeability`| 
| `Intestinal permeability (paracellular)`| 
| `Tablet dissolution Weibull Shape`|
| `Tablet dissolution Weibull Time`|


 