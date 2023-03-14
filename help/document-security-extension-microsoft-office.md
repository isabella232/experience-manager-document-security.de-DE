---
title: Einführung in AEM Document Security Extension für Microsoft&reg; Office
description: Verwenden der Document Security-Erweiterung für Microsoft&reg; Office können Sie vordefinierte Vertraulichkeitseinstellungen auf Ihre Microsoft&reg anwenden. Office-Dateien.
uuid: a5428c50-fae3-4823-9e6f-0f5306e7248f
content-type: reference
topic-tags: using
discoiquuid: cf93f9f5-1fb6-4909-815e-0ffb8c6ea6d1
exl-id: 3e07c031-3f88-4bde-bdb3-b136ef5f9527
source-git-commit: f3456fa7243405a4986ac50540f8b578a6412a6c
workflow-type: tm+mt
source-wordcount: '1313'
ht-degree: 67%

---

# Einführung in AEM Document Security Extension für Microsoft® Office{#introduction-to-aem-document-security-extension-for-microsoft-office}

Adobe® Experience Manager Document Security Extension for Microsoft® Office stellt sicher, dass nur von Ihnen autorisierte Benutzer mit Word-, Excel- und PowerPoint-Dateien arbeiten dürfen, die Ihr geistiges Eigentum enthalten. Durch die Verwendung von Document Security Extension for Microsoft® Office können Sie vordefinierte Vertraulichkeitseinstellungen auf Ihre Dateien anwenden.

Document Security Extension for Microsoft® Office erweitert das LiveCycle Rights Management- und Document Security-Add-On für Adobe Experience Manager Forms, um Word-, Excel- und PowerPoint-Dateien zu schützen und autorisierten Benutzern, die diese Software installiert haben, die Verwendung richtliniengeschützter Dateien gemäß den in der Richtlinie festgelegten Vertraulichkeitseinstellungen zu ermöglichen.

## Schutz von geistigem Eigentum mit Document Security {#how-document-security-protects-intellectual-property}

Document Security stellt sicher, dass nur die von Ihnen autorisierten Personen Dateien verwenden können, die Ihr geistiges Eigentum enthalten. Mit Document Security können Sie Dateien mithilfe von Vertraulichkeitsrichtlinien schützen. Eine *Richtlinie* ist eine Zusammenstellung von Informationen, die unter anderem Vertraulichkeitseinstellungen und eine Liste berechtigter Benutzer umfasst. Die Einstellungen, die Sie in einer Richtlinie angeben, bestimmen, wie ein Empfänger eine Datei nutzen darf, auf die Sie die Richtlinie anwenden. Sie können beispielsweise angeben, ob Empfänger Text drucken oder kopieren oder Änderungen speichern können.

Document Security-Administratoren und -Benutzer erstellen Richtlinien. Administratoren erstellen Organisationsrichtlinien, die allen autorisierten Benutzern zur Verfügung stehen. Administratoren oder Richtliniensatzkoordinatoren können auch Gruppen von Richtlinien mit der Bezeichnung *Richtliniensätze* erstellen, die einer Untergruppe von Benutzern zur Verfügung stehen. Benutzer können eigene Richtlinien erstellen, die nur sie verwenden können. Administratoren, Richtliniensatzkoordinatoren und Benutzer erstellen Richtlinien auf den Document Security-Web-Seiten.

Die Richtlinien sind zwar in Document Security gespeichert, Sie wenden sie aber über Word, Excel oder PowerPoint auf Dateien an. Wenn Sie eine Richtlinie auf eine Datei anwenden, werden die in der Datei enthaltenen Informationen durch die in der Richtlinie angegebenen Vertraulichkeitseinstellungen geschützt. Wenn Sie die richtliniengeschützte Datei verteilen, können nur die von der Richtlinie autorisierten Empfänger auf den Inhalt der Datei zugreifen.

