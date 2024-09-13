<img src="https://formacionmassalud.iavante.es/pluginfile.php/1/theme_edumy/headerlogo2/1722409266/logo-web-fps-718x150%20v2%20copia.png" alt="Fundación Progreso y salud" style="float: right; width: 200px; height: auto; margin-left: 10px;">

# IBD Project

## FPS-EII-2021-04

Development and validation of Machine Learning models for the prediction of medium-to-long-term clinical remission in patients with Crohn's disease and ulcerative colitis treated with vedolizumab and ustekinumab.

## Summary

This project involves the collaboration of the Big Data Area of the Progreso y Salud Foundation and the Virgen Macarena University Hospital. We aim to develop a clinical decision support system based on models for predicting medium- and long-term treatment response with vedolizumab and ustekinumab (clinical response at 26 and 52 weeks, and clinical remission at 52 weeks) using patient clinical information before the start of biological treatment. This could help healthcare professionals properly manage resources for these patients and improve the management and control of the disease. The goal is to determine which variables are most relevant for the models when making decisions and how their values affect a positive or negative response in the target variables.

In addition to the general cohort, subcohorts will be created by grouping patients by medication and disease, for which the target variables will be predicted, just as in the general cohorts.

## Inclusion / Exclusion Criteria

The study population includes subjects from the Andalusian Public Health System in the area served by HUVM, meeting the following inclusion criteria and none of the exclusion criteria:

**Inclusion criteria:**

- Be of legal age (>18 years).
- Coded diagnosis of moderate-to-severe Crohn's disease or Ulcerative Colitis.
- Being or having been treated with ustekinumab and/or vedolizumab.

**Exclusion criteria:**

- No availability/access to electronic health record data.
- Less than 50% of study variables recorded.
- Loss of patient follow-up before week 26 after starting the drug.

## Variables

Not all variables are included in the model; only those most relevant to the target variables are selected according to clinical criteria.

### Independent

