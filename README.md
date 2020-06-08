# git-auchan
Git course for Auchan employees.

## Git Config
- `git config --list` beállítások listázása.

## Git Revert
### Önálló feladatok 
* Hozz létre a Github rendszerében egy új tárolót 'git-course' néven.  
Inicializáld a Readme.md fájlt, hogy ne kelljen kézzel létrehozni.  
* Klónozd a saját gépedre a tárolót.
* Módosítsd a Readme.md fájlt és kommitold a módosításokat.
* Vond vissz a módosítást a revert parancs használatával.

## Git Reset
### Önálló feladatok  
* Az előzőhöz hasonlóan módosítsd a Readme.md fájlt ízlés szerint.
* Add hozzá a stage -hez és kommitold a módosításodat.
* A log segítségével keresd meg az utolsó előtti állapotot és állj vissza  
rá a reset paranccsal.  

## Git Log
### Önálló feladatok  
* Keresd meg a mai napon létrejött commit -ok közül azokat, amelyek fájlokat 
módosítottak és listázd ki őket a log paranccsal.  

## Git Diff
### Önálló feladatok

-   Módosítsd a Readme.md fájlt, majd ellenőrizd az eltéréseket a VSCode
    beépített diff tool -jának a segítségével.
-   Commitold és push -old a módosításokat, majd ellenőrizd ismét a
    diff tool -t.

## Git Status
### Önálló feladatok  
* Kérd le a projekted státuszát v2 -es kimeneti formátumban.  

## Git Grep
### Önálló feladatok
* A tanultak alapján keressünk rá egy sorra a Readme.md fájlban.  

## Git Branch
### Önálló feladatok
* Készíts egy develop branch -et, majd állj rá a VSCode -ban.  
* Hajts végre módosításokat a fájlokon és commitold, pushold őket.  

## Git Merge
### Önálló feladatok
* Az előzőleg létrehozott branch pillanatnyi állapotát merge -eld vissza a 
master branch -be.

## Git Conflict
> Már volt szó a pull, és a fetch műveletről. Tudjuk, hogy a kettő között a 
különbség „csak” annyi, hogy a pull automatikusan elvégzi a merge műveletet is.  
  
### Egy tanulságos történet  
> Amikor egy remote szerveren lévő változásokat pull-ozom, vagy branch-eket 
olvasztok össze, conflict keletkezhet. Ez abban az esetben történhet, ha egy 
file ugyanazon sorát többen szerkesztették, azaz két különböző commit a 
file ugyanazon sorának módosítását tárolja. 
  
> __Például:__ két fejlesztő ugyanazon a development branchen fejleszt, 
és az index.html 1. sorát mindketten módosítják.
  
> Az első fejlesztő ezt írj az első sorba:  
``` html
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
```  
  
> A másikuk viszont ezt:  
``` html
<!DOCTYPE html>
```  
  
> Mindketten elmentik a file-t. Mindketten commitolnak, majd az első fejlesztő 
felpusholja a változtatások, majd amikor a második fejlesztő fel akarja pusholni 
a saját változtatásait akkor kap egy figyelmeztetést, hogy először pullozza 
le a szerveren lévő változásokat.  
  
> Elvégzi a pull műveletet. Ilyenkor kapja meg a conflict részleteit. A git nem 
tudja eldönteni, hogy melyik verzió a helyes. Ilyenkor manuálisan kell 
feloldanunk a conflit-ot. Ekkor három lehetőségünk van: 
* A pullozott verziót tartjuk meg
* A saját verziót tartjuk meg
* Összefésüljük a kettőt, és akár mindegyik kódsort megtarthatjuk.  
  
> Ezért is érdemes push előtt mindig pull-ozni, vagy először csak fetch-elni.
  
### Konklúzió  
> Tehát a következő legyen a sorrend:
* add – commit – pull (feloldás, commitolás ha kell) – push
  
> Vagy a másik megoldás:
stash -pull - stash apply- add -commit -push
  
> __Mindig nézzünk status-t.__  
  
----------

### Önálló feladatok
* Idézz elő a fent leírt módon egy conflict -ot és oldd fel tetszés szerint.
## Teszt DA 
- tezstelem a git status parancsot 
- teszt a commit parancsra
- teszt git add .
- teszt git push 