Durch das Schützen einer Datei` mit einer Richtlinie behalten Sie die Kontrolle über die Datei, auch nachdem sie verteilt wurde. Sie können Ereignisse überprüfen, um zu verfolgen, wann und wie Empfänger Ihre Datei verwenden, Änderungen an der Richtlinie vornehmen, Benutzer am weiteren Zugriff auf die Datei hindern und die mit der Datei verbundene Richtlinie ändern.

## Funktionsweise von Richtlinien {#how-policies-work}

Richtlinien enthalten Informationen zu den autorisierten Benutzern und den Vertraulichkeitseinstellungen, die für geistiges Eigentum gelten. Benutzer können alle Benutzer sein, die von Document Security durch Aufnahme in eine verknüpfte LDAP- oder Active Directory-Liste erkannt werden. Benutzer können auch Personen sein, die zur Registrierung bei Document Security eingeladen wurden oder für die der Administrator ein Konto erstellt hat.

Die Vertraulichkeitseinstellungen in einer Richtlinie bestimmen, wie die Empfänger Dateien verwenden können, die durch die Richtlinie geschützt sind. Richtlinien geben beispielsweise an, ob Empfänger Dateien drucken, Inhalte in andere Dateien kopieren oder Änderungen an geschützten Dateien speichern können. Richtlinien können auch unterschiedliche Vertraulichkeitseinstellungen für verschiedene Benutzer festlegen.

Wenn Sie eine Richtlinie auf eine Datei anwenden, werden die in der Datei enthaltenen Informationen durch die in der Richtlinie angegebenen Vertraulichkeitseinstellungen geschützt. Wenn Sie die Datei verteilen, authentifiziert Document Security die Empfänger, die versuchen, die Datei zu öffnen, und autorisiert den Zugriff entsprechend den in der Richtlinie festgelegten Berechtigungen.

Nachdem eine Richtlinie auf eine Datei angewendet wurde, können die Vertraulichkeitseinstellungen der Richtlinie jederzeit geändert werden. Auf diese Weise können Sie autorisierte Benutzer hinzufügen oder entfernen oder die Berechtigungen für Benutzer ändern, nachdem sie die Datei erhalten haben. Die auf die Datei angewendete Richtlinie kann geändert werden, und der Zugriff auf die Datei kann gesperrt werden, damit sie nicht mehr von jedem geöffnet werden kann, der über eine Kopie der Datei verfügt.

Wenn die Richtlinie den Offline-Zugriff zulässt, können die Empfänger richtliniengeschützte Dateien auch offline (ohne aktive Internet- oder Netzwerkverbindung) für den in der Richtlinie angegebenen Zeitraum verwenden.

## Funktionsweise richtliniengeschützter Dateien {#how-policy-protected-files-work}

Damit ein Benutzer richtliniengeschützte Word-, Excel- und PowerPoint-Dateien öffnen und verwenden kann, muss die Richtlinie den Benutzer als Empfänger enthalten oder anonymen Zugriff zulassen. Außerdem muss Document Security Extension for Microsoft® Office installiert sein. Um eine richtliniengeschützte Datei jemandem zur Verfügung zu stellen, der nicht über Document Security Extension for Microsoft® Office verfügt, geben Sie ihm entweder eine Kopie der Software oder teilen Sie ihm mit, wie Sie sie von Ihrer Website herunterladen können. Wenn Sie das Installationsprogramm nicht haben, können Sie es von der [Download-Seite](https://experienceleague.adobe.com/docs/experience-manager-document-security/using/download-installer.html?lang=en) herunterladen.

Wenn ein Benutzer versucht, eine richtliniengeschützte Datei zu öffnen, stellt Document Security Extension for Microsoft® Office eine Verbindung zu Document Security her, um den Benutzer zu authentifizieren. Wenn Document Security für die Prüfung der Dateinutzung konfiguriert ist, wird dem Benutzer eine Benachrichtigung angezeigt, dass die Dateinutzung geprüft wird. Document Security bestimmt, welche Dateiberechtigungen dem Benutzer gewährt werden sollen, und der Benutzer kann dann die Datei gemäß den Richtlinieneinstellungen unter diesen Bedingungen verwenden:

* Für die in der Richtlinie angegebene Gültigkeitsdauer.
* Bis ein Administrator oder die Person, die die Richtlinie angewendet hat, entweder den Zugriff auf die Datei widerruft oder die Richtlinie ändert.

   Wenn die Person, die die Richtlinie angewendet hat, die Richtlinie ändert oder den Zugriff auf die Datei widerruft, werden die Berechtigungen des Benutzers für die Datei geändert oder entfernt, auch wenn der Benutzer bereits über die Datei verfügt. Wenn die Datei selbst widerrufen wurde, kann dem Benutzer eine URL zur Verfügung gestellt werden, um eine aktualisierte Kopie zu erhalten.

   Richtliniengeschützte Dateien können während der in der Richtlinie angegebenen Offline-Nutzungsdauer offline geöffnet werden (ohne Internet- oder Netzwerkverbindung), wenn die Richtlinie den Offline-Zugriff zulässt. Wenn die Offline-Nutzungsdauer endet, muss der Benutzer online gehen und mit Document Security synchronisieren, wodurch eine neue Nutzungsdauer beginnt.

   Wenn die Richtlinie das Speichern der Datei zulässt und ein Benutzer eine Kopie der richtliniengeschützten Datei speichert, wird die Richtlinie automatisch für die gespeicherte Datei angewendet und durchgesetzt. Ereignisse, wie z. B. Versuche, die neue Datei zu öffnen, werden ebenfalls geprüft und aufgezeichnet, genau wie bei der Originaldatei.

## Verwendung von Document Security zum Schutz Ihrer Dateien {#using-document-security-to-protect-your-files}

Sie können Richtlinien verwenden, um Ihre Dateien in verschiedenen Situationen zu schützen.

Beispielsweise akzeptiert ein Hersteller Angebote von Anbietern, die Teile für ein neues Produkt bereitstellen. Der Hersteller muss den Bietern proprietäre Informationen zur Verfügung stellen, um ihre Einreichungen abzuschließen. Der Hersteller verwendet Document Security zum Schutz der Dateien mit einer Richtlinie, die es den Bietern erlaubt, die Dateien zu öffnen und die Informationen anzuzeigen. Die Bieter werden jedoch daran gehindert, die Dateien zu ändern, zu drucken oder zu kopieren, und alle, die keine Berechtigung haben, werden daran gehindert, die Dateien zu öffnen.

Nachdem er eines der Angebote akzeptiert hat, aktualisiert der Hersteller die Richtlinie, um dem erfolgreichen Bieter die Berechtigung zum Drucken, Kopieren und lokalen Speichern von Änderungen zu erteilen und die nicht erfolgreichen Bieter zu entfernen, sodass sie keine Berechtigung mehr zum Öffnen der Dateien haben.

Bei der Arbeit mit dem erfolgreichen Bieter ändern die Ingenieure des Herstellers einige der Designspezifikationen in den Dateien. Um die neuen Spezifikationen zu veröffentlichen, entzieht der Hersteller den Zugriff auf einige der Dateien und veröffentlicht neue Versionen. Wenn die Ingenieure des erfolgreichen Bieters versuchen, die Datei zu öffnen, sehen sie eine Meldung, dass der Zugriff auf die Datei widerrufen wurde. Die Meldung enthält eine URL, unter der sie eine neue Version der Datei herunterladen können.

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
   <td><p><a href="https://experienceleague.adobe.com/docs/experience-manager-65/forms/administrator-help/get-started/configure-general-aem-forms-settings.html?lang=en">Administrator-Hilfe</a> oder klicken Sie auf den Administrationsseiten von Document Security in der rechten oberen Ecke auf den Hilfelink.</p> </td>
  </tr>
  <tr>
   <td><p>Patchaktualisierungen, technische Hinweise und weitere Informationen zu dieser Produktversion</p> </td>
   <td><p><a href="https://experienceleague.adobe.com/?support-solution=General&amp;support-tab=home#support">Technischer Support für Experience Cloud</a></p> </td>
  </tr>
 </tbody>
</table>
