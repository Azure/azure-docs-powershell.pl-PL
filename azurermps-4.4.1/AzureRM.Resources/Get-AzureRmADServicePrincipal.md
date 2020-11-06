---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 4DC26C26-6162-4A15-BFCB-4D2B6B52DD81
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADServicePrincipal.md
ms.openlocfilehash: 34f4b85a299e714f524b1a4d33f2fb717483c377
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553116"
---
# Get-AzureRmADServicePrincipal

## STRESZCZENIe
Umożliwia filtrowanie podmiotów zabezpieczeń usługi Active Directory.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

### EmptyParameterSet (domyślny)
```
Get-AzureRmADServicePrincipal [-ServicePrincipalName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### SearchStringParameterSet
```
Get-AzureRmADServicePrincipal -SearchString <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ObjectIdParameterSet
```
Get-AzureRmADServicePrincipal -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SPNParameterSet
```
Get-AzureRmADServicePrincipal -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Opis
Umożliwia filtrowanie podmiotów zabezpieczeń usługi Active Directory.

## Przykłady

### --------------------------Filtruje podmioty zabezpieczeń usługi przy użyciu nazwy SPN--------------------------
```
PS C:\> Get-AzureRmADServicePrincipal -SPN 36f81fc3-b00f-48cd-8218-3879f51ff39f
```

Pobiera podmioty zabezpieczeń usługi przy użyciu 36f81fc3-b00f-48cd-8218-3879f51ff39f SPN.

### --------------------------Filtruje podmioty zabezpieczeń usługi przy użyciu ciągu wyszukiwania--------------------------
```
PS C:\> Get-AzureRmADServicePrincipal -SearchString "Web"
```

Filtruje wszystkie podmioty zabezpieczeń usługi AD z wyświetlaną nazwą, rozpoczynając od "sieci Web".

### ----------------------------------------------------Głównych usług REKLAMowych
```
PS C:\> Get-AzureRmADServicePrincipal
```

Pobiera wszystkich głównych podmiotów usługi AD.

## PARAMETRÓW

### -ObjectId
Identyfikator obiektu głównego usługi.

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SearchString
Pobiera wszystkie podmioty główne usługi, których nazwa wyświetlana rozpoczyna się od tej wartości.

```yaml
Type: System.String
Parameter Sets: SearchStringParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServicePrincipalName
SPN usługi.

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet
Aliases: SPN

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

### System. Collections. Generic. list "1 [Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADServicePrincipal]

## INFORMACYJN

## LINKI POKREWNE

[Nowe — AzureRmADServicePrincipal](./New-AzureRmADServicePrincipal.md)

[Set-AzureRmADServicePrincipal](./Set-AzureRmADServicePrincipal.md)

[Remove-AzureRmADServicePrincipal](./Remove-AzureRmADServicePrincipal.md)

[Get-AzureRmADApplication](./Get-AzureRmADApplication.md)

[Get-AzureRmADSpCredential](./Get-AzureRmADSpCredential.md)

