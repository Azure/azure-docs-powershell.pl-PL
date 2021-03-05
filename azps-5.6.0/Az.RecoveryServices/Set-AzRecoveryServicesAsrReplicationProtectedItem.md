---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/set-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: ad3f2c07d358819917706253df05bfd899c3b53e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997459"
---
# Set-AzRecoveryServicesAsrReplicationProtectedItem

## SYNOPSIS
Ustawia właściwości odzyskiwania, takie jak sieć docelowa i rozmiar maszyny wirtualnej dla określonego elementu chronionego replikacją.

## SKŁADNIA

```
Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem> [-Name <String>]
 [-Size <String>] [-UpdateNic <String>] [-RecoveryNetworkId <String>] [-PrimaryNic <String>]
 [-RecoveryCloudServiceId <String>] [-RecoveryNicSubnetName <String>] [-RecoveryNicStaticIPAddress <String>]
 [-NicSelectionType <String>] [-RecoveryResourceGroupId <String>] [-LicenseType <String>]
 [-RecoveryAvailabilitySet <String>] [-RecoveryAvailabilityZone <String>]
 [-RecoveryProximityPlacementGroupId <String>] [-EnableAcceleratedNetworkingOnRecovery]
 [-RecoveryBootDiagStorageAccountId <String>]
 [-AzureToAzureUpdateReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]>]
 [-DiskEncryptionVaultId <String>] [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionVaultId <String>] [-UseManagedDisk <String>]
 [-DiskIdToDiskEncryptionSetMap <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-RecoveryPublicIPAddressId <String>] [-RecoveryNetworkSecurityGroupId <String>]
 [-RecoveryLBBackendAddressPoolId <String[]>] [-TfoAzureVMName <String>]
 [-ASRVMNicConfiguration <ASRVMNicConfig[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## OPIS
Polecenie cmdlet **Set-AzRecoveryServicesAsrReplicationProtectedItem** ustawia właściwości odzyskiwania elementu chronionego replikacją.

## PRZYKŁADY

### Przykład 1
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $RPI -UpdateNic $NicId -RecoveryNetworkId $AzureNetworkID -RecoveryNicSubnetName $subnetName
```

Rozpoczyna operację aktualizowania ustawień elementów chronionych replikacją przy użyciu określonych parametrów i zwraca zadanie asr służące do śledzenia operacji.

### Przykład 2
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject $rpi -UpdateNic "00:50:56:8F:3F:7B" -RecoveryNetworkId $recoveryNetwork -RecoveryNicSubnetName $recoverySubnet -NicSelectionType NotSelected
```

Rozpoczyna operację aktualizowania ustawień karty interfejsu sieciowego elementu chronionego replikacją (zmniejszenie NIC) przy użyciu określonych parametrów i zwraca zadanie asr służące do śledzenia operacji.

### Przykład 3
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject $rpi -PrimaryNic "00:50:56:8F:3F:7B"
```

Rozpoczyna operację aktualizowania podstawowego elementu chronionego replikacją nic(do użycia dla odzyskanych ustawień maszyny wirtualnej) przy użyciu określonych parametrów i zwraca zadanie asr służące do śledzenia operacji.

### Przykład 4
```
PS C:\>Set-ASRReplicationProtectedItem -InputObject $rpi -UpdateNic $updateNic -RecoveryNetworkId $recoveryNetworkId -RecoveryNicSubnetName $recoveryNicSubnetName�-NicSelectionType SelectedByUser
```

Rozpoczyna operację aktualizowania ustawień elementu chronionego replikacją NIC (używanego dla odzyskanej maszyny wirtualnej) przy użyciu określonych parametrów i zwraca zadanie asr służące do śledzenia operacji.

### Przykład 5
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject $ rpi -UpdateNic $updateNic `
        -RecoveryNetworkId $recoveryNetworkId -RecoveryNicSubnetName $recoveryNicSubnetName -EnableAcceleratedNetworkingOnRecovery
```

Rozpoczyna operację aktualizowania elementu chronionego replikacją wybranego elementu noc noc włączyć przyspieszone sieci przy odzyskiwaniu maszyny WIRTUALNEj (dla platformy Azure do odzyskiwania po awarii platformy Azure).
Nie pass -EnableAcceleratedNetworkingOnRecovery, aby wyłączyć przyspieszone sieci.

### Przykład 6
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject $ rpi `
    -DiskEncryptionVaultId  $DiskEncryptionVaultId   �-DiskEncryptionSecertUrl $DiskEncryptionSecertUrl `
     -KeyEncryptionVaultId $KeyEncryptionVaultId  -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl
```

Rozpocznij operację aktualizacji dla określonego zaszyfrowanego elementu chronionego replikacją, aby użyć podanych szczegółów szyfrowania dla maszyny wirtualnej trybu failover.

### Przykład 7
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject $ rpi -RecoveryProximityPlacementGroupId $ppg
```

Uruchom operację aktualizacji dla określonego elementu chronionego replikacją, aby użyć podanej grupy położenia odległości dla maszyny wirtualnej trybu failover.

## PARAMETERS

