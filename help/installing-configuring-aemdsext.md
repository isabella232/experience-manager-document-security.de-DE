---
title: Installieren und Konfigurieren von AEM Document Security Extension for Microsoft Office
description: Dieses Dokument erläutert die Installation und Konfiguration von Adobe Experience Manager Document Security Extension 6.2 for Microsoft Office.
uuid: 9d7eb6bb-4780-4d82-8657-7c6c6d523af0
content-type: reference
topic-tags: installing
discoiquuid: f1cdf344-efe4-4cb5-9fc3-47ee4ba5faf4
translation-type: tm+mt
source-git-commit: ac385c538cdd7d3bb4772b92ee7a94b003595f56
workflow-type: tm+mt
source-wordcount: '2796'
ht-degree: 68%

---


# Installieren und Konfigurieren von AEM Document Security Extension for Microsoft Office{#installing-and-configuring-aem-document-security-extension-for-microsoft-office}

Dieses Dokument erläutert die Installation und Konfiguration von Adobe Experience Manager Document Security Extension for Microsoft Office.

Dieses Dokument enthält Informationen zu folgenden Aufgaben:

* Installieren von Document Security Extension for Microsoft Office
* Vorkonfigurieren des Installationsprogramms, um auf das LiveCycle Rights Management ES2 oder höher oder Dokument Security Add-On für AEM 6.0 Forms oder höher zu verweisen.
* Konfigurieren der automatischen Anwendung der Standardrichtlinie

## Vor der Installation {#before-you-install}

Bevor Sie Document Security Extension for Microsoft Office installieren, stellen Sie Folgendes sicher:

* Sie haben die [Versionshinweise](document-security-extension-release-notes.md) gelesen.
* Microsoft Office ist aktiviert. Aktivierungsdialogfeld wird nicht angezeigt beim Öffnen von Microsoft Office-Anwendungen.
* Neueste Service Packs für Microsoft Windows und Microsoft Office sind installiert.
* Wenn Sie Document Security for Microsoft Office für eine nicht unterstützte Sprache installieren, müssen Sie die Office-Anwendung mindestens einmal öffnen.

>[!NOTE]
>
>Installieren Sie die Software nicht in einem Ordner, dessen Name Doppelbyte-Zeichen enthält. Wenn Sie die Software in einem solchen Ordner installieren, wird das AEM Document Security-Menü nicht in Microsoft Office angezeigt.

>[!NOTE]
>
>Die Installation einer 32-Bit-Version Document Security Extension auf einem 64-Bit-Betriebssystem ist unterstützt, aber umgekehrt ist es nicht unterstützt. Sie können die 64-Bit-Version der Document Security Extension for Microsoft Office auf einem 32-Bit-Betriebssystem nicht installieren.

### Deaktivieren Sie McAfee VirusScan&amp; {#disable-mcafee-virusscan}

Wenn Sie außerdem einen reibungslosen Start von Office-Anwendungen auf Computern mit installierter Document Security Extension und aktiviertem McAfee VirusScan mit Überprüfung bei Zugriff sicherstellen möchten, deaktivieren Sie die Option „Pufferüberlaufschutz“ in der Mc Afee VirusScan-Konsole.

### Deinstallieren von Plug-Ins von Drittanbietern {#uninstall-third-party-plug-ins}

AEM Document Security Extension for Microsoft Office unterstützt keine Plug-Ins von Drittanbietern für Microsoft Office-Anwendungen. Da diese Erweiterung mit Plug-Ins von Drittanbietern im Konflikt steht, deinstallieren Sie alle Plug-Ins von Drittanbietern für Microsoft Office, bevor Sie Document Security for Microsoft Office installieren. Adobe unterstützt Document Security for Microsoft Office nicht, wenn Plug-Ins von Drittanbietern installiert sind.

## Systemanforderungen {#system-requirements}

### Dokument Security Extension Client {#document-security-extension-client}

Stellen Sie sicher, dass die folgenden Mindestkonfigurationen für die Installation der Dokument Security Extension verwendet werden:

* 32-Bit- oder 64-Bit-Versionen von Microsoft Windows 7 oder Windows 10 auf Englisch, Französisch, Deutsch, Japanisch, Italienisch, Spanisch, Portugiesisch (Brasilien), Koreanisch oder Chinesisch (vereinfacht und traditionell).
   **Hinweis:***Es wird erwartet, dass Document Security Extension for Microsoft Office auf Microsoft Surface-Geräten funktioniert.*

