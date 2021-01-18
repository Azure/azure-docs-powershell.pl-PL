---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationFabric.md
ms.openlocfilehash: 8230056069668765d3d27a9dd54538a310edf383
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98498961"
---
# Get-AzMigrateReplicationFabric

## STRESZCZENIe
Umożliwia wyświetlenie szczegółów dotyczących sieci szkieletowej odzyskiwania witryny Azure.

## POLECENIA

### Lista (domyślna)
```
Get-AzMigrateReplicationFabric -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### Pobierz
```
Get-AzMigrateReplicationFabric -FabricName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## Opis
Umożliwia wyświetlenie szczegółów dotyczących sieci szkieletowej odzyskiwania witryny Azure.

## Przykłady

### Przykład 1. Pobierz wszystkie materiały szkieletowe według grupy zasobów i nazwy magazynu
```powershell
PS C:\> PS Get-AzMigrateReplicationFabric -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault -FabricName AzMigratePWSHTc8d1replicationfabric

BcdrState                                 : Valid
CustomDetailInstanceType                  : VMwareV2
EncryptionDetailKekCertExpiryDate         :
EncryptionDetailKekCertThumbprint         :
EncryptionDetailKekState                  : None
FriendlyName                              : AzMigratePWSHTc8d1replicationfabric
Health                                    : Normal
HealthErrorDetail                         : {}
Id                                        : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsof
                                            t.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabr
                                            ic
InternalIdentifier                        : 501ff8f2-c9d7-5bf4-87ff-d0b3fc98aeb5
Location                                  :
Name                                      : AzMigratePWSHTc8d1replicationfabric
RolloverEncryptionDetailKekCertExpiryDate :
RolloverEncryptionDetailKekCertThumbprint :
RolloverEncryptionDetailKekState          : None
Type                                      : Microsoft.RecoveryServices/vaults/replicationFabrics
```

Pobieranie całej sieci szkieletowej w grupie zasobów i magazynie

### Przykład 2: pobieranie sieci szkieletowej według grup zasobów, nazwy i nazwy magazynu
```powershell
PS C:\> Get-AzMigrateReplicationFabric -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault

BcdrState                                 : Valid
CustomDetailInstanceType                  : VMwareV2
EncryptionDetailKekCertExpiryDate         :
EncryptionDetailKekCertThumbprint         :
EncryptionDetailKekState                  : None
FriendlyName                              : AzMigratePWSHTc8d1replicationfabric
Health                                    : Normal
HealthErrorDetail                         : {}
Id                                        : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsof
                                            t.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabr
                                            ic
InternalIdentifier                        : 501ff8f2-c9d7-5bf4-87ff-d0b3fc98aeb5
Location                                  :
Name                                      : AzMigratePWSHTc8d1replicationfabric
RolloverEncryptionDetailKekCertExpiryDate :
RolloverEncryptionDetailKekCertThumbprint :
RolloverEncryptionDetailKekState          : None
Type                                      : Microsoft.RecoveryServices/vaults/replicationFabrics
```

Uzyskiwanie określonego szkieletu

## PARAMETRÓW

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Fabricname
Nazwa sieci szkieletowej.

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nazwa grupy zasobów, w której znajduje się magazyn usług odzyskiwania.

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

### -ResourceName
Nazwa magazynu usług Recovery Services.

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

### -Subskrypcji
Identyfikator abonamentu.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

## WYSYŁA

### Microsoft. Azure. PowerShell. polecenia. Migruj. MODELES. Api20180110. IFabric

## INFORMACYJN

PISUJE

## LINKI POKREWNE

