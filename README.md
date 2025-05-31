# 1-Définition
DICOM (Digital Imaging and Communications in Medicine) est un standard international conçu pour l’acquisition, le stockage, la transmission et la visualisation des images médicales et de leurs métadonnées. Il permet l’interopérabilité entre les équipements d’imagerie médicale de différents fabricants, en intégrant dans un même fichier l’image (2D, 3D ou plus) ainsi que des informations essentielles telles que l’identité du patient, les paramètres de l’examen, et les détails techniques de l’acquisition. Utilisé dans les systèmes hospitaliers et les logiciels d’archivage (PACS), DICOM constitue la base de l’imagerie médicale numérique moderne.
Á Quoi sert-il dans l'imagerie médicale ?
En imagerie médicale, DICOM sert à standardiser l’enregistrement, l’échange et la visualisation des images médicales (comme celles issues d’un scanner, d’une IRM ou d’une radiographie) tout en y associant des informations cliniques précises (identité du patient, date, type d’examen, paramètres techniques.
Les principaux avantages de DICOM par rapport à d'autres formats d'images médicales:
• Support des images volumétriques (3D/4D)
• Compatibilité entre machines (scanner, IRM, PACS, logiciels de visualisation)
• DICOM est aussi un protocole de communicationpour échanger les images entre appareils et serveurs PACS.
• Support de l’anonymisation
 
 
# Types de données médicales peuvent être stockés dans un fichier DICOM
 
Un fichier DICOM peut contenir une grande variété de données médicales. Il stocke les images médicales issues de différentes modalités telles que le scanner (CT), l’IRM, la radiographie, l’échographie, la médecine nucléaire ou la mammographie, aussi des données textuelles associées au patient et à l’examen (date, type de modalité, établissement. Il intègre également, comme la résolution, l’épaisseur des coupes, la position du patient et les réglages de l’appareil. En plus des images, un fichier DICOM peut aussi contenir des rapports structurés,(flèches, mesures, commentaires), voire des séquences vidéo ou des séries d’images pour l’imagerie dynamique.
 
Structuration d’un fichier DICOM:
Un fichier DICOM est structuré en deux grandes parties :

# 1. L’en-tête (Header)
L’en-tête contient :128 octets de préambule : ils peuvent être utilisés pour la compatibilité avec d’autres formats (comme les applications multimédia), mais s’ils ne sont pas utilisés, tous les octets doivent être remplis avec la valeur 00H.

4 octets de préfixe "DICM" : ce sont les lettres "DICM" (en majuscules), marquant le début officiel du fichier DICOM.

# 2. L’ensemble de données (Data Set):
Il contient toutes les informations médicales et techniques liées à l’image. Chaque fichier DICOM contient :un seul Data Set représentant une instance d’un objet médical (image, série, etc.)une ou plusieurs images (ex : plusieurs coupes d’un scanner)

Le Data Set est : Codé selon une syntaxe de transfert (Transfer Syntax), précisée dans les métadonnées. Constitué d’éléments appelés Data Elements.

# 3. Les Data Elements

Un Data Element est une unité d’information, identifiée par une étiquette (Tag) unique (comme (0010,0010) pour le nom du patient).

Chaque élément contient :

• un Tag (identifiant),
• une longueur de valeur,
• la valeur elle-même,
• parfois un type de donnée (VR – Value Representation), comme texte, entier, date, etc.
 

Qu'est-ce qu'une "étiquette DICOM" (DICOM Tag) et comment est-elle codée :
est un identifiant unique utilisé pour référencer un élément de données (Data Element) dans un fichier DICOM. Elle permet de stocker et d'organiser les informations spécifiques dans le fichier, comme les données du patient
