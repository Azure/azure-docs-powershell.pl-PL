---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSnapshot.md
ms.openlocfilehash: 350f7d5b44f5a1c84f97511a4febb7d967ee2de4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050811"
---
# Get-AzWebAppSnapshot

## STRESZCZENIe
Pobiera migawki dostępne dla aplikacji sieci Web.

## POLECENIA

### FromResourceName
```
Get-AzWebAppSnapshot [-UseDisasterRecovery] [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### FromWebApp
```
Get-AzWebAppSnapshot [-UseDisasterRecovery] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzWebAppSnapshot** zwraca wszystkie migawki dla aplikacji sieci Web. Migawki to automatyczne tworzenie kopii zapasowych plików i ustawień aplikacji sieci Web. Migawkę można przywrócić przy użyciu polecenia cmdlet **Restore-AzWebAppSnapshot** .

## Przykłady

### Przykład 1
```
PS C:\> Get-AzWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging"
```

Pobierz migawki dla aplikacji sieci Web o nazwie "ContosoApp" z miejscem o nazwie "przemieszczanie" w grupie zasobów "Default-Web-Zachodnia"

## PARAMETRÓW

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

### -UseDisasterRecovery
Odczytaj migawki z pomocniczej jednostki skali.

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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### System. String

### Microsoft. Azure. Commands. webapps. modele. PSSite

## WYSYŁA

### Microsoft. Azure. polecenia. webapps. polecenia cmdlet. BackupRestore. AzureWebAppSnapshot

## INFORMACYJN

## LINKI POKREWNE
