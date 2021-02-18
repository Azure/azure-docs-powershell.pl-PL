---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/copy-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Copy-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Copy-AzRecoveryServicesVault.md
ms.openlocfilehash: e456ae28bec5f5421dad9c58bc5afb58c4d0d250
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202107"
---
# Copy-AzRecoveryServicesVault

## SYNOPSIS
Kopiuje dane z magazynu w jednym regionie do magazynu w innym regionie.

## SKŁADNIA

```
Copy-AzRecoveryServicesVault [-Force] [-DefaultProfile <IAzureContextContainer>] [-SourceVault] <ARSVault>
 [-TargetVault] <ARSVault> [-RetryOnlyFailed] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Copy-AzRecoveryServicesVault** kopiuje dane z magazynu w jednym regionie do magazynu w innym regionie. Obecnie obsługujemy tylko przenoszenie danych na poziomie magazynu.

## PRZYKŁADY

### Przykład 1. Kopiowanie danych z magazynu 1 do magazynu2
```
PS C:\> $sourceVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName1" -Name "vault1"
PS C:\> $targetVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName2" -Name "vault2"
PS C:\> Copy-AzRecoveryServicesVault -SourceVault $sourceVault -TargetVault $targetVault
```

Pierwsze dwa polecenia cmdlet pobierają magazyn usług odzyskiwania — odpowiednio magazyn1 i magazyn2.
Drugie polecenie wyzwala pełne przeniesienie danych z magazynu 1 do magazynu2. 

### Przykład 2. Kopiowanie danych z magazynu 1 do magazynu2 tylko z elementami, które zakończyły się niepowodzeniem
```
PS C:\> $sourceVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName1" -Name "vault1"
PS C:\> $targetVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName2" -Name "vault2"
PS C:\> Copy-AzRecoveryServicesVault -SourceVault $sourceVault -TargetVault $targetVault -RetryOnlyFailed
```

Pierwsze dwa polecenia cmdlet pobierają magazyn usług odzyskiwania — odpowiednio magazyn1 i magazyn2.
Drugie polecenie wyzwala częściowe przeniesienie danych z magazynu 1 do magazynu2 tylko z tymi elementami, które nie powiodły się w poprzednich operacjach przenoszenia.

## PARAMETERS

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.

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

### — Wymuszanie
Wymusza operację przenoszenia danych (uniemożliwia okno dialogowe potwierdzenia) bez pytania o potwierdzenie dla docelowego typu nadmiarowości magazynu magazynu. Ten parametr jest opcjonalny. 

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

### -RetryOnlyFailed
Przełącz parametr, aby wypróbować przenoszenie danych tylko dla kontenerów w magazynie źródłowym, które nie zostały jeszcze przeniesione.

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

### -SourceVault
Obiekt magazynu źródłowego, który ma zostać przeniesiony.

```yaml
Type: ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### - TargetVault
Obiekt magazynu docelowego, do którego należy przenieść dane.

```yaml
Type: ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### Microsoft.Azure.Commands.RecoveryServices.ARSVault

## DANE WYJŚCIOWE

### System.String

## NOTATKI

## LINKI POKREWNE
