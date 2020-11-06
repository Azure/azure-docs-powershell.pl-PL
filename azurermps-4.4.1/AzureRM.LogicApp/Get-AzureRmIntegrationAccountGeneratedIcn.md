---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountGeneratedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountGeneratedIcn.md
ms.openlocfilehash: 2855f5da15de776d7fd85bd267f6a082a85ba5c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527510"
---
# Get-AzureRmIntegrationAccountGeneratedIcn

## STRESZCZENIe
To polecenie cmdlet pobiera bieżącą wartość wygenerowanego numeru kontrolnego wymiany na umowę.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Get-AzureRmIntegrationAccountGeneratedIcn -ResourceGroupName <String> -Name <String> [-AgreementName <String>]
 [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
To polecenie cmdlet jest przeznaczone do użycia w scenariuszach odzyskiwania po awarii w celu pobrania bieżącej wartości wygenerowanego numeru kontrolnego wymiany, tak aby można było zapisać zwiększoną wartość o wartości Set-AzureRmIntegrationAccountGeneratedIcn.
Numer kontrolki wymiany należy zwiększyć, aby uniknąć powielonych numerów kontrolnych wymiany dla liczb, które nie zostały jeszcze zreplikowane w regionie pasywnym, gdy wystąpił klęska żywiołowa w aktywnym regionie.
Podaj parametr "-Agreementtype", aby określić, czy numery kontrolek X12 lub EDIFACT mają być zwracane.

## Przykłady

### Przykład 1
```
PS C:\> Get-AzureRmIntegrationAccountGeneratedIcn -AgreementType "X12" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "X12IntegrationAccountAgreement"
ControlNumber            : 1000
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

To polecenie umożliwia uzyskiwanie wygenerowanego numeru kontrolnego wymiany X12 z konta integracji według nazwy umowy. Upewnij się, że określona umowa jest typu "X12"

### Przykład 2
```
PS C:\> Get-AzureRmIntegrationAccountGeneratedIcn -AgreementType "Edifact" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "EdifactIntegrationAccountAgreement"
ControlNumber            : 1000
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

To polecenie umożliwia uzyskiwanie wygenerowanego numeru kontrolnego wymiany EDIFACT z konta integracji według nazwy umowy. Upewnij się, że określona umowa jest typu "EDIFACT"

### Przykład 3
```
PS C:\> Get-AzureRmIntegrationAccountGeneratedIcn -AgreementType "X12" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1"
ControlNumber            : 1000
ControlNumberChangedTime : 2/22/2017 8:05:41 PM
AgreementName            : X12IntegrationAccountAgreement1
IsMessageProcessingFailed:

ControlNumber            : 1000
ControlNumberChangedTime : 2/22/2017 8:05:41 PM
AgreementName            : X12IntegrationAccountAgreement2
IsMessageProcessingFailed:

ControlNumber            : No generated control number was found for this agreement.
ControlNumberChangedTime : 1/1/0001 12:00:00 AM
AgreementName            : X12IntegrationAccountAgreement3
IsMessageProcessingFailed:
```

To polecenie pobiera wszystkie wygenerowaną X12 numery kontrolne wymiany według nazwy konta integracji.

## PARAMETRÓW

### -Agreementname
Nazwa umowy dotyczącej konta integracji.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (nazwa)
Nazwa konta integracji.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nazwa grupy zasobów konta integracji.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Agreementtype
Typ umowy dotyczącej konta integracji.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MessageType

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### System. String

## WYSYŁA

### Microsoft. Azure. Commands. LogicApp. Utilities. IntegrationAccountClient + IntegrationAccountControlNumber

## INFORMACYJN

## LINKI POKREWNE

[Set-AzureRmIntegrationAccountGeneratedIcn](./Set-AzureRmIntegrationAccountGeneratedIcn.md)

