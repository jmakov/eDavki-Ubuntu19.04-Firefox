# Navodila za delovanje podpisne komponente na Ubuntu 19.04 z brskalnikom Firefox
#### Opombe: Podpisna komponenta deluje samo z Oracle Java 8.

Navodila za namestitev:
1. pojdi na https://www.java.com/en/download/linux_manual.jsp
2. s klikom na "Linux x64" prenesi datoteko
3. odpri terminal kamor si prenesel datoteko 
4. naslednji ukazi odpakirajo prenešeno datoteko in jo namestijo v sistem
    ```
    tar -xvf jdk-8*
    sudo mkdir /usr/lib/jvm
    sudo mv ./jdk1.8* /usr/lib/jvm/oracle_jdk1.8
    sudo update-alternatives --install "/usr/bin/java" "java" "/usr/lib/jvm/oracle_jdk1.8/bin/java" 1
    sudo update-alternatives --install "/usr/bin/javaws" "javaws" "/usr/lib/jvm/oracle_jdk1.8/bin/javaws" 1
    sudo chmod a+x /usr/bin/java
    sudo chmod a+x /usr/bin/javac
    sudo chmod a+x /usr/bin/javaws
    ```
5. zapri in ponovno odpri Firefox
6. preveri uspešnost namestitve z obiskom strani https://edavki.durs.si/EdavkiPortal/OpenPortal/CommonPages/Sign/IESign.aspx?id=test
