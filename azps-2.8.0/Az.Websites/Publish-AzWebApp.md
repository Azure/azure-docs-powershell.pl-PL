---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/publish-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Publish-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Publish-AzWebApp.md
ms.openlocfilehash: 07ec4223414bbdbab8e3fa4d11641d040d918209
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93888281"
---
# Publish-AzWebApp

## STRESZCZENIe
Wdrażanie aplikacji Azure Web App z pliku ZIP, JAR lub WAR przy użyciu zipdeploy. 

## POLECENIA

### FromResourceName
```
Publish-AzWebApp -ArchivePath <String> [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### FromWebApp
```
Publish-AzWebApp -ArchivePath <String> [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Publish-AzWebApp** umożliwia przekazywanie zawartości do istniejącej aplikacji Azure Web App. Zawartość powinna zostać spakowana w pliku ZIP, jeśli korzystasz ze stosów, takich jak .NET, Python lub Node, lub pliku WAR lub JAR, jeśli korzystasz z języka Java. Zawartość powinna być wstępnie zbudowana i gotowa do uruchomienia bez dodatkowych kroków kompilacji podczas wdrażania. To polecenie cmdlet umożliwia wdrożenie zawartości przy użyciu funkcji kudu zipdeploy i wardeploy. Zapoznaj się z kudu wiki, aby uzyskać szczegółowe informacje na temat działania zipdeploy i wardeploy oraz jak poprawnie spakować aplikację sieci Web do wdrożenia. https://aka.ms/kuduzipdeploy i https://aka.ms/kuduwardeploy zawierające pomocne informacje na temat zipdeploy i wardeploy.

## Przykłady

### Przykład 1
```powershell
PS C:\> Publish-AzWebApp -ResourceGroupName Default-Web-WestUS -Name MyApp -ArchivePath C:\project\app.zip
```

Umożliwia przekazywanie zawartości app.zip do aplikacji sieci Web o nazwie MojaApl należącej do grupy zasobów Default — w sieci Web.

### Przykład 2
```powershell
PS C:\> Publish-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp -Slot Staging -ArchivePath C:\project\javaproject.war
```

Umożliwia przekazywanie zawartości javaproject. War do miejsca przemieszczania aplikacji sieci Web o nazwie ContosoApp należącej do ContosoRG grupy zasobów.

### Przykład 3
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> Publish-AzWebApp -WebApp $app -ArchivePath C:\project\app.zip -AsJob
```

Umożliwia przekazywanie zawartości app.zip do aplikacji sieci Web o nazwie ContosoApp należącej do ContosoRG grupy zasobów. Polecenie cmdlet zostanie uruchomione w tle zadania.

### Przykład 4
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> $app | Publish-AzWebApp -ArchivePath C:\project\java_app.jar
```

Umożliwia przekazywanie zawartości java_app. jar do aplikacji sieci Web o nazwie ContosoApp należącej do ContosoRG grupy zasobów.

## PARAMETRÓW

### -ArchivePath
Ścieżka pliku archiwum. Obsługa ZIP, wojny i JAR.

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

### -AsJob
Uruchom polecenie cmdlet w tle

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
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

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

### -Name (nazwa)
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

### -Slot
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

### -Aplikacji
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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### System. String

### Microsoft. Azure. Commands. webapps. modele. PSSite

## WYSYŁA

### Microsoft. Azure. Commands. webapps. modele. PSSite

## INFORMACYJN

## LINKI POKREWNE
