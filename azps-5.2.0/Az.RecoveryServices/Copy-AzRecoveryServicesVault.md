---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/copy-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Copy-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Copy-AzRecoveryServicesVault.md
ms.openlocfilehash: 68c2914c694dbfb89044597fc35582a83f426b6c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341581"
---
# Copy-AzRecoveryServicesVault

## STRESZCZENIe
Kopiuje dane z magazynu w jednym regionie do magazynu w innym regionie.

## POLECENIA

```
Copy-AzRecoveryServicesVault [-Force] [-DefaultProfile <IAzureContextContainer>] [-SourceVault] <ARSVault>
 [-TargetVault] <ARSVault> [-RetryOnlyFailed] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **copy-AzRecoveryServicesVault** kopiuje dane z magazynu w jednym regionie do magazynu w innym regionie. Obecnie obsługujemy tylko przenoszenie danych na poziomie magazynu.

## Przykłady

### Przykład 1: kopiowanie danych z vault1 do vault2
```powershell
PS C:\> $sourceVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName1" -Name "vault1"
PS C:\> $targetVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName2" -Name "vault2"
PS C:\> Copy-AzRecoveryServicesVault -SourceVault $sourceVault -TargetVault $targetVault
```

Pierwszy z dwóch pierwszych apletów polecenia Pobierz magazyn usług Recovery Services-vault1 i vault2.
Drugie polecenie wyzwala pełne dane z vault1 do vault2. 

### Przykład 2: kopiowanie danych z vault1 do vault2 tylko za pomocą elementów nieuszkodzonych
```powershell
PS C:\> $sourceVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName1" -Name "vault1"
PS C:\> $targetVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName2" -Name "vault2"
PS C:\> Copy-AzRecoveryServicesVault -SourceVault $sourceVault -TargetVault $targetVault -RetryOnlyFailed
``` 

Pierwszy z dwóch pierwszych apletów polecenia Pobierz magazyn usług Recovery Services-vault1 i vault2.
Drugie polecenie wyzwala częściowe dane przenoszone z vault1 do vault2 z tylko elementami, które nie powiodły się w poprzednich operacjach przenoszenia.

## PARAMETRÓW

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

### -Force
Wymusza operację przenoszenia danych (zapobiega wyświetleniu okna dialogowego potwierdzenia) bez monitowania o potwierdzenie typu nadmiarowości miejsca do magazynowania w magazynie docelowym. Ten parametr jest opcjonalny. 

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
Parametr Przełącz umożliwiający przenoszenie danych tylko w przypadku kontenerów w magazynie źródłowym, które nie zostały jeszcze przeniesione.

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

### -TargetVault
Docelowy obiekt magazynu, w którym mają zostać przeniesione dane.

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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

### Microsoft. Azure. Commands. RecoveryServices. ARSVault

## WYSYŁA

### System. String

## INFORMACYJN

## LINKI POKREWNE
