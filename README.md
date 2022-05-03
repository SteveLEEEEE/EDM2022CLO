# Dataset and source code for [Automatic Classification of Learning Objectives Based on Bloom’s Taxonomy](./Classification_of_Learning_Objectives_preprint.pdf) (EDM2022)

## 1. How the Dataset was Collected
We collected 21,380 learning objectives publicly available from 5,558 courses provided by the 10 faculties at an Australian university in 2021. To collect the data, we developed a web scraper using Python to automatically parse the content of the available course web pages to obtain learning objectives of a course. 


## 2. Files in the Dataset
The [data](./data/sample_full.csv) contains textual learning objectives as well as the humanly annotated labels in binary format for different Bloom's taxonomy levels. We also generate the [LIWC features](<./data/LIWC2015 Results (Learning_outcome.csv).csv>) using LIWC2015 for the machine learning experiments in our project.


## 3. Experiments
The experiments with respect to machine learning binary classifiers and BERT-based deep learning binary classifiers are in [this notebook](<./EDM2022 CLO.ipynb>) while the multi-label multi-class classifiers are in [this notebook](<./Multi-Label.ipynb>).


## 4. Results
<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" colspan="2" rowspan="2">Methods</th>
    <th class="tg-0lax" colspan="4"><span style="font-weight:bold">Remember</span></th>
    <th class="tg-0lax" colspan="4"><span style="font-weight:bold">Understand</span></th>
    <th class="tg-0lax" colspan="4"><span style="font-weight:bold">Apply</span></th>
  </tr>
  <tr>
    <th class="tg-0lax">Accuracy</th>
    <th class="tg-0lax">Cohen's Kappa</th>
    <th class="tg-0lax">AUC</th>
    <th class="tg-0lax">F1</th>
    <th class="tg-0lax">Accuracy</th>
    <th class="tg-0lax">Cohen's Kappa</th>
    <th class="tg-0lax">AUC</th>
    <th class="tg-0lax">F1</th>
    <th class="tg-0lax">Accuracy</th>
    <th class="tg-0lax">Cohen's Kappa</th>
    <th class="tg-0lax">AUC</th>
    <th class="tg-0lax">F1</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax" rowspan="6">Binary<br>Classifiers</td>
    <td class="tg-0lax">NB</td>
    <td class="tg-0lax">0.640</td>
    <td class="tg-0lax">0.111</td>
    <td class="tg-0lax">0.716</td>
    <td class="tg-0lax">0.198</td>
    <td class="tg-0lax">0.642</td>
    <td class="tg-0lax">0.327</td>
    <td class="tg-0lax">0.716</td>
    <td class="tg-0lax">0.581</td>
    <td class="tg-0lax">0.778</td>
    <td class="tg-0lax">0.507</td>
    <td class="tg-0lax">0.781</td>
    <td class="tg-0lax">0.668</td>
  </tr>
  <tr>
    <td class="tg-0lax">SVM</td>
    <td class="tg-0lax">0.982</td>
    <td class="tg-0lax">0.827</td>
    <td class="tg-0lax">0.923</td>
    <td class="tg-0lax">0.837</td>
    <td class="tg-0lax">0.922</td>
    <td class="tg-0lax">0.801</td>
    <td class="tg-0lax">0.891</td>
    <td class="tg-0lax">0.855</td>
    <td class="tg-0lax">0.923</td>
    <td class="tg-0lax">0.805</td>
    <td class="tg-0lax">0.890</td>
    <td class="tg-0lax">0.858</td>
  </tr>
  <tr>
    <td class="tg-0lax">LR</td>
    <td class="tg-0lax">0.960</td>
    <td class="tg-0lax">0.485</td>
    <td class="tg-0lax">0.681</td>
    <td class="tg-0lax">0.503</td>
    <td class="tg-0lax">0.891</td>
    <td class="tg-0lax">0.714</td>
    <td class="tg-0lax">0.839</td>
    <td class="tg-0lax">0.787</td>
    <td class="tg-0lax">0.896</td>
    <td class="tg-0lax">0.726</td>
    <td class="tg-0lax">0.837</td>
    <td class="tg-0lax">0.793</td>
  </tr>
  <tr>
    <td class="tg-0lax">RF</td>
    <td class="tg-0lax">0.983</td>
    <td class="tg-0lax">0.830</td>
    <td class="tg-0lax">0.892</td>
    <td class="tg-0lax">0.839</td>
    <td class="tg-0lax">0.920</td>
    <td class="tg-0lax">0.793</td>
    <td class="tg-0lax">0.880</td>
    <td class="tg-0lax">0.847</td>
    <td class="tg-0lax">0.936</td>
    <td class="tg-0lax">0.837</td>
    <td class="tg-0lax">0.904</td>
    <td class="tg-0lax">0.881</td>
  </tr>
  <tr>
    <td class="tg-0lax">XGBoost</td>
    <td class="tg-0lax">0.981</td>
    <td class="tg-0lax">0.820</td>
    <td class="tg-0lax">0.916</td>
    <td class="tg-0lax">0.830</td>
    <td class="tg-0lax">0.928</td>
    <td class="tg-0lax">0.818</td>
    <td class="tg-0lax">0.900</td>
    <td class="tg-0lax">0.867</td>
    <td class="tg-0lax">0.938</td>
    <td class="tg-0lax">0.844</td>
    <td class="tg-0lax">0.914</td>
    <td class="tg-0lax">0.887</td>
  </tr>
  <tr>
    <td class="tg-0lax">BERT</td>
    <td class="tg-0lax"><span style="font-weight:bold">0.987</span></td>
    <td class="tg-0lax"><span style="font-weight:bold">0.871</span></td>
    <td class="tg-0lax">0.916</td>
    <td class="tg-0lax"><span style="font-weight:bold">0.878</span></td>
    <td class="tg-0lax"><span style="font-weight:bold">0.971</span></td>
    <td class="tg-0lax"><span style="font-weight:bold">0.926</span></td>
    <td class="tg-0lax">0.959</td>
    <td class="tg-0lax"><span style="font-weight:bold">0.947</span></td>
    <td class="tg-0lax"><span style="font-weight:bold">0.961</span></td>
    <td class="tg-0lax"><span style="font-weight:bold">0.904</span></td>
    <td class="tg-0lax">0.951</td>
    <td class="tg-0lax"><span style="font-weight:bold">0.931</span></td>
  </tr>
  <tr>
    <td class="tg-0lax" rowspan="2">MCML<br>Classifiers</td>
    <td class="tg-0lax">RF</td>
    <td class="tg-0lax">0.982</td>
    <td class="tg-0lax">0.809</td>
    <td class="tg-0lax"><span style="font-weight:bold">0.989</span></td>
    <td class="tg-0lax">0.818</td>
    <td class="tg-0lax">0.927</td>
    <td class="tg-0lax">0.811</td>
    <td class="tg-0lax">0.970</td>
    <td class="tg-0lax">0.860</td>
    <td class="tg-0lax">0.921</td>
    <td class="tg-0lax">0.794</td>
    <td class="tg-0lax">0.970</td>
    <td class="tg-0lax">0.847</td>
  </tr>
  <tr>
    <td class="tg-0lax">BERT</td>
    <td class="tg-0lax">0.984</td>
    <td class="tg-0lax">0.848</td>
    <td class="tg-0lax">0.988</td>
    <td class="tg-0lax">0.856</td>
    <td class="tg-0lax">0.955</td>
    <td class="tg-0lax">0.889</td>
    <td class="tg-0lax"><span style="font-weight:bold">0.982</span></td>
    <td class="tg-0lax">0.920</td>
    <td class="tg-0lax">0.951</td>
    <td class="tg-0lax">0.877</td>
    <td class="tg-0lax"><span style="font-weight:bold">0.976</span></td>
    <td class="tg-0lax">0.912</td>
  </tr>
  <tr>
    <td class="tg-0lax" colspan="2" rowspan="2">Methods</td>
    <td class="tg-0lax" colspan="4"><span style="font-weight:bold">Analyze</span></td>
    <td class="tg-0lax" colspan="4"><span style="font-weight:bold">Evaluate</span></td>
    <td class="tg-0lax" colspan="4"><span style="font-weight:bold">Create</span></td>
  </tr>
  <tr>
    <td class="tg-0lax">Accuracy</td>
    <td class="tg-0lax">Cohen's Kappa</td>
    <td class="tg-0lax">AUC</td>
    <td class="tg-0lax">F1</td>
    <td class="tg-0lax">Accuracy</td>
    <td class="tg-0lax">Cohen's Kappa</td>
    <td class="tg-0lax">AUC</td>
    <td class="tg-0lax">F1</td>
    <td class="tg-0lax">Accuracy</td>
    <td class="tg-0lax">Cohen's Kappa</td>
    <td class="tg-0lax">AUC</td>
    <td class="tg-0lax">F1</td>
  </tr>
  <tr>
    <td class="tg-0lax" rowspan="6">Binary<br>Classifiers</td>
    <td class="tg-0lax">NB</td>
    <td class="tg-0lax">0.549</td>
    <td class="tg-0lax">0.183</td>
    <td class="tg-0lax">0.684</td>
    <td class="tg-0lax">0.392</td>
    <td class="tg-0lax">0.596</td>
    <td class="tg-0lax">0.234</td>
    <td class="tg-0lax">0.703</td>
    <td class="tg-0lax">0.447</td>
    <td class="tg-0lax">0.676</td>
    <td class="tg-0lax">0.300</td>
    <td class="tg-0lax">0.743</td>
    <td class="tg-0lax">0.474</td>
  </tr>
  <tr>
    <td class="tg-0lax">SVM</td>
    <td class="tg-0lax">0.956</td>
    <td class="tg-0lax">0.832</td>
    <td class="tg-0lax">0.897</td>
    <td class="tg-0lax">0.858</td>
    <td class="tg-0lax">0.959</td>
    <td class="tg-0lax">0.861</td>
    <td class="tg-0lax">0.922</td>
    <td class="tg-0lax">0.886</td>
    <td class="tg-0lax">0.942</td>
    <td class="tg-0lax">0.791</td>
    <td class="tg-0lax">0.880</td>
    <td class="tg-0lax">0.825</td>
  </tr>
  <tr>
    <td class="tg-0lax">LR</td>
    <td class="tg-0lax">0.936</td>
    <td class="tg-0lax">0.732</td>
    <td class="tg-0lax">0.818</td>
    <td class="tg-0lax">0.767</td>
    <td class="tg-0lax">0.920</td>
    <td class="tg-0lax">0.694</td>
    <td class="tg-0lax">0.799</td>
    <td class="tg-0lax">0.739</td>
    <td class="tg-0lax">0.902</td>
    <td class="tg-0lax">0.604</td>
    <td class="tg-0lax">0.762</td>
    <td class="tg-0lax">0.659</td>
  </tr>
  <tr>
    <td class="tg-0lax">RF</td>
    <td class="tg-0lax">0.961</td>
    <td class="tg-0lax">0.851</td>
    <td class="tg-0lax">0.902</td>
    <td class="tg-0lax">0.874</td>
    <td class="tg-0lax">0.967</td>
    <td class="tg-0lax">0.887</td>
    <td class="tg-0lax">0.932</td>
    <td class="tg-0lax">0.907</td>
    <td class="tg-0lax">0.943</td>
    <td class="tg-0lax">0.792</td>
    <td class="tg-0lax">0.877</td>
    <td class="tg-0lax">0.826</td>
  </tr>
  <tr>
    <td class="tg-0lax">XGBoost</td>
    <td class="tg-0lax">0.959</td>
    <td class="tg-0lax">0.844</td>
    <td class="tg-0lax">0.903</td>
    <td class="tg-0lax">0.868</td>
    <td class="tg-0lax">0.964</td>
    <td class="tg-0lax">0.878</td>
    <td class="tg-0lax">0.924</td>
    <td class="tg-0lax">0.900</td>
    <td class="tg-0lax">0.944</td>
    <td class="tg-0lax">0.796</td>
    <td class="tg-0lax">0.882</td>
    <td class="tg-0lax">0.829</td>
  </tr>
  <tr>
    <td class="tg-0lax">BERT</td>
    <td class="tg-0lax"><span style="font-weight:bold">0.975</span></td>
    <td class="tg-0lax"><span style="font-weight:bold">0.906</span></td>
    <td class="tg-0lax">0.950</td>
    <td class="tg-0lax"><span style="font-weight:bold">0.922</span></td>
    <td class="tg-0lax">0.974</td>
    <td class="tg-0lax">0.913</td>
    <td class="tg-0lax">0.954</td>
    <td class="tg-0lax">0.929</td>
    <td class="tg-0lax"><span style="font-weight:bold">0.962</span></td>
    <td class="tg-0lax"><span style="font-weight:bold">0.866</span></td>
    <td class="tg-0lax">0.924</td>
    <td class="tg-0lax"><span style="font-weight:bold">0.888</span></td>
  </tr>
  <tr>
    <td class="tg-0lax" rowspan="2">MCML<br>Classifiers</td>
    <td class="tg-0lax">RF</td>
    <td class="tg-0lax">0.951</td>
    <td class="tg-0lax">0.803</td>
    <td class="tg-0lax">0.972</td>
    <td class="tg-0lax">0.831</td>
    <td class="tg-0lax">0.950</td>
    <td class="tg-0lax">0.822</td>
    <td class="tg-0lax">0.981</td>
    <td class="tg-0lax">0.852</td>
    <td class="tg-0lax">0.928</td>
    <td class="tg-0lax">0.715</td>
    <td class="tg-0lax">0.964</td>
    <td class="tg-0lax">0.755</td>
  </tr>
  <tr>
    <td class="tg-0lax">BERT</td>
    <td class="tg-0lax">0.971</td>
    <td class="tg-0lax">0.890</td>
    <td class="tg-0lax"><span style="font-weight:bold">0.984</span></td>
    <td class="tg-0lax">0.907</td>
    <td class="tg-0lax"><span style="font-weight:bold">0.974</span></td>
    <td class="tg-0lax"><span style="font-weight:bold">0.914</span></td>
    <td class="tg-0lax"><span style="font-weight:bold">0.989</span></td>
    <td class="tg-0lax"><span style="font-weight:bold">0.930</span></td>
    <td class="tg-0lax">0.958</td>
    <td class="tg-0lax">0.846</td>
    <td class="tg-0lax"><span style="font-weight:bold">0.971</span></td>
    <td class="tg-0lax">0.872</td>
  </tr>
</tbody>
</table>

## 5. Contact
For any questions about the dataset or the notebooks, please contact Yuheng Li via yuheng.li@monash.edu or yuhengleeeee@gmail.com

## 6. Citation
If you are using our data or codes, please cite (the BibTeX will be updated when the paper is published):
```
@paper{EDM2022CLO,
  author = {Yuheng Li, Mladen Raković, Boon Xin Poh, Dragan Gašević, Guanliang Chen},
  title = {Automatic Classification of Learning Objectives Based on Bloom's Taxonomy},
  conference = {The 15th International Conference on Educational Data Mining},
  year = {2022}
}

```