---
title: AEM Document Security für Microsoft Office - Versionshinweise
description: Bitte lesen Sie die Versionshinweise, bevor Sie AEM Document Security 6.2 Extension for Microsoft Office installieren.
uuid: f6ab73d4-ac4e-4fff-9bb8-917b75401653
content-type: reference
topic-tags: installing
discoiquuid: c9342c28-8289-4831-a613-4bc03431f557
translation-type: tm+mt
source-git-commit: 403b800eab086d131beb65a496836158778954ee
workflow-type: tm+mt
source-wordcount: '1030'
ht-degree: 81%

---


# AEM Document Security für Microsoft Office - Versionshinweise{#aem-document-security-for-microsoft-office-release-notes}

## Neue Funktionen in AEM Document Security für Microsoft Office {#whats-new-in-aem-document-security-for-microsoft-office}

* **Unterstützung für Office 2019** Document Security Extension for Microsoft Office unterstützt Microsoft Office 2019. Es wird überdies erwartet, dass es mit Microsoft Office 2019 Desktop-Anwendungen als Teil von Office. 365 funktioniert.

>[!NOTE]
>
>Das Dokument verwendet austauschbar Adobe Experience Manager Document Security für Microsoft Office, Adobe Experience Manager Document Security Extension for Microsoft Office und Document Security Extension for Microsoft Office. 

## Installieren und Konfigurieren von AEM Document Security Extension for Microsoft Office {#installing-and-configuring-aem-document-security-extension-for-microsoft-office}

Diese Version von Document Security Extension for Microsoft Office ist mit Adobe mit LiveCycle Rights Management ES2 und höher und Document Security-Add-On für AEM Forms kompatibel.

Prüfen Sie die Informationen in diesem Dokument, bevor Sie AEM Document Security Extension for Microsoft Office installieren. Genauere Installationsanweisungen finden Sie unter [Installieren und Konfigurieren von AEM Document Security Extension for Microsoft Office](installing-configuring-aemdsext.md).

## Behobene Probleme {#fixed-issues}

* Zeichenfolgen werden vertikal angezeigt und dem Inhalt werden falsche Zeilenumbrüche hinzugefügt. (Referenznummer CQ-4201054)

## Bekannte Probleme {#known-issues}

### Plug-Ins von Drittanbietern werden nicht unterstützt.{#third-party-plug-ins-not-supported}

AEM Document Security Extension for Microsoft Office funktioniert nicht mit Plug-Ins von Drittanbietern. Deinstallieren Sie alle Plug-Ins von Drittanbietern für Microsoft Office, bevor Sie Document Security für Microsoft Office installieren.

### Deaktivieren Sie Menüoptionen in Microsoft Word, Excel und PowerPoint {#disabled-menu-options-in-microsoft-word-excel-and-powerpoint}

AEM Document Security Extension for Microsoft Office verwendet integrierte Schutzfunktionen, um Dokumente, Arbeitsmappen und Präsentationen zu schützen. Es werden einige Menüoptionen in Excel, Word und PowerPoint deaktiviert.

### Einschränkungen für Microsoft Excel 2013, 2016 und 2019  {#restrictions-for-microsoft-office}

In Microsoft und sind während einer geschützten Sitzung folgende Optionen nicht verfügbar:

* Microsoft Office 2016 oder Microsoft Office 2019

   * Datei > Speichern unter
   * Datei > Verlauf
   * Datei > Teilen
   * Datei > Export
   * Datei > Veröffentlichen
   * Datei > Konto
   * Datei > Info > Dokument/Arbeitsmappe/Präsentation schützen > Mit Kennwort verschlüsseln
   * Datei > Info > Dokument schützen > Digitale Signatur hinzufügen
   * Datei > Info > Dokument schützen > Als abgeschlossen kennzeichnen
   * Freigabeoption oben rechts

* Microsoft Office 2013

   * Datei > Speichern unter
   * Datei > Teilen
   * Datei > Export
   * Datei > Konto
   * Datei > Info > Dokument/Arbeitsmappe/Präsentation schützen > Mit Kennwort verschlüsseln
   * Datei > Info > Dokument schützen > Digitale Signatur hinzufügen
   * Datei > Info > Dokument schützen > Als abgeschlossen kennzeichnen

### Öffnen eines geschützten Dokuments vom SharePont-Server aus  {#opening-a-protected-document-from-sharepoint-server}

Öffnen des geschützten Dokuments: Wenn Sie versuchen, ein geschütztes Dokument von SharePoint Server aus in Dokument Security Extension for Microsoft Office zu öffnen, ohne das mit dem Dateityp verknüpfte Microsoft Office-Programm wie Microsoft Word, Microsoft Excel oder Microsoft PowerPoint zu öffnen, wird das Dokument möglicherweise nicht geöffnet. Es wird eine Fehlermeldung angezeigt, die angibt, dass Sie das entsprechende Plug-In installieren. Es wird daher empfohlen, das zugehörige Microsoft Office-Programm zu öffnen, bevor Sie ein geschütztes Dokument in Dokument Security Extension for Microsoft Office über SharePoint Server öffnen.

(Optional) Es wird empfohlen, den Cacheordner zu leeren, bevor Sie ein geschütztes Dokument in Dokument Security Extension for Microsoft Office über SharePoint Server öffnen.

Wenn Sie ein geschütztes Dokument über SharePoint Server öffnen, werden alle Berechtigungen für das Dokument deaktiviert, unabhängig von der angewendeten Richtlinie.

### Anwenden von Richtlinien mit dynamischem Wasserzeichen auf Microsoft Excel 2013, Microsoft Excel 2016 und Microsoft Excel 2019-Dateien, wenn kein Drucker installiert ist  {#apply-a-policy-with-a-dynamic-watermark-to-microsoft-excel-microsoft-excel-and-microsoft-excel-file-with-no-printer-installed}

