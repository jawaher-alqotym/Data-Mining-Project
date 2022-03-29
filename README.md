# Data-Mining-Project
Comparing three data mining algorithms in order to find the most suitable one to use in a medical  system that predicts patient survival before heart surgery.
We used the Heart failure clinical records Data Set from 2020 that have the following 
information.
Thirteen (13) clinical features:
- age: age of the patient (years)
- anemia: decrease of red blood cells or hemoglobin (Boolean)
- high blood pressure: if the patient has hypertension (Boolean)
- creatinine phosphokinase (CPK): level of the CPK enzyme in the blood (mcg/L)
- diabetes: if the patient has diabetes (Boolean)
- ejection fraction: percentage of blood leaving the heart at each contraction 
(percentage)
- platelets: platelets in the blood (kiloplatelets/mL)
- sex: woman or man (binary)
- serum creatinine: level of serum creatinine in the blood (mg/dL)
- serum sodium: level of serum sodium in the blood (mEq/L)
- smoking: if the patient smokes or not (Boolean)
- time: follow-up period (days)
- [class] death event: if the patient deceased during the follow-up period (Boolean)

**pre processing**
It is a numerical data set; thus, the attributes had been normalized first, and no empty 
cells were found. For the WEKA software to be able to work with the dataset, the class attribute 
had to be transformed from a numerical with the values 0 and 1 to the categorical data 
type. The value (yes) for 1 and (no) for the zero.


# K-Nn
classification using K-Nn Alg. After we tried more than one value for K, we conclude that 14 is the best for k for it achieve the highest precision score.
Result of confusion matrix:
Confusion matrix has:(a= yes) and (b=no)

![Screenshot (343)](https://user-images.githubusercontent.com/63616896/160510852-b9560d8a-1405-4d36-872e-4367a4b931ce.png)



- TP = 30 instances which mean they have a class (yes) and they classified as (yes).
- FN = 66 instances which mean they have a class (yes) and they classified as (no).
- FP = 12 instances which mean they have a class (no) and they classified as (yes).
- TN = 191 instances which mean they have a class (no) and they classified as (no).


**performance measures:**
- Accuracy= ((30+191)/ (96+203)) *100=73,9%
- Error Rate = ((66+12)/ (96+203)) *100=26,1% 
- FN Rate= (66/96) *100=68.75%
- TP Rate= (30/96) *100=31.25%
- TN Rate= (191/203) *100= 94.1%
- FP Rate= (12/203) *100=5.9%
In the context of the project, FP means that a patient with the death event value of (NO), meaning they did not die from the surgery, had been misclassified and given the value to the death event (YES) they will die because of the surgery. Thus, a doctor might not perform the surgery the patient needs in fear of them dying.

FN means that a patient whose death event is (YES) will die from the surgery had been misclassified and given the value to the death event (NO), death event will not occur. Thus, a doctor will perform surgery on a patient who will likely die from it. 

It is challenging to determine which of the two error are more critical. However, since a patient life is the most valuable, it is dangerous to perform surgery on him where he will likely die. No hospital will want a high FN Rate in a system because it will repeatedly recommend performing highly risky surgery on the patient. K-Nn algorithm have a high FN rate. Thus, we need to reduce it.




_Fined the full project document here_ :point_down:
[PROJECT-IS-FEMALE-Data-mining-group-jawaher-khlod-Raown-Ahlam.pdf](https://github.com/jawaher-alqotym/Data-mining-project/files/7664653/PROJECT-IS-FEMALE-Data-mining-group-jawaher-khlod-Raown-Ahlam.pdf)



