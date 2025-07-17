# CCR development 

This repo serves as a landing pad for active areas of development of our Coastal Climate Resilience (CCR) program. Specifically, this repo houses 1-pager .md documents ready for development, and also a hub to communicate via the **Issues** tab. 

### 1-pager project descriptions 
<table>
  <tr> <td> <b> <a href="https://github.com/Seattle-Aquarium/CCR_development/blob/main/1-pagers/AI-ML_image_processing.md"> AI/ML to process .GPR photos </a> </b> </td> <td> Explore AI/ML methods to use raw .GPR input and processed .JPEG outputs to train a model to assist with photo processing, our most rate-limiting step </td> </tr>
  <tr> <td> <b> <a href="https://github.com/zhrandell/Seattle_Aquarium_CCR_development/blob/main/1-pagers/bull_kelp_tracking.md"> bull_kelp_tracking </a> </b> </td> <td> Identify a computer vision path forward for detecting and tracking bull kelp stipes </td> </tr>
  <tr> <td> <a href="https://github.com/zhrandell/Seattle_Aquarium_CCR_development/blob/main/1-pagers/localization_fixit.md"> <b> ArduSub Localization Fixit </b> </a> </td> <td> BlueOS extension to diagnose and fix common localization problems </td> </tr>
 </table>

<!---  <tr> <td> <a href="URL"> <b> TITLE </b> </a> </td> <td> DESCRIPTION </td> </tr>  -->

# CCR GitHub repos

## General information; workflows ready to implement
The following repos contain general information about our work, and specialized repos for ROV telemetry analyses, processing and analyses of ROV-derived benthic abundance and distribution data, and simulating benthic data.  

```mermaid
graph TD

A["<a href='https://github.com/Seattle-Aquarium/Coastal_Climate_Resilience' target='_blank' style='font-size: 16px; font-weight: bold;'>Coastal_Climate_Resilience</a><br><font color='darkgray'>the main landing pad for the CCR research program</font>"]

A --> E["<a href='https://github.com/Seattle-Aquarium/CCR_analytical_resources' target='_blank' style='font-size: 16px; font-weight: bold;'>CCR_ROV_telemetry_processing</a><br><font color='darkgray'>analytical tools for working with ROV telemetry data</font>"]

A --> F["<a href='https://github.com/Seattle-Aquarium/CCR_benthic_analyses' target='_blank' style='font-size: 16px; font-weight: bold;'>CCR_benthic_analyses</a><br><font color='darkgray'>code to work with ROV-derived benthic community data</font>"]

A --> G["<a href='https://github.com/Seattle-Aquarium/CCR_benthic_taxa_simulation' target='_blank' style='font-size: 16px; font-weight: bold;'>CCR_benthic_taxa_simulation</a><br><font color='darkgray'>code to simulate ROV-derived benthic community</font>"]
```

## Help wanted! 
The following repos involve active areas of open-source software development, AI/ML implementation, and computer vision challenges; areas where we could use assistance are 🔶 highlighted in orange 🔶

```mermaid
graph TD

B["<a href='https://github.com/Seattle-Aquarium/CCR_development' target='_blank' style='font-size: 16px; font-weight: bold;'>CCR_development</a><br><font color='darkgray'>main hub for organizing active Issues under development </font>"]

B --> C["<a href='https://github.com/Seattle-Aquarium/CCR_image_processing' target='_blank' style='font-size: 16px; font-weight: bold;'>CCR_image_processing</a><br><font color='darkgray'>help wanted to implement AI/ML solution to expendite image processing</font>"]

B --> D["<a href='https://github.com/Seattle-Aquarium/CCR_kelp_feature_detection' target='_blank' style='font-size: 16px; font-weight: bold;'>CCR_kelp_feature_detection</a><br><font color='darkgray'>active research re: photogrammetry in kelp forests</font>"]

style B stroke:#FF8600,stroke-width:4px
style C stroke:#FF8600,stroke-width:4px
```
