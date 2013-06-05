In deze map bevindt zich alles wat met de administratie van hackerspace VoidWarranties te maken heeft.

De statuten die zich hier bevinden zijn onder voorbehoudt, de officiële statuten vindt je in de publicaties van het staatsblad:

<http://www.ejustice.just.fgov.be/tsv_pdf/2011/03/16/11041542.pdf>

<http://www.ejustice.just.fgov.be/tsv_pdf/2012/08/17/12143193.pdf>

Wijzigingen aanbrengen
======================

Bepaalde bestanden kunnen niet zomaar gewijzigd worden:
* De statuten kunnen enkel gewijzigd worden op een algemene vergadering en volgens de in de statuten omschreven regels.
* De huisregels kunnen enkel worden aangepast op een monthly meeting.

Pull requests op bovenstaande bestanden zullen enkel aanvaard worden nadat deze aanpassingen goedgekeurd zijn.

PDFs genereren
==============

Markdown bestanden kunnen omgezet worden in een PDF door gebruik te maken van pandoc:

    pandoc -o donation.pdf donation.markdown

Of gebaseerd op de officiële repo:

    curl https://raw.github.com/voidwarranties/bureaucracy/master/huisregels.md |  pandoc -o donation.pdf

Hiervoor dient LaTeX geïnstalleerd te zijn. 
In de repository zit ook aangepaste template om pdf's te generen, die je op deze manier gebruikt:

    pandoc --template=template.tex --latex-engine=xelatex  -o donation.pdf donation.markdown

Je kan de marges ook aanpassen door de variable layout='compact' op te geven:

    pandoc --template=template.tex --latex-engine=xelatex --variable layout='compact' -o huisregels.pdf huisregels.md

