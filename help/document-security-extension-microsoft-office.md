---
title: Einführung in AEM Document Security Extension for Microsoft Office
description: Mit Hilfe von Document Security Extension for Microsoft Office können Sie vordefinierte Vertraulichkeitseinstellungen auf Ihre Dateien anwenden.
uuid: a5428c50-fae3-4823-9e6f-0f5306e7248f
content-type: reference
topic-tags: using
discoiquuid: cf93f9f5-1fb6-4909-815e-0ffb8c6ea6d1
translation-type: tm+mt
source-git-commit: 19de0b62ac493c7507581abb607b008c64f77597
workflow-type: tm+mt
source-wordcount: '1304'
ht-degree: 24%

---


# Einführung in AEM Document Security Extension for Microsoft Office{#introduction-to-aem-document-security-extension-for-microsoft-office}

Adobe® Experience Manager Document Security Extension for Microsoft® Office stellt sicher, dass nur von Ihnen autorisierte Benutzer mit Word-, Excel- und PowerPoint-Dateien arbeiten dürfen, die Ihr geistiges Eigentum enthalten. Durch den Einsatz von Document Security Extension for Microsoft Office können Sie vordefinierte Vertraulichkeitseinstellungen auf Ihre Dateien anwenden.

Document Security Extension for Microsoft Office erweitert LiveCycle Rights Management und Document Security Add-On für Adobe Experience Manager Forms, um Word-, Excel- und PowerPoint-Dateien zu schützen und autorisierten Benutzern, die diese Software installiert haben, die Nutzung richtliniengeschützter Dateien gemäß den in der Richtlinie angegebenen Vertraulichkeitseinstellungen zu ermöglichen.

## So schützt Dokument Security geistiges Eigentum {#how-document-security-protects-intellectual-property}

Dokument Security stellt sicher, dass nur die von Ihnen autorisierten Personen Dateien verwenden können, die Ihr geistiges Eigentum enthalten. Mit Dokument Security können Sie Dateien mithilfe von Vertraulichkeitsrichtlinien schützen. Eine *Richtlinie* ist eine Zusammenstellung von Informationen, die unter anderem Vertraulichkeitseinstellungen und eine Liste berechtigter Benutzer umfasst. Die von Ihnen in einer Richtlinie festgelegten Einstellungen bestimmen, wie ein Empfänger eine Datei verwenden kann, auf die Sie die Richtlinie anwenden. Sie können beispielsweise angeben, ob Empfänger Text drucken, kopieren oder speichern können.

Dokument Security-Administratoren und -Benutzer erstellen Richtlinien. Administratoren erstellen Organisationsrichtlinien, die allen autorisierten Benutzern zur Verfügung stehen. Administratoren oder Richtliniensatzkoordinatoren können auch Gruppen von Richtlinien mit der Bezeichnung *Richtliniensätze* erstellen, die einer Untergruppe von Benutzern zur Verfügung stehen. Benutzer können eigene Richtlinien erstellen, die nur sie verwenden können. Administratoren, Richtliniensatzkoordinatoren und Benutzer erstellen Richtlinien auf den Dokument Security-Webseiten.

Richtlinien werden zwar unter Dokument Security gespeichert, Sie wenden sie jedoch über Word, Excel oder PowerPoint auf Dateien an. Wenn Sie eine Richtlinie auf eine Datei anwenden, werden die in der Datei enthaltenen Informationen durch die in der Richtlinie angegebenen Vertraulichkeitseinstellungen geschützt. Wenn Sie die richtliniengeschützte Datei verteilen, können nur die von der Richtlinie autorisierten Empfänger auf den Dateiinhalt zugreifen.

Durch die Verwendung einer Richtlinie zum Schutz einer Datei behalten Sie die Kontrolle über diese Datei, auch nachdem sie verteilt wurde. Sie können Ereignisse prüfen, um zu verfolgen, wann und wie Empfänger Ihre Datei verwenden, Änderungen an der Richtlinie vorzunehmen, zu verhindern, dass Benutzer weiterhin auf die Datei zugreifen können, und die Richtlinie zu ändern, die an die Datei angehängt wird.

