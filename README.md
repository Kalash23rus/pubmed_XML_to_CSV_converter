# pubmed_XML_to_CSV_converter
this python3.x script converts pubmed_result.xml to csv format

import xml.etree.ElementTree as et 
import pandas as pd
import pubmed_parser as pp

parse_pbresult_pl_biotech = pp.parse_medline_xml('pubmed_result.xml', year_info_only=True)
df_parse_pbresult_pl_biotech = pd.DataFrame(parse_pbresult_pl_biotech)
df_parse_pbresult_pl_biotech.to_csv('pubmed_result.csv')
