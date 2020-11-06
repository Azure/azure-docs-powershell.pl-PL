---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: ECD0950F-2490-49E2-85E6-5FA2A59364E6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsQuota.md
ms.openlocfilehash: b6edc46131bac545d649e6ea3fe41b142d596850
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527186"
---
# Get-AzureRmStreamAnalyticsQuota

## STRESZCZENIe
Pobiera informacje na temat przydziału jednostki transmisji strumieniowej dla regionu.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Get-AzureRmStreamAnalyticsQuota [-Location] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureRmStreamAnalyticsQuota** pobiera informacje na temat przydziału jednostki transmisji strumieniowej dla regionu.

## Przykłady

### PRZYKŁAD 1: uzyskiwanie informacji na temat przydziału jednostek transmisji strumieniowej dla regionu
```
PS C:\>Get-AzureRmStreamAnalyticsQuota -Location "West US"
```

To polecenie zwraca informacje na temat przydziału jednostek transmisji strumieniowej i użytkowania w zachodnim regionie Stanów Zjednoczonych.

## PARAMETRÓW

### — Lokalizacja
Określa nazwę obszaru platformy Azure lub lokalizacji centrum danych, dla którego mają być uzyskiwane informacje o przydziałach jednostki transmisji strumieniowej.
Zobacz https://azure.microsoft.com/en-us/regions/#serviceshttps://azure.microsoft.com/en-us/regions/#services listę obsługiwanych regionów platformy Azure.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
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

### System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. StreamAnalytics. MODELES. PSQuota, Microsoft. Azure. Commands. StreamAnalytics]] Microsoft. Azure. Commands. StreamAnalytics. modele. PSQuota

## INFORMACYJN

## LINKI POKREWNE

[Polecenia cmdlet usługi Analiza strumienia Azure](./AzureRM.StreamAnalytics.md)