| Name | Type | Units | Description |
| --- | --- | --- | --- |
| ID | Text | - | Anonymized patient ID. |
| fecha_inicio_far | Date | dd/mm/yyyy | Start date of drug treatment. |
| fecha_diag | Date | dd/mm/yyyy | Date of disease diagnosis. |
| ppio_activo | Factor | - | Biological treatment drug:<br>USTEKINUMAB<br>VEDOLIZUMAB |
| sexo | Factor | - | Biological sex of the patient. |
| familia_eii | factor | - | Family history of IBD:<br><br>none (0)<br>first degree (1)<br>second degree(2) |
| loc_ec | factor | - | Crohn's Disease location:<br><br>Other disease (0)<br>Ileal (1)<br>Colonic (2)<br>Ileocolonic (3)<br>Ileocolonic + upper (4)<br>Ileal + upper (5) |
| comp_ec | factor | - | Crohn's Disease behavior:<br><br>Other disease (0)<br>Inflammatory (1)<br>Stenosing (2)<br>Fistulizing (3) |
| exten_cu | factor | - | Ulcerative Colitis extension:<br><br>Other disease (0)<br>Proctitis (1)<br>Left-sided colitis (2)<br>Pancolitis (3) |
| tipo_eii | factor | - | Disease type:<br><br>Crohn's Disease (CD)<br>Ulcerative Colitis (UC) |
| preianal | Factor | - | Appearance of recurrent perianal fistulas:<br><br>Yes (1)<br>No (0) |
| ada_previo | Factor | - | Previous treatment with Adalimumab (a type of TNF):<br><br>Yes (1)<br>No (0) |
| ifx_previo | Factor | - | Previous treatment with Infliximab (a type of TNF):<br><br>Yes (1)<br>No (0) |
| uste_previo | Factor | - | Previous treatment with Ustekinumab (a type of Biologic):<br><br>Yes (1)<br>No (0) |
| vedo_previo | Factor | - | Previous treatment with Vedolizumab (a type of Biologic):<br><br>Yes (1)<br>No (0) |
| tofa_previo | Factor | - | Previous treatment with Tofacitinib (a type of Biologic):<br><br>Yes (1)<br>No (0) |
| certol_previo | Factor | - | Previous treatment with Certolizumab (a type of Biologic):<br><br>Yes (1)<br>No (0) |
| golim_previo | Factor | - | Previous treatment with Golimumab (a type of Biologic):<br><br>Yes (1)<br>No (0) |
| cx_previa_eii | Factor | - | Previous surgery related to IBD before starting the drug:<br><br>Yes (1)<br>No (0) |
| tabaco | Factor | - | Indicates if the patient smokes at the start of the drug:<br><br>Non-smoker (0)<br>Smoker (1)<br>Ex-smoker (2) |
| meis_espondiloartropatías | Factor | - | Extraintestinal manifestations, spondyloarthropathies:<br><br>Present (1)<br>Not present (0) |
| meis_uveitis | Factor | - | Extraintestinal manifestations, uveitis:<br><br>Present (1)<br>Not present (0) |
| meis_eritema_nodoso | Factor | - | Extraintestinal manifestations, erythema nodosum:<br><br>Present (1)<br>Not present (0) |
| meis_pioderma_gangrenoso | Factor | - | Extraintestinal manifestations, pyoderma gangrenosum:<br><br>Present (1)<br>Not present (0) |
| meis_colangitis_esclerosanteprimaria | Factor | - | Extraintestinal manifestations, primary sclerosing cholangitis:<br><br>Present (1)<br>Not present (0) |
| meis_estomatitis_aftosa | Factor | - | Extraintestinal manifestations, aphthous stomatitis:<br><br>Present (1)<br>Not present (0) |
| meis_SdSweet | Factor | - | Extraintestinal manifestations, Sweet’s syndrome:<br><br>Present (1)<br>Not present (0) |
| meis_psoriasis | Factor | - | Extraintestinal manifestations, psoriasis:<br><br>Present (1)<br>Not present (0) |
| meis_hidrosiadenitis | Factor | - | Extraintestinal manifestations, hidradenitis:<br><br>Present (1)<br>Not present (0) |
| meis_vasculitis | Factor | - | Extraintestinal manifestations, vasculitis:<br><br>Present (1)<br>Not present (0) |
| meis_vitiligo | Factor | - | Extraintestinal manifestations, vitiligo:<br><br>Present (1)<br>Not present (0) |
| meis_osteoporosis | Factor | - | Extraintestinal manifestations, osteoporosis:<br><br>Present (1)<br>Not present (0) |
| meis_fenom_tromboembolico | Factor | - | Extraintestinal manifestations, thromboembolic phenomenon:<br><br>Present (1)<br>Not present (0) |
| edad_inicio_far | Integer | Years | Patient's age at the start of the drug. |
| edad_diag | Integer | Years | Patient's age at disease diagnosis. |
| cort_12m_previo | Factor | - | Indicates if the patient took corticosteroids in the 12 months prior to starting the drug:<br><br>Took corticosteroids (1)<br>Did not take corticosteroids (0) |
| diabetes | Factor | - | Indicates if the patient was diagnosed with diabetes at the start of the drug:<br><br>Diagnosed (1)<br>Not diagnosed (0) |
| asma | Factor | - | Indicates if the patient was diagnosed with asthma at the start of the drug:<br><br>Diagnosed (1)<br>Not diagnosed (0) |
| vih | Factor | - | Indicates if the patient was diagnosed with HIV at the start of the drug:<br><br>Diagnosed (1)<br>Not diagnosed (0) |
| migrana | Factor | - | Indicates if the patient was diagnosed with migraine at the start of the drug:<br><br>Diagnosed (1)<br>Not diagnosed (0) |
| calprotectina | Continuous | µg/g | Fecal calprotectin levels, collected between 8 weeks before and the start of the drug. |
| lab_velocidad_sed_globular | Continuous | mm/h | Erythrocyte sedimentation rate in mm/h in whole blood. |
| lab_sodio | Continuous | mEq/L | Sodium concentration in mEq/L in serum. |
| lab_aspartato_transaminasa | Integer | U/L | Aspartate transaminase enzyme activity in U/L in serum. |
| lab_glucosa | Continuous | mg/dL | Glucose level in mg/dL in serum. |
| lab_proteinas_totales | Continuous | g/dL | Total protein concentration in g/dL in serum. |
| lab_urea | Continuous | mg/dL | Urea level in mg/dL in serum. |
| lab_potasio | Continuous | mEq/L | Potassium concentration in mEq/L in serum. |
| lab_fosfato | Continuous | mg/dL | Phosphate concentration in mg/dL in serum. |
| lab_proteina_C | Continuous | mg/L | C-reactive protein concentration in mg/L in serum. |

### Dependent

| Name | Type | Units | Description |
| --- | --- | --- | --- |
| id_paciente | Text | - | Anonymized patient ID. |
| remision_clinica_26s | Factor | - | Indicates whether clinical remission was achieved 26 weeks after starting the drug:<br><br>Achieved (1)<br>Not achieved (0) |
| remision_clinica_52s | Factor | - | Indicates whether clinical remission was achieved 52 weeks after starting the drug:<br><br>Achieved (1)<br>Not achieved (0) |
| respuesta_clinica_26s | Factor | - | Indicates whether a clinical response was achieved 26 weeks after starting the drug:<br><br>Achieved (1)<br>Not achieved (0) |
| respuesta_clinica_52s | Factor | - | Indicates whether a clinical response was achieved 52 weeks after starting the drug:<br><br>Achieved (1)<br>Not achieved (0) |

We will only use the target variables: respuesta_clinica_26s, respuesta_clinica_52s, and remision_clinica_52s to train the predictive models.