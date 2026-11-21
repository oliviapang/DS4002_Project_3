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
flowchart TD
    %% Styling
    classDef data fill:#e1f5fe,stroke:#0288d1,stroke-width:2px,color:#01579b
    classDef script1 fill:#f3e5f5,stroke:#7b1fa2,stroke-width:2px,color:#4a148c
    classDef script2 fill:#e8f5e9,stroke:#388e3c,stroke-width:2px,color:#1b5e20
    classDef output fill:#fff3e0,stroke:#f57c00,stroke-width:2px,color:#e65100

    %% External Input
    RAW[("aic_paintings_movements_links (1).csv<br/><i>Raw AIC API metadata (1,586 rows)</i>")]:::data

    %% SCRIPTS Folder - Script 1
    subgraph SCRIPTS ["SCRIPTS/"]
        direction TB
        S1["<b>1_Cleaning_EDA_Script.ipynb</b><br/>• Deduplicate & handle missing artist/medium nulls<br/>• Split semicolon style tags & remap 64 raw tags &rarr; 17 categories<br/>• Plot pre/post-mapping bar charts & co-occurrence heatmaps"]:::script1

        S2["<b>2_Build_and_Test_Model.ipynb</b><br/>• Extract primary style & download images via AIC IIIF URLs<br/>• Drop rare classes (&lt;15 samples &rarr; 1,558 paintings, 14 classes)<br/>• Stratified 80/20 split (1,246 train / 312 test)<br/>• 5-Fold Stratified CV + Two-Stage ConvNeXt-Tiny Fine-Tuning<br/>• Generate test metrics, confusion matrix & Grad-CAM overlays"]:::script2
    end

    %% DATA Folder
    subgraph DATA ["DATA/"]
        direction TB
        D1[("cleaned_aic_paintings_colab.csv<br/><i>Cleaned dataset with remapped Style lists</i>")]:::data
        D2[("cleaned_aic_style_counts_colab.csv<br/><i>Aggregated style frequency counts</i>")]:::data
    end

    %% OUTPUT Folder
    subgraph OUTPUT ["OUTPUT/"]
        direction TB
        O_SPLITS[("train_split.csv<br/>test_split.csv")]:::output
        O_CV[("cv_results.csv<br/>cv_fold1_history.csv ... cv_fold5_history.csv")]:::output
        O_MODEL[("convnext_art_movement.pt <i>(external link)</i><br/>final_train_history.csv")]:::output
        O_EVAL[("test_metrics.json / classification_report.txt<br/>test_predictions.csv / confusion_matrix.csv<br/>confusion_matrix.png / gradcam.png")]:::output
    end

    %% Pipeline Connections
    RAW --> S1
    S1 --> D1
    S1 --> D2
    D1 --> S2
    S2 --> O_SPLITS
    S2 --> O_CV
    S2 --> O_MODEL
    S2 --> O_EVAL
## Instructions for Reproduction 

## References