### -ASRVMNicConfiguration
Określa szczegóły konfiguracji testów trybu failover i nic trybu failover.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMNicConfig[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AzureToAzureUpdateReplicationConfiguration
Określa konfigurację dysku do upated dla zarządzanej maszyny wirtualnej dysku (Azure to Azure DR scenrio).

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### -DiskEncryptionSecretUrl
Określa tajny adres URL szyfrowania dysku z wersją(szyfrowanie dysku platformy Azure), który ma być używany jako odzyskiwania maszyny wirtualnej po trybie failover.

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

### -DiskEncryptionVaultId
Określa identyfikator magazynu klucza tajnego szyfrowania dysku(szyfrowanie dysku platformy Azure), który ma być używany jako odzyskiwania maszyny wirtualnej po trybie failover.

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

### -DiskIdTo DefragmentEncryptionSetMap
Słownik z identyfikatorem zasobu dysku ustawionym jako identyfikator ARM dysków.

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableAcceleratedNetworkingOnRecovery
Określa określoną wartość NIC na maszyny wirtualnej odzyskiwania po trybie failover z przyspieszonym trybem sieci.

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

### -InputObject
Obiekt wejściowy do polecenia cmdlet: obiekt elementu chronionego replikacją asr, odpowiadający elementowi chronionego replikacją do zaktualizowania.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: ReplicationProtectedItem

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -KeyEncryptionKeyUrl
Określa wersję adresu URL klucza szyfrowania dysku (szyfrowanie dysku platformy Azure), która ma być używana jako odzyskiwania maszyny wirtualnej po trybie failover.

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

### -KeyEncryptionVaultId
Określa klucz klucza szyfrowania dyskuVault ID(szyfrowanie dysku platformy Azure), który ma być używany jako maszyny wirtualnej odzyskiwania po trybie failover.


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

### -LicenseType
Specyfikuj wybór typu licencji, który ma być używany dla maszyn wirtualnych systemu Windows Server. Jeśli masz prawo do używania korzyści z używania hybrydowego rozwiązania azure (HUB) do migracji i chcesz określić, że ustawienie CENTRUM ma być używane w przypadku awarii tego chronionego elementu, ustaw dla tego chronionego elementu typ licencji: WindowsServer.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: NoLicenseType, WindowsServer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Nazwa
Określa nazwę maszyny wirtualnej odzyskiwania, która zostanie utworzona w trybie failover.

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

### -NicSelectionType
Określa właściwości karty interfejsu sieciowego (NIC) ustawiane domyślnie przez użytkownika.
Aby wrócić do wartości domyślnych, możesz określić wartość NotSelected (Niesłyszące).

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: NotSelected, SelectedByUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrimaryNic
Określa wartość NIC, która będzie używana jako podstawowa karta NIC dla recvcovery MASZYNY WIRTUALNEj po zakończeniu trybu failover.

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

### -RecoveryAvailabilitySet
Zestaw dostępności dla elementu chronionego replikacją po trybie failover.

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

### -RecoveryAvailabilityZone
Określa strefę dostępności dla elementu chronionego replikacją po trybie failover.

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

### -RecoveryBootDiagStorageAccountId
Określa konto magazynu na potrzeby diagnostyki rozruchu dla odzyskiwania maszyny wirtualnej azure.

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

### -RecoveryCloudServiceId
Identyfikator zasobu usługi odzyskiwania w chmurze do trybu failover tej maszyny wirtualnej.

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

### -RecoveryLBBackendAddressPoolId
Określa pule docelowych adresów zaplecza, które mają być skojarzone z skojarzoną z siecią NIC odzyskiwania.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecoveryNetworkId
Określa identyfikator sieci wirtualnej platformy Azure, w której należy przelać element chroniony.

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

### -RecoveryNetworkSecurityGroupId
Określa identyfikator grupy zabezpieczeń sieci, która ma zostać skojarzona z skojarzoną z siecią NIC odzyskiwania.

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

### -RecoveryNicDressIPAddress
Określa statyczny adres IP, który powinien być przypisany do podstawowej karty NIC podczas odzyskiwania.

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

### -RecoveryNicSubnetName
Określa nazwę podsieci w wirtualnej sieci azure odzyskiwania, z którą ten element chroniony powinien być połączony w trybie failover.

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

### -RecoveryProximityPlacementGroupId
Określa identyfikator zasobu grupy położenia odległości odzyskiwania do trybu failover maszyny wirtualnej.

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

### -RecoveryPublicIPAddressId
Określa identyfikator publicznego zasobu adresu IP, który ma zostać skojarzony z skojarzoną z skojarzoną z siecią NIC odzyskiwania.

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

### -RecoveryResourceGroupId
Identyfikator grupy zasobów platformy Azure w regionie odzyskiwania, w którym chroniony element zostanie odzyskany w trybie failover.

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

### — Rozmiar
Określa rozmiar maszyny wirtualnej odzyskiwania.
Wartość powinna pochodzić z zestawu rozmiarów obsługiwanych przez maszyny wirtualne platformy Azure.

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

### -TfoAzureVMName
Określa nazwę testowej maszyny wirtualnej trybu failover.

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

### -UpdateNic
Określa wartość NIC maszyny wirtualnej, dla której to polecenie cmdlet ustawia właściwość sieci odzyskiwania wymaga udpated.

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

### -UseManaged Jednakowy
Określa, czy maszyną wirtualną platformy Azure utworzoną w ramach trybu failover powinny być dyskietki zarządzane.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: True, False

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Potwierdź
Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet. Polecenie cmdlet nie zostanie uruchomione.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob

## NOTATKI

## LINKI POKREWNE

[Get-AzRecoveryServicesAsrReplicationProtectedItem](./Get-AzRecoveryServicesAsrReplicationProtectedItem.md)

[New-AzRecoveryServicesAsrReplicationProtectedItem](./New-AzRecoveryServicesAsrReplicationProtectedItem.md)

[Remove-AzRecoveryServicesAsrReplicationProtectedItem](./Remove-AzRecoveryServicesAsrReplicationProtectedItem.md)