Wenn Sie auf einem Computer, bei dem kein Drucker installiert ist, eine Richtlinie mit dynamischem Wasserzeichen auf eine Excel 2013-, Microsoft Excel 2016- und Microsoft Excel 2019-Datei anwenden und diese Datei speichern, wird folgende Fehlermeldung angezeigt: „Interner Fehler beim Anwenden des dynamischen Wasserzeichens.“ Dieser Fehler wird auch angezeigt, wenn Sie die geschützte Datei erneut öffnen. Das Wasserzeichen wird nicht angewendet und ist unter Ansicht > Seitenlayout nicht sichtbar.

### Deaktivieren Sie Windows Data Execution Prevention für unterstützte Office-Anwendungen  {#disable-windows-data-execution-prevention-for-supported-office-applications}

Es wird empfohlen, dass Sie bei der Verwendung von Microsoft Office -Anwendungen, die von Document Security Extension unterstützt werden, die Windows Data Execution Prevention(DEP)-Einstellungen deaktivieren.

### Freigegebene Microsoft Office-Dateien können nicht mit Document Security Extension geschützt werden {#shared-microsoft-office-files-cannot-be-protected-using-document-security-extension}

Wenn Sie eine freigegebene Microsoft Office-Datei mit Dokument Security Extension schützen, tritt ein Fehler auf und die freigegebene Datei wird nicht gesichert.

### Starten von Office-Anwendungen auf einem Computer, auf dem Dokument Security Extension for Microsoft Office- und McAfee VirusScan installiert ist {#starting-office-applications-on-a-machine-containing-document-security-extension-for-microsoft-office-and-mcafee-virusscan}

Wenn Sie außerdem einen reibungslosen Start von Office-Anwendungen auf Computern mit installierter Document Security und aktiviertem McAfee VirusScan mit Überprüfung bei Zugriff sicherstellen möchten, deaktivieren Sie die Option „Pufferüberlaufschutz“ in der Mc Afee VirusScan-Konsole.

### Installieren von Document Security Extension for Microsoft Office auf einem Computer mit einer nicht unterstützten Microsoft Office-Sprache  {#installing-document-security-extension-for-microsoft-office-on-a-machine-with-an-unsupported-microsoft-office-language}

Bevor Sie Document Security Extension for Microsoft Office auf einem Computer installieren, auf dem eine Microsoft Office-Anwendung mit einer nicht unterstützten Sprache installiert ist, öffnen Sie die Office-Anwendung mindestens einmal.

### Die Schaltfläche „Offline synchronisieren“ ist selbst dann aktiviert, wenn ein Benutzer keine Offline-Berechtigungen hat  {#synchronize-offline-button-is-enabled-even-when-a-user-does-not-have-offline-permissions}

Die Schaltfläche „Offline synchronisieren“ ist verfügbar, obwohl der Benutzer keine Offline-Berechtigung für dieses Dokument hat. Das Klicken auf die Schaltfläche bleibt jedoch wirkungslos.

### Keine Unterstützung für Testversionen von Microsoft Office{#no-support-for-trial-versions-of-microsoft-office} 

AEM Document Security Extension for Microsoft Office unterstützt keine Testversionen von Microsoft Office. Bevor Sie die Erweiterung installieren, stellen Sie sicher, dass Sie eine lizenzierte Kopie von Microsoft Office installiert haben und diese aktiviert ist.

### Geschützte Microsoft Office-Dateien {#unable-to-open-a-protected-microsoft-office-files} können nicht geöffnet werden

Wenn die geschützte Ansicht von Microsoft Office aktiviert ist, kann Rights Management Extension keine geschützten Microsoft Excel-Dateien (XLS, XLSX) und geschützte Microsoft PowerPoint (PPT)-Dateien von einem Remotestandort aus öffnen.

### Zellen des Microsoft Excel-Dokuments, die ein Bild oder eine Hintergrundfarbe enthalten, werden oben auf Wasserzeichen angezeigt {#cells-of-microsoft-excel-document-containing-an-image-or-background-color-appear-on-top-of-watermark}

Wenn eine Zelle eines Microsoft Excel-Dokuments ein Bild enthält oder mit einer Hintergrundfarbe befüllt ist, und eine dynamische Wasserzeichenrichtlinie auf das Dokument angewendet wird, wird das Bild oder die Hintergrundfarbe über dem Wasserzeichen angezeigt und das Wasserzeichen wird davon überdeckt.

### Bedienungsproblem mit mehreren Zertifikaten {#usability-issue-with-multiple-certificates}

Wenn mehrere Zertifikate auf einem Client-Computer vorhanden sind und der Benutzer das Dialogfeld für die Zertifikatauswahl abbricht, wird das Dialogfeld noch einmal angezeigt und der Benutzer muss es zweimal abbrechen.

### Microsoft PowerPoint ermöglicht das Bearbeiten von geschützten Dokumenten  {#microsoft-powerpoint-allows-editing-protected-documents}

Wenn Sie geschützte Dokumente bearbeiten wollen, zeigt Microsoft PowerPoint eine Nachricht an „Sie dürfen dieses Dokument nicht ändern. Sie können die Änderungen nicht speichern.“ Nachdem Sie die Nachricht geschlossen haben, können Benutzer weiterhin Text zum Dokument hinzuzufügen oder es bearbeiten. Die Änderungen am geschützten Dokument werden aber nicht gespeichert.

Das oben erwähnte Verhalten wird in PowerPoint 2013, PowerPoint 2016 und PowerPoint 2019 erwartet.