* 32-Bit- oder 64-Bit-Versionen Microsoft Office 2013, 2016, 2019 und Microsoft Office Desktop-Anwendungen, die als Teil von Office 365 auf Englisch, Französisch, Deutsch, Japanisch, Italienisch, Spanisch, Portugiesisch (Brasilien), Koreanisch oder Chinesisch (vereinfacht und traditionell) installiert sind.

   **Hinweis**: *AEM Document Security Extension for Microsoft Office unterstützt keine Plug-Ins von Drittanbietern für Microsoft Office-Anwendungen. Da Konflikte zwischen Plug-Ins von Drittanbietern und dieser Erweiterung auftreten können, müssen Sie vor der Installation von Document Security Extension for Microsoft Office alle Plug-Ins für Microsoft Office-Anwendungen deinstallieren, die nicht von Adobe stammen. Adobe unterstützt Document Security Extension for Microsoft Office nicht, wenn Plug-Ins von Drittanbietern installiert sind.*

* 1,3-GHz-Prozessor oder höher
* 2 GB RAM
* 100 MB verfügbarer Festplattenspeicher

### Document Security {#document-security}

Um Document Security Extension zu verwenden, stellen Sie sicher, dass Sie eine Verbindung zu Adobe LiveCycle Rights Management ES2 und höher oder Document Security-Add-On für AEM 6.0 Forms oder höher herstellen können.

## Installieren von Document Security Extension for Microsoft Office {#installing-document-security-extension-for-microsoft-office}

Sie können das Installationsprogramm von der [Downloadseite](download-installer.md) herunterladen. Sie können die ausführbare Installationsprogramm-Datei nicht direkt anpassen, allerdings kann sie interaktiv oder im Hintergrund installiert werden. Zur Installation der Software, melden Sie sich bei Windows als Administrator an.

Separate Installationsprogramme sind für 32-Bit- und 64-Bit-Versionen von Microsoft Office verfügbar. Für 32-Bitt-Versionen von Microsoft Office laden Sie DocumentSecurityExtensionforMicrosoftOffice.exe herunter. Eine 64-Bit-Version von Microsoft Office laden Sie DocumentSecurityExtensionforMicrosoftOffice64.exe herunter.

>[!NOTE]
>
>Dieses Dokument verwendet 32-Bit-Installationsdatei (DocumentSecurityExtensionforMicrosoftOffice.exe), um verschiedene Befehle und Optionen zu erklären. Wenn Sie die 64-Bit-Version von Microsoft Office verwenden, verwenden Sie die 64-Bit Installationsdatei (DocumentSecurityExtensionforMicrosoftOffice64.exe), um Vorgänge auszuführen, die in diesem Dokument aufgeführt sind.

### Installation im Hintergrund {#install-in-silent-mode}

Verwenden Sie ein Extrahierungsprogramm wie WinZip, um `DocumentSecurityExtensionforMicrosoftOffice.exe` aus der Installationsdatei zu extrahieren. Öffnen Sie die Eingabeaufforderung, navigieren Sie zum Ordner, der die Setupdatei enthält, und geben Sie den folgenden Text ein:

`DocumentSecurityExtensionforMicrosoftOffice.exe -s -a -s -v" /qn"`

Das Installationsprogramm steht auch als MSI-Datei zur Verfügung, die zur Anpassung verwendet werden kann.

### Installieren einer MSI-Datei im Hintergrund {#install-an-msi-file-in-silent-mode}

1. Verwenden Sie ein Extrahierungsprogramm wie WinZip, um die Datei `DocumentSecurityExtensionforMicrosoftOffice.msi` aus der ZIP-Datei zu extrahieren.

1. Öffnen Sie die Eingabeaufforderung, navigieren Sie zum Ordner, der die MSI-Datei enthält, und geben Sie den folgenden Text ein:

   `msiexec /I DocumentSecurityExtensionforMicrosoftOffice.msi /qn`

## Vorkonfigurieren des Installationsprogramms für die Verbindung mit Dokument Security {#preconfiguring-the-installer-to-connect-to-document-security}

