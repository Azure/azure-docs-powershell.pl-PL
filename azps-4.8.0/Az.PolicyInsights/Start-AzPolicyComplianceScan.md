---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/start-azpolicycompliancescan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyComplianceScan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyComplianceScan.md
ms.openlocfilehash: 61022603ad34c345274328d47767e90580e54d6b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223679"
---
# Start-AzPolicyComplianceScan

## STRESZCZENIe
Wyzwala ocenę zgodności zasad dla wszystkich zasobów w subskrypcji lub grupie zasobów.

## POLECENIA

```
Start-AzPolicyComplianceScan [-ResourceGroupName <String>] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Start-AzPolicyComplianceScan** rozpoczyna ocenę zgodności zasad dla subskrypcji lub grupy zasobów. Stan zgodności wszystkich zasobów w tym zakresie będzie oceniany względem wszystkich przypisanych zasad.

## Przykłady

### Przykład 1. Rozpoczynanie skanowania zgodności w zakresie subskrypcji
```
PS C:\> Start-AzPolicyComplianceScan
```

To polecenie rozpoczyna ocenę zgodności z zasadami dotyczącymi aktywnej subskrypcji.

### Przykład 2: Rozpoczynanie skanowania zgodności w zakresie grupy zasobów
```
PS C:\> Start-AzPolicyComplianceScan -ResourceGroupName "myRG"
```

To polecenie rozpoczyna ocenę zgodności zasad dla grupy zasobów "myRG" w aktywnej subskrypcji.

### Przykład 3: Rozpoczynanie skanowania zgodności i oczekiwanie na ukończenie pracy w tle
```
PS C:\> $job = Start-AzPolicyComplianceScan -AsJob
PS C:\> $job | Wait-Job
```

To polecenie rozpoczyna ocenę zgodności z zasadami dotyczącymi aktywnej subskrypcji. Przestanie on czekać na ukończenie skanowania.

## PARAMETRÓW

### -AsJob
Uruchom polecenie cmdlet w tle.

```yaml
Type: SwitchParameter
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
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Zwraca wartość true, jeśli polecenie zostało pomyślnie ukończone.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nazwa grupy zasobów.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Potwierdź
Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.
Polecenie cmdlet nie jest uruchamiane.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

### System. String

## WYSYŁA

### System. Boolean

## INFORMACYJN

## LINKI POKREWNE