## Funktionsweise von Richtlinien {#how-policies-work}

Richtlinien enthalten Informationen zu den autorisierten Benutzern und den Vertraulichkeitseinstellungen, die für geistiges Eigentum gelten. Benutzer können alle Benutzer sein, die von Dokument Security durch Aufnahme in eine verknüpfte LDAP- oder Active Directory-Liste erkannt werden. Benutzer können auch Personen sein, die zur Registrierung bei Dokument Security eingeladen wurden oder für die der Administrator ein Konto erstellt hat.

Die Vertraulichkeitseinstellungen in einer Richtlinie bestimmen, wie die Empfänger Dateien verwenden können, die durch die Richtlinie geschützt sind. Richtlinien geben beispielsweise an, ob Empfänger Dateien drucken, Inhalte in andere Dateien kopieren oder Änderungen an geschützten Dateien speichern können. Richtlinien können auch unterschiedliche Vertraulichkeitseinstellungen für verschiedene Benutzer angeben.

Wenn Sie eine Richtlinie auf eine Datei anwenden, werden die in der Datei enthaltenen Informationen durch die in der Richtlinie angegebenen Vertraulichkeitseinstellungen geschützt. Wenn Sie die Datei verteilen, authentifiziert Dokument Security die Empfänger, die versuchen, die Datei zu öffnen, und autorisiert den Zugriff gemäß den in der Richtlinie angegebenen Berechtigungen.

Nachdem eine Richtlinie auf eine Datei angewendet wurde, können die Vertraulichkeitseinstellungen der Richtlinie jederzeit geändert werden, sodass Sie autorisierte Benutzer hinzufügen oder entfernen oder die Berechtigungen für Benutzer ändern können, nachdem diese die Datei erhalten haben. Die auf die Datei angewendete Richtlinie kann geändert werden, und der Zugriff auf die Datei kann gesperrt werden, damit sie nicht mehr von jedem geöffnet werden kann, der über eine Kopie der Datei verfügt.

Wenn die Richtlinie den Offline-Zugriff zulässt, können Empfänger für den in der Richtlinie angegebenen Zeitraum auch offline (ohne aktive Internet- oder Netzwerkverbindung) richtliniengeschützte Dateien verwenden.

## Funktionsweise richtliniengeschützter Dateien  {#how-policy-protected-files-work}

