---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 3CD449A1-084E-4950-80EF-06B5ECDFB70F
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/reset-azwebappslotpublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppSlotPublishingProfile.md
ms.openlocfilehash: 840e0bb2bfa10a89a5ba963e83ab434e795b3dd4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063764"
---
# Reset-AzWebAppSlotPublishingProfile

## STRESZCZENIe

## POLECENIA

### S1
```
Reset-AzWebAppSlotPublishingProfile [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### S2
```
Reset-AzWebAppSlotPublishingProfile [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Reset-AzWebAppSlotPublishingProfile** resetuje profil publikowania dla określonego miejsca aplikacji sieci Web.

## Przykłady

### Przykład 1
```powershell
PS C:\> Reset-AzWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001"
```

To polecenie resetuje profil publikowania dla gniazda o nazwie slot001 dla aplikacji sieci Web ContosoWebApp skojarzonego z domyślną grupą zasobów — Web-Zachodnia.

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
Nazwa aplikacji

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Nazwa grupy zasobów

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Slot
Nazwa gniazda aplikacji

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Aplikacji
Obiekt aplikacji

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
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

### System. String

## INFORMACYJN

## LINKI POKREWNE
