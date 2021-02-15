---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 82C7B128-8818-4390-B1A5-CB40AC9D53CA
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchAccount.md
ms.openlocfilehash: cd175baa39c329c301913f2abb5e70eaedcf45f6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197075"
---
# New-AzBatchAccount

## SYNOPSIS
Tworzy konto usługi Batch.

## SKŁADNIA

```
New-AzBatchAccount [-AccountName] <String> [-Location] <String> [-ResourceGroupName] <String>
 [[-AutoStorageAccountId] <String>] [-PoolAllocationMode <PoolAllocationMode>] [-KeyVaultId <String>]
 [-KeyVaultUrl <String>] [-Tag <Hashtable>] [-PublicNetworkAccess <PublicNetworkAccessType>]
 [-IdentityType <ResourceIdentityType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet New-AzBatchAccount** tworzy konto usługi Azure Batch dla określonej grupy zasobów i lokalizacji.

## PRZYKŁADY

### Przykład 1. Tworzenie konta wsadowego
```powershell
PS C:\>New-AzBatchAccount -AccountName "pfuller" -ResourceGroupName "ResourceGroup03" -Location "WestUS"
AccountName                  : pfuller
Location                     : westus
ResourceGroupName            : ResourceGroup03
DedicatedCoreQuota           : 20
LowPriorityCoreQuota         : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

To polecenie tworzy konto usługi Batch o nazwie Pfuller przy użyciu grupy zasobów ResourceGroup03 w lokalizacji Stanów Zjednoczonych Zachód.

### Przykład 2

Tworzy konto usługi Batch. (wygenerowane automatycznie)

<!-- Aladdin Generated Example -->
```powershell
New-AzBatchAccount -AccountName 'pfuller' -AutoStorageAccountId <String> -Location 'WestUS' -ResourceGroupName 'ResourceGroup03'
```

## PARAMETERS

### -AccountName
Określa nazwę konta usługi Batch, które tworzy to polecenie cmdlet.
Nazwy kont partii muszą mieć od 3 do 24 znaków i zawierać tylko cyfry i małe litery.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AutoStorageAccountId
Określa identyfikator zasobu konta magazynu używanego do automatycznego przechowywania.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -IdentityType
Tożsamość skojarzona z batchaccount

```yaml
Type: Microsoft.Azure.Management.Batch.Models.ResourceIdentityType
Parameter Sets: (All)
Aliases:
Accepted values: SystemAssigned, None

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyVaultId
Identyfikator zasobu magazynu kluczy platformy Azure skojarzonego z kontem usługi Batch.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -KeyVaultUrl
Adres URL magazynu kluczy platformy Azure skojarzonego z kontem usługi Batch.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Lokalizacja
Określa region, w którym to polecenie cmdlet tworzy konto.
Aby uzyskać więcej informacji, zobacz [Regiony platformy Azure.](https://azure.microsoft.com/en-us/regions)

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PoolAllocationMode
Tryb alokacji dla tworzenia pul na koncie wsadowym.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Batch.Models.PoolAllocationMode]
Parameter Sets: (All)
Aliases:
Accepted values: BatchService, UserSubscription

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublicNetworkAccess
Typ dostępu do sieci publicznej

```yaml
Type: Microsoft.Azure.Management.Batch.Models.PublicNetworkAccessType
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów, w której to polecenie cmdlet tworzy konto.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Tag
Pary klucz-wartość w postaci tabeli skrótu. Na przykład: @{key0="value0";key1=$null;key2="wartość2"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### System.String

### System.Nullable'1[[Microsoft.Azure.Management.Batch. Models.PoolAllocationMode, Microsoft.Azure.Management.Batch, Version=9.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]

### System.Collections.Hashtable

## OUTPUTS

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## NOTATKI

## LINKI POKREWNE

[Get-AzBatchAccount](./Get-AzBatchAccount.md)

[Remove-AzBatchAccount](./Remove-AzBatchAccount.md)

[Set-AzBatchAccount](./Set-AzBatchAccount.md)

[Polecenia cmdlet partii platformy Azure](/powershell/module/Az.Batch/)
