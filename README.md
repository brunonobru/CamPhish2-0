Què és CamPhish?
<p>CamPhish són tècniques per fer captures amb la càmera frontal del telèfon d’una víctima o la webcam del seu ordinador. CamPhish allotja una pàgina web falsa en un servidor PHP incorporat i fa servir ngrok i CloudFlare Tunnel per generar un enllaç que reenviarem a la víctima perquè es pugui utilitzar per internet. La pàgina demana permisos per a la càmera i, si la víctima els concedeix, aquesta eina captura les imatges del dispositiu de la víctima.

S’ha afegit una funció de captura de localització GPS.</p>

Característiques
<p>En aquesta eina he afegit dues plantilles de pàgina web automàtiques per captar millor l’atenció de la víctima a la pàgina i obtenir més imatges de la càmera</p> <ul> <li>Desitjos festius</li> <li>Televisió en directe de YouTube</li> <li>Reunió en línia [Beta]</li> <li>Seguiment de localització GPS</li> </ul> <p>S’ha afegit un script de neteja per eliminar tots els fitxers i registres innecessaris.</p>
Aquesta eina provada en:
<ul> <li>Kali Linux</li> <li>Termux</li> <li>MacOS</li> <li>Ubuntu</li> <li>Parrot Sec OS</li> <li>Windows (WSL)</li> </ul>
Instal·lació i requisits
<p>Aquesta eina requereix PHP per al servidor web i wget per descarregar les dependències. Primer executa la següent ordre al terminal</p>
