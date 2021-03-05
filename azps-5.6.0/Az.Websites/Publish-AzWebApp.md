---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/publish-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Publish-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Publish-AzWebApp.md
ms.openlocfilehash: 726f991f5e51b6196b61a6e977ba1c5d4a1debf0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014458"
---
# Publish-AzWebApp

## SYNOPSIS
Wdraża aplikację Azure Web App z pliku ZIP, JAR lub WAR przy użyciu pliku zipdeploy. 

## SKŁADNIA

### FromResourceName
```
Publish-AzWebApp -ArchivePath <String> [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>]  [-Force] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### FromWebApp
```
Publish-AzWebApp -ArchivePath <String> [-AsJob] [-WebApp] <PSSite> [-Force] [-DefaultProfile <IAzureContextContainer>] 
 [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Publish-AzWebApp** umożliwia przekazywanie zawartości do istniejącej aplikacji Azure Web App. Zawartość powinna zostać spakowana do pliku ZIP, jeśli używasz stosów, takich jak .NET, Python, Node lub PLIK WAR lub JAR, jeśli używasz języka Java. Zawartość powinna być wstępnie wbudowana i gotowa do użycia bez dodatkowych kroków kompilacji podczas wdrażania. To polecenie cmdlet używa funkcji zipdeploy i wardeploy kudu do wdrażania zawartości. Aby uzyskać szczegółowe informacje o tym, jak działają aplikacje zipdeploy i wardeploy oraz jak poprawnie spakuj aplikację sieci Web do wdrożenia, zapoznaj się z witryną typu wiki kudu. https://aka.ms/kuduzipdeploy i https://aka.ms/kuduwardeploy zawierają pomocne informacje na temat zipdeploy i wardeploy.

## PRZYKŁADY

### Przykład 1
```powershell
PS C:\> Publish-AzWebApp -ResourceGroupName Default-Web-WestUS -Name MyApp -ArchivePath C:\project\app.zip
```

Przekazanie zawartości pliku app.zip do aplikacji sieci Web o nazwie MyApp należącej do grupy zasobów Default-Web-WestUS.

### Przykład 2
```powershell
PS C:\> Publish-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp -Slot Staging -ArchivePath C:\project\javaproject.war
```

Przekazanie zawartości pliku javaproject.war do miejsca tymczasowego aplikacji sieci Web o nazwie ContosoApp należącej do grupy zasobów ContosoRG.

### Przykład 3
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> Publish-AzWebApp -WebApp $app -ArchivePath C:\project\app.zip -AsJob
```

Przekazanie zawartości pliku app.zip do aplikacji sieci Web o nazwie ContosoApp należącej do grupy zasobów ContosoRG. Polecenie cmdlet zostanie uruchomione w zadaniu w tle.

### Przykład 4
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> $app | Publish-AzWebApp -ArchivePath C:\project\java_app.jar
```
### Przykład 5
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> Publish-AzWebApp -WebApp $app -ArchivePath C:\project\app.zip -Force
```

Przekazanie zawartości pliku java_app.jar do aplikacji sieci Web o nazwie ContosoApp należącej do grupy zasobów ContosoRG.

### Przykład 6
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> Publish-AzWebApp -WebApp $app -ArchivePath C:\project\app.zip -Timeout 300000 -Force
```

Przekazanie zawartości pliku java_app.jar do aplikacji sieci Web o nazwie ContosoApp należącej do grupy zasobów ContosoRG. Użytkownik może ustawić czas (w milisekundach) na czas oczekiwania przed przeożeniem czasu żądania.

## PARAMETERS

### - ArchivePath
Ścieżka pliku archiwum. Obsługiwane są kody ZIP, WAR i JAR.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — AsJob
Uruchamianie polecenia cmdlet w tle

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Wymuszanie
Wymuszanie usuwania opcji

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Nazwa
Nazwa aplikacji sieci Web.

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Nazwa grupy zasobów.

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Slot
Nazwa miejsca aplikacji sieci Web.

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Limit czasu
Ustawia czas (w milisekundach) oczekiwania przed przeożeniem czasu żądania.

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### - WebApp
Obiekt aplikacji sieci Web

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: FromWebApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### System.String

### Microsoft.Azure.Commands.WebApps.Models.PSSite

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.WebApps.Models.PSSite

## NOTATKI

## LINKI POKREWNE
