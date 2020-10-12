## Elaborazione di serie temporali per il rapporto '_Gli indicatori del clima in Italia_'

```
La ricerca climatica si basa sullo studio dei trend di lungo periodo dei 
fenomeni metereologici (Anderson and Gough, 2018)
```

<img src="./docs/figure/sankeyDiagram2.png" width="90%" alt="Sankey diagram for temperature serie">

Il diagramma mostra una rappresentazione grafica intuitiva del processo di identificazione ed elaborazione delle serie di temperatura
che contribuiscono al Rapporto "_Gli Indicatori del Clima in Italia_". Tale processo si articola nelle seguenti fasi:
- Controlli di qualità
- Selezione delle serie in base ai criteri di:
  - lunghezza
  - completezza & continuità
- Identificazione delle discontinuità (breakpoints) e omogeneizzazione delle serie
- Analisi statistica:
  - stima dei trend
  - calcolo degli indici estremi
  - calcolo dei valori climatologici
  - altro
  
---

## Bibliografia

[Guide to Climatological Practices](https://library.wmo.int/doc_num.php?explnum_id=5541). WMO, 2018.

### Missing values

**Regola del "3/5"**

Un mese risulta valido se presenta:
- al più 5 giorni mancanti
- al più 3 giorni mancanti consecutivi

La regola del "3/5" nasce per il calcolo dei valori climatologici ma viene comunque utilizzata nel controllo di qualita' dei dati per altri tipi 
di analisi come l'analisi delle serie storiche e lo studio dei trend (Anderson e Gough, 2018).

:point_right: [Accounting for missing data in monthly temperature series: Testing rule-of-thumb omission of months with missing values](https://rmets.onlinelibrary.wiley.com/doi/pdf/10.1002/joc.5801). Anderson and Gough, 2018.

### Controlli di qualità

:point_right: [Controlli di qualità delle serie di temperatura e  precipitazione](http://www.scia.isprambiente.it/wwwrootscia/Documentazione/Rapporto_controlli_qualit%c3%a0_clima.pdf). ISPRA, 2016.

:point_right: [Comprehensive Automated Quality Assurance of Daily Surface Observations](https://journals.ametsoc.org/jamc/article/49/8/1615/13419/Comprehensive-Automated-Quality-Assurance-of-Daily). Durre et al., 2010.

### Breakpoint point detection

:point_right: [Homogeneity of 20th century European daily temperature and precipitation series](https://rmets.onlinelibrary.wiley.com/doi/10.1002/joc.906). Wijngaard et al., 2003.

### Homogenization

:point_right: [Application of homogenization methods for Ireland'smonthly precipitation records: Comparison of breakdetection results](https://mural.maynoothuniversity.ie/12842/1/joc.6575.pdf). Coll et al., 2020.

:point_right: [Comparison of homogenization methods for daily temperature series against an observation-based benchmark dataset](https://link.springer.com/article/10.1007/s00704-019-03018-0). Squintu et al., 2020.

### Valori climatologici

:point_right: [WMO Guidelines on the Calculation of Climate Normals](https://library.wmo.int/doc_num.php?explnum_id=4166). WMO, 2017

### Stima dei trend

:point_right: [Temperature and precipitation trends in Canada during the 20th century](https://doi.org/10.1080/07055900.2000.9649654). Zhang et al., 2000.

:point_right: [The influence of autocorrelation on the ability to detect trend in hydrological series](https://www.pacificclimate.org/~wernera/zyp/Yue%20Pilon%20Phinney%20Cavadias%202002%20HP.pdf). Yue et al., 2002.

### Indici ETCCDI

:point_right: [Guidelines on Analysis of extremes in a changing climate in support of informed decisions for adaptation](https://www.ecad.eu/documents/WCDMP_72_TD_1500_en_1.pdf), 2009. WMO.

:point_right: [On the use of indices to study extreme precipitation on sub-daily and daily timescales](https://iopscience.iop.org/article/10.1088/1748-9326/ab51b6). Lisa V Alexander et al., 2019.

:point_right: [Indices for monitoring changes in extremes based on daily temperature and precipitation data](https://www.academia.edu/13435321/Indices_for_monitoring_changes_in_extremes_based_on_daily_temperature_and_precipitation_data). Zhang et al., 2011.

:point_right: [Development of an Updated Global Land In Situ‐Based Data Set of Temperature and Precipitation Extremes: HadEX3](https://agupubs.onlinelibrary.wiley.com/doi/pdf/10.1029/2019JD032263). Dunn et al., 2020. 

### Indici ET-SCI

Si tratta di indici focalizzati sugli impatti e che utilizzano soglie specificate dall'utente.

:point_right: [Expert Team on Sector-Specific Climate Indices (ET-SCI)](https://climpact-sci.org/about/project/)

:point_right:  [Introduction to the ET-SCI indices](https://www.wmo.int/pages/prog/wcp/ccl/opace/opace4/meetings/documents/fiji2015/D3-2-Alexander_Intro_to_ETSCI_indices.pdf)


:point_right:  [Useful indicesper sector](https://climpact-sci.org/indices/)

---

## Software :floppy_disk: 

Si tratta per lo piu' di una lista di pacchetti per il linguaggio R.

### Visualizzazione dei dati mancanti

- [naniar](https://cran.r-project.org/web/packages/naniar/vignettes/getting-started-w-naniar.html)

- [visdat](https://github.com/ropensci/visdat)

### Controlli di qualità dei dati

- [RClimDex](https://github.com/ECCC-CDAS/RClimDex) `r emojifont::emoji("point_left")`

- [dataresqc](https://datarescue.climate.copernicus.eu/node/54)

### Test per l'identificazione di breakpoints

- [trend](https://cran.r-project.org/web/packages/trend/vignettes/trend.pdf)

### Breakpoints detection and Homogenization

- [Climatol](https://cran.r-project.org/web/packages/climatol/index.html)

- [ACMANT](https://github.com/dpeterfree/ACMANT)

- [Lista molto completa dei software disponibili](http://www.climatol.eu/tt-hom/)

### Indici estremi

- [climdex.pcic](https://github.com/pacificclimate/climdex.pcic)

- [climpact2](https://github.com/ARCCSS-extremes/climpact2)

- La pagina web [www.climdex.org](www.climdex.org) offre una versione web di Climpact

### Analisi (non parametrica) dei trend e pre-whitening delle serie

- [zyp](https://cran.r-project.org/web/packages/zyp/zyp.pdf)