Damit ein Benutzer richtliniengeschützte Word-, Excel- und PowerPoint-Dateien öffnen kann, muss dieser Benutzer entweder in der Richtlinie als Empfänger enthalten sein oder anonymer Zugriff muss zugelassen sein. Außerdem muss auf dem Computer des Benutzers Document Security Extension for Microsoft Office installiert sein. Um eine richtliniengeschützte Datei jemandem zur Verfügung zu stellen, der Document Security Extension for Microsoft Office nicht hat, geben Sie demjenigen entweder die Software oder teilen Sie ihm mit, wie diese von Ihrer Website heruntergeladen werden kann. Wenn Sie das Installationsprogramm nicht haben, können Sie es von der [Downloadseite](https://www.adobe.com/de/products/livecycle/rightsmanagement/extension/downloads.html) herunterladen.

Wenn ein Benutzer versucht, eine richtliniengeschützte Datei zu öffnen, stellt Dokument Security Extension for Microsoft Office eine Verbindung zu Dokument Security her, um den Benutzer zu authentifizieren. Wenn Dokument Security für die Prüfung der Dateinutzung konfiguriert ist, wird dem Benutzer eine Benachrichtigung angezeigt, dass die Dateiverwendung geprüft wird. Dokument Security legt fest, welche Dateiberechtigungen dem Benutzer erteilt werden sollen und der Benutzer die Datei dann gemäß den Richtlinieneinstellungen unter folgenden Bedingungen verwenden kann:

* Für die in der Richtlinie angegebene Gültigkeitsdauer.
* Bis ein Administrator oder die Person, die die Richtlinie angewendet hat, entweder den Zugriff auf die Datei widerruft oder die Richtlinie ändert.

   Wenn die Person, die die Richtlinie angewendet hat, die Richtlinie ändert oder den Zugriff auf die Datei sperrt, werden die Berechtigungen des Benutzers für die Datei geändert oder entfernt, auch wenn der Benutzer bereits über die Datei verfügt. Wenn die Datei selbst gesperrt wurde, kann dem Benutzer eine URL zur Verfügung gestellt werden, um eine aktualisierte Kopie zu erhalten.

   Richtliniengeschützte Dateien können offline (ohne Internet- oder Netzwerkverbindung) geöffnet werden, wenn die Richtlinie den Offline-Zugriff zulässt, während der in der Richtlinie angegebenen Offline-Nutzungsdauer. Nach Ablauf der Offline-Nutzungsdauer muss der Benutzer online gehen und mit Dokument Security synchronisieren, das eine neue Nutzungsdauer Beginn.

   Wenn die Richtlinie das Speichern der Datei zulässt und ein Benutzer eine Kopie der richtliniengeschützten Datei speichert, wird die Richtlinie automatisch angewendet und für die gespeicherte Datei erzwungen. Ereignis wie Versuche, die neue Datei zu öffnen, werden ebenso geprüft und aufgezeichnet wie die Originaldatei.

## Verwenden von Dokument Security zum Schutz Ihrer Dateien {#using-document-security-to-protect-your-files}

Sie können Richtlinien verwenden, um Ihre Dateien in verschiedenen Situationen zu schützen.

Ein Hersteller akzeptiert beispielsweise Angebote von Anbietern, die Teile für ein neues Produkt bereitstellen. Der Hersteller muss den Bietern die für den Abschluss der Einreichung erforderlichen Angaben zur Verfügung stellen. Der Hersteller verwendet Dokument Security, um die Dateien mit einer Richtlinie zu schützen, die es den Bietern ermöglicht, die Dateien zu öffnen und die Informationen zu Ansicht. Bieter können die Dateien jedoch nicht ändern, drucken oder kopieren, und jeder, der keine Berechtigung hat, kann die Dateien nicht öffnen.

Nach der Annahme eines der Angebote aktualisiert der Hersteller die Richtlinie, um dem erfolgreichen Bieter Berechtigungen zum Drucken, Kopieren und Speichern von Änderungen zu erteilen und die nicht erfolgreichen Bieter zu entfernen, sodass sie nicht mehr berechtigt sind, die Dateien zu öffnen.

Beim Arbeiten mit dem erfolgreichen Bieter ändern die Ingenieure des Herstellers einige der Designspezifikationen in den Dateien. Um die neuen Spezifikationen zu veröffentlichen, widerruft der Hersteller den Zugriff auf einige der Dateien und veröffentlicht neue Versionen. Wenn Ingenieure für den erfolgreichen Bieter versuchen, die Datei zu öffnen, wird ihnen eine Meldung angezeigt, dass der Zugriff auf die Datei widerrufen wurde. Die Nachricht enthält eine URL, über die sie eine neue Version der Datei herunterladen können.

## Zusätzliche Informationen {#additional-information}

In den Ressourcen in dieser Tabelle finden Sie Informationen zu AEM Dokument Security:

<table >
 <tbody>
  <tr>
   <th><p>Informationen</p> </th>
   <th><p>Siehe</p> </th>
  </tr>
  <tr>
   <td><p>AEM Forms-Administrator-Hilfe</p> </td>
   <td><p><a href="http://www.adobe.com/go/learn_aemforms_admin_65_de">Administrator-Hilfe</a> oder klicken Sie auf den Administrationsseiten von Document Security in der rechten oberen Ecke auf den Hilfelink.</p> </td>
  </tr>
  <tr>
   <td><p>Patchaktualisierungen, technische Hinweise und weitere Informationen zu dieser Produktversion</p> </td>
   <td><p><a href="https://helpx.adobe.com/de/marketing-cloud/contact-support.html">Technische Unterstützung für Marketing Cloud</a></p> </td>
  </tr>
 </tbody>
</table>

