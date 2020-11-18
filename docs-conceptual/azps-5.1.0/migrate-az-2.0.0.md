---
title: Przewodnik migracji modułu Az 2.0.0
description: Ten przewodnik migracji zawiera listę zmian powodujących niezgodność wprowadzonych w wersji 2.0 modułu Az programu Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/24/2019
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: ebe18c24881f146b7cf885892c7869cd7167d511
ms.sourcegitcommit: d81c3b0f0f7289104be03869eb675128b61db7d3
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/17/2020
ms.locfileid: "94715820"
---
# <a name="migration-guide-for-az-200"></a>Przewodnik migracji modułu Az 2.0.0

Ten dokument zawiera opis różnic między wersjami 1.0.0 i 2.0.0 modułu Az 

## <a name="table-of-contents"></a>Spis treści
- [Zmiany powodujące niezgodność modułów](#module-breaking-changes)
  - [Az.Compute](#azcompute)
  - [Az.HDInsight](#azhdinsight)
  - [Az.Storage](#azstorage)

## <a name="module-breaking-changes"></a>Zmiany powodujące niezgodność modułów

### <a name="azcompute"></a>Az.Compute

- Usunięto parametr `Managed` z poleceń cmdlet `New-AzAvailabilitySet` i `Update-AzAvailabilitySet` na rzecz parametru ```Sku = Aligned```

  #### <a name="before"></a>Przed

  ```powershell
  Update-AzAvailabilitySet -Managed
  ```

  #### <a name="after"></a>Po

  ```powershell
  Update-AzAvailabilitySet -Sku Aligned
  ```
- W celu zapewnienia spójności usunięto parametr `Image` z zestawu parametrów „ByName” i „ByResourceId” w poleceniu `Update-AzImage` 
  
  #### <a name="before"></a>Przed

  Pamiętaj, że poniższy kod będzie działać, ale przekazany parametr ImageName nie jest używany, więc jego usunięcie nie ma żadnego wpływu na funkcjonalność.

  ```powershell
  Update-AzImage -ResourceGroupName $Rg -ImageName $Name -Image $Image -Tag $tags

  Update-AzImage -ResourceId $Id -Image $Image -Tag $tags
  ```

  #### <a name="after"></a>Po

  ```powershell
  Update-AzImage -ResourceGroupName $Rg -ImageName $Name -Tag $tags

  Update-AzImage -ResourceId $Id -Tag $tags
  ```

- W celu zapewnienia spójności usunięto parametr `Name` z zestawów parametrów „ByObject” i „ByResourceId” w poleceniu `Restart-AzVM`
  
  #### <a name="before"></a>Przed

  Pamiętaj, że poniższy kod będzie działać, ale przekazany parametr Name nie jest używany, więc jego usunięcie nie ma żadnego wpływu na funkcjonalność.
  ```powershell
  Restart-AzVM -InputObject $VM -Name $Name 

  Restart-AzVM -ResourceId $Id -Name $Name
  ```

  #### <a name="after"></a>Po

  ```powershell
  Restart-AzVM -InputObject $VM

  Restart-AzVM -ResourceId $Id
  ```

- W celu zapewnienia spójności usunięto parametr `Name` z zestawów parametrów „ByObject” i „ByResourceId” w poleceniu `Start-AzVM`
  
  #### <a name="before"></a>Przed

  Pamiętaj, że poniższy kod będzie działać, ale przekazany parametr Name nie jest używany, więc jego usunięcie nie ma żadnego wpływu na funkcjonalność.

  ```powershell
  Start-AzVM -InputObject $VM -Name $Name 

  Start-AzVM -ResourceId $Id -Name $Name
  ```

  #### <a name="after"></a>Po

  ```powershell
  Start-AzVM -InputObject $VM

  Start-AzVM -ResourceId $Id
  ```

- W celu zapewnienia spójności usunięto parametr `Name` z zestawów parametrów „ByObject” i „ByResourceId” w poleceniu `Stop-AzVM`
  
  #### <a name="before"></a>Przed

  Pamiętaj, że poniższy kod będzie działać, ale przekazany parametr Name nie jest używany, więc jego usunięcie nie ma żadnego wpływu na funkcjonalność.

  ```powershell
  Stop-AzVM -InputObject $VM -Name $Name 

  Stop-AzVM -ResourceId $Id -Name $Name
  ```

  #### <a name="after"></a>Po

  ```powershell
  Stop-AzVM -InputObject $VM

  Stop-AzVM -ResourceId $Id
  ```

- W celu zapewnienia spójności usunięto parametr `Name` z zestawów parametrów „ByObject” i „ByResourceId” w poleceniu `Remove-AzVM`
  
  #### <a name="before"></a>Przed

  Pamiętaj, że poniższy kod będzie działać, ale przekazany parametr Name nie jest używany, więc jego usunięcie nie ma żadnego wpływu na funkcjonalność.

  ```powershell
  Remove-AzVM -InputObject $VM -Name $Name

  Remove-AzVM -ResourceId $Id -Name $Name 
  ```

  #### <a name="after"></a>Po

  ```powershell
  Remove-AzVM -InputObject $VM 

  Remove-AzVM -ResourceId $Id 
  ```

- W celu zapewnienia spójności usunięto parametr `Name` z zestawów parametrów „ByObject” i „ByResourceId” w poleceniu `Set-AzVM`
  
  #### <a name="before"></a>Przed

  Pamiętaj, że poniższy kod będzie działać, ale przekazany parametr Name nie jest używany, więc jego usunięcie nie ma żadnego wpływu na funkcjonalność.

  ```powershell
  Set-AzVM -InputObject $VM -Name $Name ...

  Set-AzVM -ResourceId $Id -Name $Name ...
  ```

  #### <a name="after"></a>Po

  ```powershell
  Set-AzVM -InputObject $VM ...

  Set-AzVM -ResourceId $Id ...
  ```

- W celu zapewnienia spójności usunięto parametr `Name` z zestawów parametrów „ByObject” i „ByResourceId” w poleceniu `Save-AzVMImage` 
  
  #### <a name="before"></a>Przed
  Pamiętaj, że poniższy kod będzie działać, ale przekazany parametr Name nie jest używany, więc jego usunięcie nie ma żadnego wpływu na funkcjonalność.
  ```powershell
  Save-AzVMImage -InputObject $VM -Name $Name ...

  Save-AzVMImage -ResourceId $Id -Name $Name ...
  ```
  #### <a name="after"></a>Po
  ```powershell
  Save-AzVMImage -InputObject $VM ...

  Save-AzVMImage -ResourceId $Id ...
  ```

- Dodano właściwość ProtectionPolicy w celu hermetyzacji właściwości `ProtectFromScaleIn` w klasie `PSVirtualMachineScaleSetVM`

  #### <a name="before"></a>Przed

  ```powershell
  $vmss = Get-AzVMssVM ...
  $vmss.ProtectFromScaleIn = $true

  $vmss = Update-AzVMssVM ...
  $vmss.ProtectFromScaleIn = $true

  $vmss = Remove-AzVMssVMDataDisk ...
  $vmss.ProtectFromScaleIn = $true
  ```

  #### <a name="after"></a>Po

  ```powershell
  $vmss = Get-AzVMssVM ...
  $vmss.ProtectionPolicy.ProtectFromScaleIn = $true

  $vmss = Update-AzVMssVM ...
  $vmss.ProtectionPolicy.ProtectFromScaleIn = $true

  $vmss = Remove-AzVMssVMDataDisk ...
  $vmss.ProtectionPolicy.ProtectFromScaleIn = $true

  ```

- Dodano właściwość ```EncryptionSettingsCollection``` w celu objęcia właściwości `EncryptionSettings` w klasie `PSDisk`

  #### <a name="before"></a>Przed

  ```powershell
  $disk = New-AzDisk ... | Set-AzDiskDiskEncrytionKey ...
  $disk.EncryptionSettings

  $disk = New-AzDisk ... | Set-AzDiskKeyEncrytionKey ...
  $disk.EncryptionSettings

  $update = New-AzDiskUpdateConfig | Set-AzDiskUpdateDiskEncryptionKey ...
  $update.EncryptionSettings

  $update = New-AzDiskUpdateConfig | Set-AzDiskUpdateKeyEncryptionKey ...
  $update.EncryptionSettings
  ```

  #### <a name="after"></a>Po

  ```powershell
  $disk = New-AzDisk ... | Set-AzDiskDiskEncrytionKey ...
  $disk.EncryptionSettingsCollection.EncryptionSettings

  $disk = New-AzDisk ... | Set-AzDiskKeyEncrytionKey ...
  $disk.EncryptionSettingsCollection.EncryptionSettings

  $update = New-AzDiskUpdateConfig | Set-AzDiskUpdateDiskEncryptionKey ...
  $update.EncryptionSettingsCollection.EncryptionSettings

  $update = New-AzDiskUpdateConfig | Set-AzDiskUpdateKeyEncryptionKey ...
  $update.EncryptionSettingsCollection.EncryptionSettings
  ```

- Dodano właściwość ```EncryptionSettingsCollection``` w celu objęcia właściwości `EncryptionSettings` w klasie `PSSnapshot`

  #### <a name="before"></a>Przed

  ```powershell
  $snap = New-AzSnapshotConfig ... | Set-AzSnapshotDiskEncryptionKey ...
  $snap.EncryptionSettings

  $snap = New-AzSnapshotConfig ... | Set-AzSnapshotKeyEncryptionKey ...
  $snap.EncryptionSettings

  $update = New-AzSnapshotUpdateConfig ... | Set-AzSnapshotUpdateDiskEncryptionKey ...
  $update.EncryptionSettings

  $update = New-AzSnapshotUpdateConfig ... | Set-AzSnapshotUpdateKeyEncryptionKey ...
  $update.EncryptionSettings
  ```

  #### <a name="after"></a>Po

  ```powershell
  $snap = New-AzSnapshotConfig ... | Set-AzSnapshotDiskEncryptionKey ...
  $snap.EncryptionSettingsCollection.EncryptionSettings

  $snap = New-AzSnapshotConfig ... | Set-AzSnapshotKeyEncryptionKey ...
  $snap.EncryptionSettingsCollection.EncryptionSettings

  $update = New-AzSnapshotUpdateConfig ... | Set-AzSnapshotUpdateDiskEncryptionKey ...
  $update.EncryptionSettingsCollection.EncryptionSettings

  $update = New-AzSnapshotUpdateConfig ... | Set-AzSnapshotUpdateKeyEncryptionKey ...
  $update.EncryptionSettingsCollection.EncryptionSettings
  ```

- Usunięto właściwość `VirtualMachineProfile` z klasy `PSVirtualMachineScaleSet`

  #### <a name="before"></a>Przed

  ```powershell
  $vmss = New-AzVMSSConfig ...
  $vmss.VirtualMachineProfile.AdditionalCapabilities.UltraSSDEnabled = $true
  ```

  #### <a name="after"></a>Po

  ```powershell
  $vmss = New-AzVMSSConfig ...
  $vmss.AdditionalCapabilities.UltraSSDEnabled = $true
  ```

- W przypadku polecenia cmdlet `Set-AzVMBootDiagnostic` usunięto alias polecenia cmdlet `Set-AzVMBootDiagnostics`

  #### <a name="before"></a>Przed

  Użycie przestarzałego aliasu

  ```powershell
  Set-AzVMBootDiagnostics
  ```

  #### <a name="after"></a>Po

  ```powershell
  Set-AzVMBootDIagnostic
  ```

- W przypadku polecenia cmdlet `Export-AzLogAnalyticThrottledRequest` usunięto alias polecenia cmdlet `Export-AzLogAnalyticThrottledRequests`

  #### <a name="before"></a>Przed

  Użycie przestarzałego aliasu

  ```powershell
  Export-AzLogAnalyticThrottledRequests
  ```

  #### <a name="after"></a>Po

  ```powershell
  Export-AzLogAnalyticThrottledRequest
  ```

### <a name="azhdinsight"></a>Az.HDInsight

- Usunięto polecenia cmdlet `Grant-AzHDInsightHttpServicesAccess` i `Revoke-AzHDInsightHttpServicesAccess`. Nie są one już potrzebne, ponieważ dostęp HTTP jest zawsze włączony na wszystkich klastrach HDInsight.
- Dodano nowe polecenie cmdlet `Set-AzHDInsightGatewayCredential`. Za pomocą tego polecenia cmdlet można zmienić nazwę i hasło użytkownika HTTP bramy (zastępuje polecenie cmdlet `Grant-AzHDInsightHttpServicesAccess`).
- Zaktualizowano polecenie cmdlet `Get-AzHDInsightJobOutput` tak, aby obsługiwało szczegółowy dostęp na podstawie ról do klucza magazynu.
    - Nie ma to wpływu na użytkowników mających rolę Operator, Współautor lub Właściciel w klastrze usługi HDInsight.
    - Użytkownicy mający tylko rolę Czytelnik będą musieli jawnie określać parametr `DefaultStorageAccountKey`.

Aby uzyskać więcej informacji o tych zmianach dostępu na podstawie ról, zobacz [aka.ms/hdi-config-update](https://aka.ms/hdi-config-update)

  #### <a name="before"></a>Przed

  ```powershell
  Grant-AzHDInsightHttpServicesAccess -ClusterName $cluster -HttpCredential $credential
  ```

  #### <a name="after"></a>Po

  ```powershell
  Set-AzHDInsightGatewayCredential -ClusterName $cluster -HttpCredential $credential
  ```

###  <a name="users-with-only-reader-role-for-cmdlet-get-azhdinsightjoboutput"></a>Polecenie cmdlet Get-AzHDInsightJobOutput w przypadku użytkowników mających tylko rolę Czytelnik

  ####  <a name="before"></a>Przed

  ```powershell
  Get-AzHDInsightJobOutput  -ClusterName $clusterName -JobId $jobId
  ```

  #### <a name="after"></a>Po

  ```powershell
  Get-AzHDInsightJobOutput  -ClusterName $clusterName -JobId $jobId -DefaultStorageAccountKey $storageAccountKey
  ```

### <a name="azstorage"></a>Az.Storage

- Przestrzenie nazw dla typów zwracanych przez polecenia cmdlet Blob, Queue i File zostały zmienione z `Microsoft.WindowsAzure.Storage` na `Microsoft.Azure.Storage`.  Chociaż w zasadzie nie jest to zmiana powodująca niezgodność zgodnie z zasadami zmian powodujących niezgodność, może spowodować konieczność wprowadzenia pewnych zmian w kodzie, który używa metod z zestawu .Net SDK magazynu do interakcji z obiektami zwracanymi przez te polecenia cmdlet.

  #### <a name="example-1--add-a-message-to-a-queue-change-cloudqueuemessage-object-namespace"></a>Przykład 1:  Dodawanie komunikatu do kolejki (zmiana przestrzeni nazw obiektu CloudQueueMessage)

  Przed: 

  ```powershell
  $queue = Get-AzStorageQueue –Name $queueName –Context $ctx
  $queueMessage = New-Object -TypeName "Microsoft.WindowsAzure.Storage.Queue.CloudQueueMessage,$($queue.CloudQueue.GetType().Assembly.FullName)" -ArgumentList "This is message 1"
  $queue.CloudQueue.AddMessageAsync($QueueMessage)
  ```

  Po:

  ```powershell
  $queue = Get-AzStorageQueue –Name $queueName –Context $ctx
  $queueMessage = New-Object -TypeName "Microsoft.Azure.Storage.Queue.CloudQueueMessage,$($queue.CloudQueue.GetType().Assembly.FullName)"  -ArgumentList "This is message 1"
  $queue.CloudQueue.AddMessageAsync($QueueMessage)
  ```

  #### <a name="example-2--fetch-blobfile-attributes-with-accesscondition-change-accesscondition-object-namespace"></a>Przykład 2:  Pobieranie atrybutów obiektu blob/pliku przy użyciu obiektu AccessCondition (zmiana przestrzeni nazw obiektu AccessCondition)

  Przed: 

  ```powershell
  $accessCondition= New-Object Microsoft.WindowsAzure.Storage.AccessCondition

  $blob = Get-AzureStorageBlob -Container $containerName -Blob $blobName
  $blob.ICloudBlob.FetchAttributes($accessCondition)

  $file = Get-AzureStorageFile -ShareName $shareName -Path $filepath
  $file.FetchAttributes($accessCondition)
  ```

  Po:

  ```powershell
  $accessCondition= New-Object Microsoft.Azure.Storage.AccessCondition

  $blob = Get-AzureStorageBlob -Container $containerName -Blob $blobName
  $blob.ICloudBlob.FetchAttributes($accessCondition)

  $file = Get-AzureStorageFile -ShareName $shareName -Path $filepath
  $file.FetchAttributes($accessCondition)
  ```

- Chociaż w zasadzie nie jest to zmiana powodująca niezgodność, zauważysz następujące różnice w danych wyjściowych właściwości Sku.Name kont magazynu zwracanych przez polecenie `New/Get/Set-AzStorageAccount`. (Po zmianie wyjściowa i wejściowa wartość SkuName będą zgodne).
  - „StandardLRS” -> „Standard_LRS”;
  - „StandardGRS” -> „Standard_GRS”;
  - „StandardRAGRS” -> „Standard_RAGRS”;
  - „StandardZRS” -> „Standard_ZRS”;
  - „PremiumLRS” -> „Premium_LRS”;

- Zmieniono domyślne zachowanie usługi podczas tworzenia konta magazynu bez określania rodzaju.  W poprzednich wersjach, gdy konto magazynu zostało utworzone bez określenia parametru `Kind`, używany był rodzaj konta magazynu `Storage`. W nowej wersji `StorageV2` to wartość domyślna parametru `Kind`. Jeśli chcesz utworzyć konto magazynu w wersji 1 o rodzaju „Storage”, dodaj parametr „-Kind Storage”

  #### <a name="example--create-a-storage-account-default-kind-change"></a>Przykład: Tworzenie konta magazynu (zmiana domyślnego rodzaju)  

  Przed:

  ```powershell
  PS c:\> New-AzStorageAccount -ResourceGroupName groupname -Name accountname -SkuName Standard_LRS -Location "westus"

  StorageAccountName ResourceGroupName Location SkuName     Kind      AccessTier CreationTime          ProvisioningState EnableHttpsTrafficOnly
  ------------------ ----------------- -------- -------     ----      ---------- ------------          ----------------- ----------------------
  accountname        groupname         westus   StandardLRS Storage   Hot        4/17/2018 10:34:32 AM Succeeded         False
  ```

  Po:

  ```powershell
  PS c:\> New-AzStorageAccount -ResourceGroupName groupname -Name accountname -SkuName Standard_LRS -Location "westus"

  StorageAccountName ResourceGroupName Location SkuName      Kind      AccessTier CreationTime          ProvisioningState EnableHttpsTrafficOnly
  ------------------ ----------------- -------- -------      ----      ----------  ------------          ----------------- ----------------------
  accountname        groupname         westus   Standard_LRS StorageV2 Hot        4/17/2018 10:34:32 AM Succeeded         False
  ```