Sie können das Installationsprogramm für Dokument Security Extension for Microsoft Office so konfigurieren, dass es auf einen LiveCycle- oder AEM-Server verweist, damit Benutzer, die Dokument Security Extension for Microsoft Office installieren, diese Funktionen verwenden können, ohne eine Verbindung zu konfigurieren. Daher können Benutzer geschützte Dokumente ohne Konfigurationsanforderung öffnen. Neue Dokumente können jedoch erst geschützt werden, wenn der Client für die Verwendung eines bestimmten Servers konfiguriert wurde.

Im Folgenden werden die Schritte zum Erstellen und Konfigurieren einer MSI-Datei beschrieben. Diese MSI-Datei enthält die Registrierungswerte, die erforderlich sind, um das Installationsprogramm von Dokument Security Extension for Microsoft Office auf dem in Ihrem Unternehmen installierten LiveCycle- oder AEM-Server vorkonfigurieren zu können.

### Voraussetzungen für die Anpassung des Installationsprogramms {#prerequisites-for-customizing-the-installer}

Verwenden Sie den Orca-Datenbank-Editor, um das Installationsprogramm anzupassen. Die folgenden Schritte beschreiben, wie Sie eine benutzerdefinierte MSI-Datei erstellen, indem Sie eine Kopie der MSI-Installationsdatei mit dem Orca-Datenbankeditor bearbeiten. Orca ist als Teil von Windows SDK für Windows Server 2008 und .NET Framework 3.5 verfügbar. Weitere Informationen zur Bearbeitung von Microsoft Windows®-Installationsdateien mithilfe von Orca finden Sie unter [Microsoft Support](http://support.microsoft.com/kb/255905/DE-DE/).

>[!NOTE]
>
>Es wird empfohlen, dass Sie eine vollständige Sicherung aller Installationsdateien durchführen, bevor Sie die benutzerdefinierte MSI-Datei erstellen.

#### Orca {#install-orca} installieren

1. Laden Sie das Windows SDK für Windows Server 2008 und .NET Framework 3.5 vom [Microsoft Download Center](http://www.microsoft.com/download/en/details.aspx?displaylang=en&amp;id=11310) herunter.
1. Klicken Sie bei gedrückter Dublette auf die Datei Orca.msi im Ordner \Microsoft SDK\bin.

   Sie benötigen auch die MSI-Variante der Installationsdatei. Wenden Sie sich an den Support der Adobe, um die neueste Version des MSI-Installationsprogramms zu erhalten.

   >[!NOTE]
   >
   >Schließen Sie immer die Datei &quot;DocumentSecurityExtensionforMicrosoftOffice.msi&quot;, bevor Sie das Installationsprogramm ausführen. Sie können das Installationsprogramm nicht ausführen, wenn Orca die MSI-Datei verwendet.

### Erstellen und konfigurieren Sie die MSI-Datei {#create-and-configure-the-msi-file}

1. Klicken Sie auf **[!UICONTROL Start > Programme > Orca]**.

1. Wählen Sie **[!UICONTROL Datei > Öffnen]** und navigieren Sie dann zur Datei `DocumentSecurityExtensionforMicrosoftOffice.msi`.

1. Wählen Sie die Eigenschaft aus der Tabellenliste (links) aus.

1. Bearbeiten Sie die folgenden Schlüsselnamenwerte, sofern sie auf Ihre Unternehmensinstallation von Rights Management zutreffen oder Document Security.

<table>
 <tbody>
  <tr>
   <td><p><strong></strong><strong></strong><strong>Schlüsselname</strong></p> </td>
   <td><p><strong>Beschreibung</strong></p> </td>
   <td><p><strong>Standardwert </strong><strong></strong><strong>für Schlüsselwert</strong></p> </td>
  </tr>
  <tr>
   <td><p><code>APS_SERVER_NAME</code></p> </td>
   <td><p>Anzeigename.</p> </td>
   <td><p>Standardserver</p> </td>
  </tr>
  <tr>
   <td><p><code>APS_SERVER_URL</code></p> </td>
   <td><p>Host-Server-URL.</p> </td>
   <td><p>https://default.corp.com:1234</p> </td>
  </tr>
 </tbody>
</table>

1. Wählen Sie Registrierung aus der Liste der Tabellen (links).

1. Bearbeiten Sie den folgenden Schlüsselnamenwert.

   | **Schlüsselname** | **Beschreibung** | **Standardwert** |
   |---|---|---|
   | `IsDefault` | Der standardmäßige APS-Server. | Standardserver |

1. Speichern Sie die geänderte Datei in demselben Ordner, der das ursprüngliche MSI-Installationsprogramm enthält.

   >[!NOTE]
   >
   >Üblicherweise wird der gleiche Dateiname wie die ursprüngliche MSI-Datei verwendet (z. B. `DocumentSecurityExtensionforMicrosoftOffice.msi`).

## Konfigurieren der automatischen Anwendung einer Standardrichtlinie {#configuring-automatic-application-of-a-default-policy}

Im Rahmen der Konfiguration können Sie die automatische Anwendung einer Standardrichtlinie so konfigurieren, dass Dokument Security Extension for Microsoft Office jedes gespeicherte Dokument schützt.

Sie können eine der folgenden Optionen angeben:

* Protect alle Dokumente mit einer Standardrichtlinie.
* Benutzer können optional eine Datei in einem ungeschützten Format speichern, wenn sie keine Verbindung zum Server herstellen können. Diese Flexibilität ermöglicht es Ihnen, Fälle zu berücksichtigen, in denen Benutzer Dokumente erstellen, während sie vom Netzwerk getrennt sind (z. B. im Flugzeug).

Nachdem Sie die Funktion &quot;Richtlinie automatisch anwenden&quot;aktiviert haben, wird das Dokument in den folgenden Fällen mit der Standardrichtlinie geschützt:

* Benutzer bearbeitet und speichert ein neu erstelltes Dokument
* Benutzer bearbeitet und speichert ein ungeschütztes Dokument
* Der Benutzer öffnet eine Anwendung, die mit einem Standard-Dokument geöffnet wird, bearbeitet sie und speichert dann das Dokument

### Konfigurieren der Funktion für die automatische Anwendung der Richtlinie in der MSI-Datei  {#configure-the-auto-apply-policy-feature-in-the-msi-file}

Nehmen Sie zuerst eine Vorkonfiguration des Installationsprogramms vor, um auf den LiveCycle- oder AEM Forms-Server zu zeigen (wie zuvor in diesem Artikel beschrieben).

1. Klicken Sie auf **[!UICONTROL Start > Programme > Orca]**.

1. Wählen Sie **[!UICONTROL Datei > Öffnen]** und navigieren Sie dann zur Datei `DocumentSecurityExtensionforMicrosoftOffice.msi`.

1. Wählen Sie die Eigenschaft aus der Tabellenliste (links) aus.

1. Bearbeiten Sie die folgenden Schlüsselnamenwerte, sofern sie auf Ihre Unternehmensinstallation von Rights Management zutreffen oder Document Security.

<table>
 <tbody>
  <tr>
   <td><p><strong>Schlüsselname</strong></p> </td>
   <td><p><strong>Beschreibung</strong></p> </td>
   <td><p><strong>Standardwert </strong><strong></strong><strong>für Schlüsselwert</strong></p> </td>
  </tr>
  <tr>
   <td><p><code>AUTO_APPLY_POLICY_IS_AUTO_ APPLY</code></p> </td>
   <td><p>Aktivieren oder deaktivieren Sie die Funktion zum automatischen Anwenden von Richtlinien.</p> <p><code>1</code>: Aktivieren</p> <p>0: Deaktivieren</p> </td>
   <td><p>0</p> </td>
  </tr>
  <tr>
   <td><p><code>AUTO_APPLY_POLICY_POLICY_I D</code></p> </td>
   <td><p>Die Richtlinien-GUID, die beim Speichern neuer Dokumente verwendet wird. Gilt für die Funktion "Richtlinie automatisch anwenden".</p> </td>
   <td><p>Hexadezimale Richtlinien-ID als auf dem RM-Server sichtbar</p> </td>
  </tr>
  <tr>
   <td><p><code>AUTO_APPLY_POLICY_SERVER_U RL</code></p> </td>
   <td><p>Server-URL.</p> </td>
   <td><p>default.corp.com</p> </td>
  </tr>
  <tr>
   <td><p><code>AUTO_APPLY_POLICY_SERVER_P ORT_NO</code></p> </td>
   <td><p>Server-Anschlussnummer.</p> </td>
   <td><p>1234</p> </td>
  </tr>
  <tr>
   <td><p><code>AUTO_APPLY_POLICY_ALLOW_UN PROTECTED_SAVE</code></p> </td>
   <td><p>Legt fest, ob Dokumente ohne Dokument Security-Schutz erstellt werden können, wenn der Client beim ersten Speichern nicht mit dem Server Kontakt aufnehmen kann, um das Dokument zu schützen.</p> <p>1: Ungeschützte Speicherung zulassen </p> <p>0: Vermeiden Sie die Erstellung neuer Dokumente, wenn der Client zum Speichern des Dokuments nicht mit dem Server in Verbindung treten kann.</p> </td>
   <td><p>0</p> </td>
  </tr>
 </tbody>
</table>

>[!NOTE]
>
>`AUTO_APPLY_POLICY_ALLOW_UN PROTECTED_SAVE` ist nützlich, wenn Sie Kunden daran erinnern möchten, alle Dokumente zu schützen, ohne sie dazu zwingen zu müssen. Dies ist auch hilfreich, wenn Sie sehen, dass Benutzer Dokumente erstellen, wenn keine Verbindung zum Netzwerk besteht. Sie wollen sie nicht daran hindern, Dokumente zu erstellen und zu speichern.

1. Speichern Sie die bearbeitete Datei in demselben Ordner, in dem sich die ursprüngliche MSI-Datei befindet.

   >[!NOTE]
   >
   >Üblicherweise wird der gleiche Dateiname wie die ursprüngliche MSI-Datei verwendet (z. B. `DocumentSecurityExtensionforMicrosoftOffice.msi`).

## Automatischer Schutz neuer Dokumente {#enabling-automatic-protection-of-new-documents}

Der Administrator kann die Möglichkeit zum automatischen Schutz jedes Dokuments aktivieren, das ein Benutzer speichert. Der Administrator konfiguriert die Funktion &quot;Richtlinie automatisch anwenden&quot;im Programm &quot;Dokument Security Extension for Microsoft Office&quot;.

Wenn die Option &quot;Richtlinie automatisch anwenden&quot;aktiviert ist, werden alle vom Benutzer gespeicherten Dokumente mit der Standardrichtlinie geschützt. Dies gilt in folgenden Fällen:

* Wenn ein Benutzer ein neues Dokument erstellt, bearbeitet und speichert es.
* Wenn ein Benutzer ein ungeschütztes Dokument öffnet, bearbeitet und speichert es.

Weitere Informationen zum Konfigurieren der automatischen Anwendung von Richtlinien finden Sie unter[ Konfigurieren der automatischen Anwendung der Standardrichtlinie](installing-configuring-aemdsext.md#p-configuring-automatic-application-of-a-default-policy-p).

## Benutzeroberfläche ohne Menüband aktivieren  {#enable-ribbon-less-user-interface}

Sie können die Benutzeroberfläche ohne Menüband aktivieren/deaktivieren, indem Sie die Einstellungen in der Windows-Registrierung ändern. Führen Sie die folgenden Schritte durch, um die Registrierung zu aktualisieren und die Benutzeroberfläche ohne Menüband zu aktualisieren

1. Machen Sie eine Sicherungskopie von der Windows-Registrierung, bevor Sie daran Änderungen vornehmen. Ausführliche Anweisungen finden Sie unter[ Wie ändere ich die Windows-Registrierung](https://support.microsoft.com/de-de/kb/136393).
1. Navigieren Sie im Registrierungseditor zu diesem Schlüssel: HKEY_CURRENT_USER\Software\Adobe\LiveCycle Rights Management ES4\11.0.0 oder HKEY_LOCAL_MACHINE\Software\Adobe\LiveCycle Rights Management ES4\11.0.0
1. Erstellen Sie einen neuen Dword-Wert (32 Bit) mit dem Namen **HidePluginUI**.

1. Legen Sie den Wert der **HidePluginUI **Eigenschaft auf 1 fest, um die Benutzeroberfläche ohne Menüband zu aktivieren.

1. Schließen Sie den Registrierungseditor.

## Aktivieren des Wasserzeichens zum Drucken in Microsoft Excel  {#enable-watermark-for-printing-in-microsoft-excel}

Sie können die Einstellungen in der Windows-Registrierung ändern, damit ein dynamisches Wasserzeichen gleichzeitig mit vorhandenen Kopf- und Fußzeilen verwendet werden kann. Die Registrierungseinstellungen machen das Wasserzeichen nur während des Druckens verfügbar. Führen Sie die folgenden Schritte durch, um die Registrierung zu aktualisieren und um die Wasserzeichen während des Druckens zu aktivieren.

1. Machen Sie eine Sicherungskopie von der Windows-Registrierung, bevor Sie daran Änderungen vornehmen. Ausführliche Anweisungen finden Sie unter[ Wie ändere ich die Windows-Registrierung](https://support.microsoft.com/en-us/kb/136393).
1. Navigieren Sie im Registrierungseditor zu diesem Schlüssel: HKEY_CURRENT_USER\Software\Adobe\LiveCycle Rights Management ES4\11.0.0 oder HKEY_LOCAL_MACHINE\WOW6432NODE\Software\Adobe\LiveCycle Rights Management ES4\11.0.0
1. Erstellen Sie einen neuen benannten Registrierungswert **WatermarkMode**.
1. Erstellen Sie im WatermarkMode-Registrierungsschlüssel ein DWORD **WatermarkMode** und der Wert der DWORD **WatermarkMode** bis **1.**

1. Schließen Sie den Registrierungseditor.

>[!NOTE]
>
>In Windows Explorer können Sie das Dateimenü oder Kontextmenü verwenden, um ein Microsoft Excel-Dokument zu erstellen. Wenn ein Dokument mit angegebenen Methoden erstellt wurde, kann das Druckdatum nicht abgerufen oder geändert werden. Es handelt sich hier um eine Beschränkung von Microsoft Excel. AEM Document Security-Wasserzeichen hängen von dem Druckdatum des Dokuments ab. Für derartige Dokumente wird das Wasserzeichen auf ein vorheriges Datum zurückgesetzt. Außerdem werden die Kopf- und Fußzeilen nicht beibehalten.

## Eine benutzerdefinierte Titelseite hinzufügen {#coverpage}

Ein Benutzer kann versuchen, das geschützte Dokument auf einem Computer zu öffnen, das keine AEM Document Security for Microsoft Office-Plug-In installiert hat. Derartige Computer können das Dokument nicht öffnen. Auf solchen Computern können Sie eine Titelseite anzeigen, die Anweisungen zum Verwenden von AEM Document Security for Microsoft Office-Plug-In und anderen Informationen enthalten.

### Vor der Konfiguration der Titelseite  {#before-you-configure-a-cover-page}

* Erstellen Sie eine Sicherungskopie der Datei „CommonResources.dll“. Der Standardpfad lautet:

   * **(Für 32-Bit Office auf 32-Bit Computern)** C:\Programme\Adobe\Adobe Experience Manager Forms\Document Security Extension

   * **(Für 32-Bit Office auf 64-Bit Computern)** C:\Programme(x86)\Adobe\Adobe Experience Manager Forms\Document Security Extension

   * **(Für 64-Bit Office auf 64-Bit Computern)** C:\Programme\Adobe\Adobe Experience Manager Forms\Document Security Extension

* Vergewissern Sie sich zunächst, dass Microsoft Visual Studio 2008 oder höher installiert ist. Sie können auch ein anderes Dienstprogramm zum Bearbeiten von DLL-Dateien verwenden.
* Extrahieren Sie das templates.zip-Archiv. Das Archiv enthält folgende Vorlagen für die Titelseite: .xlsx, .docx und .pptx. Verwenden Sie nur bereitgestellte Vorlagen für Dateitypen .xlsx, .docx und .pptx. Sie können auch Ihre eigenen Vorlagen für andere Dateitypen erstellen. Passen Sie Vorlagen an, um benutzerdefinierte Nachrichten und Anweisungen einzubeziehen. Sie finden template.zip unter:

[Datei laden](assets/templates.zip)

### Struktur der Datei „CommonResources.dll“{#structure-of-the-commonresources-dll-file}

Die Datei „CommonResources.dll“ enthält Informationen zu den Ressourcenvorlagen. Sie enthält zwei Namensbezeichner TEMPLATE_FILE und RT_MANIFEST. Um ein benutzerdefiniertes Titelblatt zu aktivieren, wird der TEMPLATE_FILE-Namensbezeichner geändert. Der TEMPLATE_FILE-Namensbezeichner hat sechs Ressourcen.

<table>
 <tbody>
  <tr>
   <td><p><strong>Resource</strong></p> </td>
   <td><p><strong>Repräsentiert </strong></p> </td>
  </tr>
  <tr>
   <td><p>101 </p> </td>
   <td><p>.xls</p> </td>
  </tr>
  <tr>
   <td><p>102</p> </td>
   <td><p>.doc</p> </td>
  </tr>
  <tr>
   <td><p>103 </p> </td>
   <td><p>.ppt</p> </td>
  </tr>
  <tr>
   <td><p>104 </p> </td>
   <td><p>.xlsx</p> </td>
  </tr>
  <tr>
   <td><p>105</p> </td>
   <td><p>.docx</p> </td>
  </tr>
  <tr>
   <td><p>106</p> </td>
   <td><p>.pptx</p> </td>
  </tr>
 </tbody>
</table>

#### Konfigurieren der Vorlage als Titelseite  {#configure-the-template-as-a-cover-page}

1. Microsoft Visual Studio öffnen Öffnen Sie die Datei „CommonResources.dll“, um sie zu bearbeiten.

   >[!NOTE]
   >
   >Wenn die Datei nicht im Solution Explorer-Fenster angezeigt wird, öffnen Sie die Datei mit der Option „Öffnen mit“. Wählen Sie anschließend den Ressourcen-Editor als Editor.

1. Erweitern Sie im Solution Explorer-Fenster, den TEMPLATE_FILE-Ordner und löschen Sie Ressourcen 101.

1. Ressourcen hinzufügen:

   1. Wählen Sie ein Projekt in Solution Explorer im Menü „Projekt“ und klicken Sie auf „Voreinstellungen“.
   1. Wählen Sie die Registerkarte „Ressourcen“.
   1. Zeigen Sie auf der Symbolleiste „Ressource-Designer“ auf „Ressource hinzufügen“ und klicken Sie auf den Pfeil. Wählen Sie als Ressourcentyp TEMPLATE_FILE und klicken Sie auf „Importieren“.
   1. Im Dialogfeld „Vorhandene Datei hinzufügen“ navigieren Sie zur Datei „Resource.xlsx“ und klicken Sie dann auf „Öffnen“. Die Datei wird zum TEMPLATE_FILE-Ordner hinzugefügt.

   >[!NOTE]
   >
   >Überprüfen Sie, ob die Spracheinstellungen richtig sind. Ressource mit neutraler Sprache löschen.

1. Wiederholen Sie die Schritte 2 und 3 für alle Ressourcentypen.

   >[!NOTE]
   >
   >Löschen Sie keine Ressourcentypen oder fügen Sie keine Ressourcentypen hinzu in beliebiger Reihenfolge. Nach 101, konfigurieren Sie 102 usw.

### Verpacken Sie die benutzerdefinierte CommonResources.dll-Datei mit dem Installationsprogramm von AEM Document Security Extension for Microsoft Office  {#package-custom-commonresources-dll-file-with-the-installer-of-aem-document-security-extension-for-microsoft-office}

Sie können die CommonResources.dll-Datei anpassen, um eine benutzerdefinierte Titelseite einzubeziehen. Nach dem Anpassen der Datei können Sie die Originaldatei mit der benutzerdefinierten Datei auf allen Computern manuell ersetzen oder Sie können eine automatische Methode zum Ersetzen der Datei wählen.

In großer Umgebung ist es schwierig und mühsam, die Standarddatei `CommonResources.dll file` manuell durch eine benutzerdefinierte Datei `CommonResources.dll` zu ersetzen. Sie können ein selbstentpackendes und Verpackungswerkzeug verwenden (z. B. WinZip Self-Extractor), um die benutzerdefinierte CommonResources.dll-Datei mit AEM Document Security Extension for Microsoft Office zu verpacken. Später können Sie das benutzerdefinierte Installationsprogramm allen Computern zur Verfügung stellen. Diese Methode reduziert die Zeit, die benötigt wird, um die Standarddatei`CommonResources.dll`   durch eine benutzerdefinierte Datei zu ersetzen. Außerdem wird sichergestellt, dass alle Computer die erforderliche CommonResources.dll-Datei haben. Selbstentpackendes und Verpackungswerkzeug ist nur eine der vielen Möglichkeiten, eine Datei automatisch zu ersetzen. Sie können die Methode wählen, die für Sie und Ihre Umgebung geeignet ist.

Sie können die folgenden Schritte ausführen, um die benutzerdefinierte `CommonResources.dll`-Datei mit dem Installationsprogramm der AEM Document Security Extension for Microsoft Office zu verpacken:

1. Installieren Sie ein selbstentpackendes und Verpackungswerkzeug. Beispielsweise WinZip Self-Extractor.
1. Neuen Ordner erstellen. Beispielsweise YOUR_FOLDER_NAME
1. Platzieren Sie das ursprüngliche Installationsprogramm von AEM Document Security Extension und die benutzerdefinierte CommonResources.dll-Datei in den neu erstellten Ordner.
1. Erstellen einer Batch-Datei im Ordner. Z. B. YOUR_FOLDER_NAME\Installer.bat
1. Öffnen Sie die Batch-Datei zur Bearbeitung und fügen Sie den folgenden Code der Batch-Datei hinzu:

   ```shell
    @echo off
   
    setlocal EnableDelayedExpansion
   
    msiexec /i YOUR_FOLDER_NAME\MSI_NAME.exe
   
   
    FOR /F "tokens=2,*" %%A IN ('REG query "HKLM\HARDWARE\DESCRIPTION\System\CentralProcessor\0" /v "Identifier"') DO set "IDENTIFIER=%%B"
   
    set IDENTIFIER= %IDENTIFIER: =%
   
    if not %IDENTIFIER:x86=%==%IDENTIFIER% (
   
    REM Fetching install path for 32 bit machine.
   
    FOR /F "tokens=2,*" %%A IN ('REG query "HKLM\SOFTWARE\Adobe\LiveCycle Rights Management ES4\11.0.0" /v "InstallPath"') DO set "INSTALLPATH=%%B"
   
    ) else (
   
        REM Fetching install path for 64 bit machine.
   
            FOR /F "tokens=2,*" %%A IN ('REG query "HKLM\SOFTWARE\Wow6432Node\Adobe\LiveCycle Rights Management ES4\11.0.0" /v "InstallPath"') DO set "INSTALLPATH=%%B"
   
        )
   
    COPY "YOUR_FOLDER_NAME\CommonResources.dll" "%INSTALLPATH%"
   
    endlocal
   ```

   Wenn Sie eine andere Version von LiveCycle oder AEM Forms on JEE außer LiveCycle Rights Management ES4 und Version 11.0.0 verwenden, ersetzen Sie den Pfad des Registrierungsschlüssels wie folgt:

   * (LiveCycle Rights Management ES2 und Version 9.0): *HKLM\SOFTWARE\Adobe/LiveCycle* *Rights Management ES2\9.0 *
   * (LiveCycle Rights Management ES3 und Version 10.0)
   * (Livecycle-Rights Management ES4 und Version 11.0) HKLM\SOFTWARE\Adobe\LiveCycle Rights Management ES4\11.0.0
   * (AEM 6.0 Forms on JEE und höher) HKLM\SOFTWARE\Adobe\LiveCycle Rights Management ES4\11.0.0

1. Ersetzen Sie im obigen Code alle Instanzen von YOUR_FOLDER_NAME durch den Namen des Ordners, den Sie in Schritt 2 erstellt haben.
1. **(Für AEM Document Security Extension for Microsoft Office-Installationsprogramme nur mit .exe-Erweiterung)** Ersetzen Sie die folgende Codezeile:

   `msiexec /i YOUR_FOLDER_NAME\MSI_NAME.msi`
durch

   `START /w YOUR_FOLDER_NAME\APPLICATION_NAME.exe`

1. Speichern und schließen Sie die Batch-Datei.
1. Verwenden Sie ein selbstentpackendes und Verpackungswerkzeug, um den Ordner mit der benutzerdefinierten Datei &quot;CommonResources.dll&quot;, dem Originalinstallationsprogramm AEM Dokument Security Extension for Microsoft Office und der Stapeldatei zu verpacken.

   >[!NOTE]
   >
   >Stellen Sie sicher, dass das selbstextrahierende Paket so eingestellt ist, dass es als Administrator ausgeführt wird und automatisch
   >führt die Batch-Datei nach Abschluss der Extraktion aus.

Jetzt komprimiert das selbstentpackende Installationsprogramm der AEM Document Security Extension for Microsoft Office-Pakete die benutzerdefinierte CommonResources.dll-Datei und steht zur Bereitstellung bereit.
