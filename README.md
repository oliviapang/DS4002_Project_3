# DS4002_Project_3
## Table of Contents
1. Software and Platform  
2. Documentation Map  
3. Instructions for Reproduction  

## Software and Platform
Softwares used: Google Collab and Python 3.13.15    
Add-ons: pandas 2.2.3, numpy 2.1.3, matplotlib.pyplot 3.10.0, seaborn 0.13.2, scikit-learn 1.6.1, joblib 1.6.0    
Platform: Windows
## Documentation Map
```mermaid
graph TD
    %% Repository Root
    Repo[Repository]

    %% Top Level Folders & Files
    Repo --> DATA[DATA]
    Repo --> OUTPUT[OUTPUT]
    Repo --> SCRIPTS[SCRIPTS]
    Repo --> LICENSE[LICENSE.md]
    Repo --> README_ROOT[README.md]

    %% DATA Directory Chain
    DATA --> D1[README.md]
    D1 --> D2[cleaned_aic_paintings_colab.csv]
    D2 --> D3[cleaned_aic_style_counts_colab.csv]

    %% OUTPUT Directory Chain
    OUTPUT --> O1[classification_report.txt]
    O1 --> O2[confusion_matrix.csv]
    O2 --> O3[confusion_matrix.png]
    O3 --> O4[convnext_art_movement.pt]
    O4 --> O5[cv_fold1_history.csv]
    O5 --> O6[cv_fold2_history.csv]
    O6 --> O7[cv_fold3_history.csv]
    O7 --> O8[cv_fold4_history.csv]
    O8 --> O9[cv_fold5_history.csv]
    O9 --> O10[cv_results.csv]
    O10 --> O11[final_train_history.csv]
    O11 --> O12[gradcam.png]
    O12 --> O13[test_metrics.json]
    O13 --> O14[test_predictions.csv]
    O14 --> O15[test_split.csv]
    O15 --> O16[train_split.csv]

    %% SCRIPTS Directory Chain
    SCRIPTS --> S1[1_Cleaning_EDA_Script.ipynb]
    S1 --> S2[2_Build_and_Test_Model.ipynb]

    %% Color Styling to Match Reference
    classDef purple fill:#E1D5E7,stroke:#9673A6,stroke-width:1.5px,color:#000;
    classDef blue fill:#DAE8FC,stroke:#6C8EBF,stroke-width:1.5px,color:#000;
    classDef green fill:#D5E8D4,stroke:#82B366,stroke-width:1.5px,color:#000;

    class Repo purple;
    class DATA,OUTPUT,SCRIPTS,LICENSE,README_ROOT blue;
    class D1,D2,D3,O1,O2,O3,O4,O5,O6,O7,O8,O9,O10,O11,O12,O13,O14,O15,O16,S1,S2 green;

```
## Instructions for Reproduction 

## References

