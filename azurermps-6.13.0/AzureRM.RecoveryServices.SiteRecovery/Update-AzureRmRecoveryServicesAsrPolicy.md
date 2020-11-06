---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/update-azurermrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 805e421aedbb06b6f9a821b3f575b8a5035c86d9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526102"
---
# <span data-ttu-id="8ab6d-101">Update-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="8ab6d-101">Update-AzureRmRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="8ab6d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8ab6d-102">SYNOPSIS</span></span>
<span data-ttu-id="8ab6d-103">Aktualizuje zasady replikacji odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8ab6d-103">Updates an Azure Site Recovery replication policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8ab6d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8ab6d-104">SYNTAX</span></span>

### <span data-ttu-id="8ab6d-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="8ab6d-105">Default (Default)</span></span>
```
Update-AzureRmRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-ReplicationMethod <String>]
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] [-ReplicationPort <UInt16>]
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-RecoveryAzureStorageAccountId <String>] [-Encryption <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ab6d-106">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="8ab6d-106">VMwareToAzure</span></span>
```
Update-AzureRmRecoveryServicesAsrPolicy [-VMwareToAzure] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-RPOWarningThresholdInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ab6d-107">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="8ab6d-107">AzureToAzure</span></span>
```
Update-AzureRmRecoveryServicesAsrPolicy [-AzureToAzure] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8ab6d-108">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="8ab6d-108">AzureToVMware</span></span>
```
Update-AzureRmRecoveryServicesAsrPolicy [-AzureToVMware] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-RPOWarningThresholdInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ab6d-109">HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="8ab6d-109">HyperVToAzure</span></span>
```
Update-AzureRmRecoveryServicesAsrPolicy [-HyperVToAzure] -InputObject <ASRPolicy>
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>]
 [-RecoveryAzureStorageAccountId <String>] [-Encryption <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ab6d-110">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="8ab6d-110">EnterpriseToEnterprise</span></span>
```
Update-AzureRmRecoveryServicesAsrPolicy [-VmmToVmm] -InputObject <ASRPolicy> [-ReplicationMethod <String>]
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] [-ReplicationPort <UInt16>]
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ab6d-111">Opis</span><span class="sxs-lookup"><span data-stu-id="8ab6d-111">DESCRIPTION</span></span>
<span data-ttu-id="8ab6d-112">Polecenie cmdlet **Update-AzureRmRecoveryServicesAsrPolicy** aktualizuje określone zasady replikacji odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8ab6d-112">The **Update-AzureRmRecoveryServicesAsrPolicy** cmdlet updates the specified Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="8ab6d-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8ab6d-113">EXAMPLES</span></span>

### <span data-ttu-id="8ab6d-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8ab6d-114">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrPolicy -Policy $Policy -ReplicationFrequencyInSeconds 900
```

<span data-ttu-id="8ab6d-115">Rozpoczyna operację aktualizowania zasad replikacji przy użyciu określonych parametrów i zwraca zadanie ASR używane do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="8ab6d-115">Starts the update replication policy operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="8ab6d-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="8ab6d-116">Example 2</span></span>
```
PS C:\> Update-AzureRmRecoveryServicesAsrPolicy -AzureToAzure -InputObject $Policy -ReplicationFrequencyInSeconds 900
```

<span data-ttu-id="8ab6d-117">Rozpoczyna operację aktualizowania zasad replikacji platformy Azure do platformy Azure przy użyciu określonych parametrów i zwraca zadanie ASR używane do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="8ab6d-117">Starts the update azure to azure replication policy operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="8ab6d-118">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="8ab6d-118">Example 3</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrPolicy -AzureToAzure -InputObject $Policy -RecoveryPointRetentionInHours 20
```

<span data-ttu-id="8ab6d-119">Uruchamia zasady replikacji usługi Azure to Azure przy użyciu określonych parametrów i zwraca zadanie ASR używane do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="8ab6d-119">Starts the update azure to azure replication policy using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="8ab6d-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8ab6d-120">PARAMETERS</span></span>

### <span data-ttu-id="8ab6d-121">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="8ab6d-121">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="8ab6d-122">Określa częstotliwość (w godzinach) tworzenia spójnych punktów odzyskiwania aplikacji.</span><span class="sxs-lookup"><span data-stu-id="8ab6d-122">Specifies the frequency(in hours) at which to create application consistent recovery points.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ab6d-123">— Uwierzytelnianie</span><span class="sxs-lookup"><span data-stu-id="8ab6d-123">-Authentication</span></span>
<span data-ttu-id="8ab6d-124">Określa typ użytego uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="8ab6d-124">Specifies the type of authentication used.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:
Accepted values: Certificate, Kerberos

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ab6d-125">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="8ab6d-125">-AzureToAzure</span></span>
<span data-ttu-id="8ab6d-126">Parametr Switch określający, że zasady replikacji używane do replikowania maszyn wirtualnych platformy Azure między dwoma regionami Azure zostaną zaktualizowane.</span><span class="sxs-lookup"><span data-stu-id="8ab6d-126">Switch parameter specifying that the replication policy used to replicate Azure virtual machines between two Azure regions will be updated.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ab6d-127">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="8ab6d-127">-AzureToVMware</span></span>
<span data-ttu-id="8ab6d-128">Parametr Switch wskazujący, że zasady specfied są używane do replikowania niepowodzeniem na maszynach wirtualnych uruchomionych na platformie Azure z powrotem do lokalnej witryny programu VMware.</span><span class="sxs-lookup"><span data-stu-id="8ab6d-128">Switch parameter indicating that the specfied policy is used to replicate failed over virtual machines running in Azure back to an on-premises VMware site.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToVMware
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ab6d-129">-Compression</span><span class="sxs-lookup"><span data-stu-id="8ab6d-129">-Compression</span></span>
<span data-ttu-id="8ab6d-130">Określa, czy kompresja powinna być włączona.</span><span class="sxs-lookup"><span data-stu-id="8ab6d-130">Specifies if compression should be enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ab6d-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ab6d-131">-DefaultProfile</span></span>
<span data-ttu-id="8ab6d-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8ab6d-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="8ab6d-133">— Szyfrowanie</span><span class="sxs-lookup"><span data-stu-id="8ab6d-133">-Encryption</span></span>
<span data-ttu-id="8ab6d-134">{{Opis szyfrowania wypełniania}}</span><span class="sxs-lookup"><span data-stu-id="8ab6d-134">{{Fill Encryption Description}}</span></span>

```yaml
Type: System.String
Parameter Sets: Default, HyperVToAzure
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ab6d-135">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="8ab6d-135">-HyperVToAzure</span></span>
<span data-ttu-id="8ab6d-136">Parametr Switch wskazujący, że zasady specfied są używane do replikowania maszyn wirtualnych funkcji Hyper-V na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="8ab6d-136">Switch parameter indicating that the specfied policy is used to replicate Hyper-V virtual machines to Azure.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: HyperVToAzure
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ab6d-137">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8ab6d-137">-InputObject</span></span>
<span data-ttu-id="8ab6d-138">Obiekt wejściowy polecenia cmdlet: określa obiekt zasad replikacji ASR odpowiadający zasadom replikacji, które mają zostać zaktualizowane.</span><span class="sxs-lookup"><span data-stu-id="8ab6d-138">Input object for the cmdlet: Specifies the ASR replication policy object corresponding to the replication policy to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy
Parameter Sets: (All)
Aliases: Policy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8ab6d-139">-MultiVmSyncStatus</span><span class="sxs-lookup"><span data-stu-id="8ab6d-139">-MultiVmSyncStatus</span></span>
<span data-ttu-id="8ab6d-140">Określa stan synchronizacji multiVm dla zasad.</span><span class="sxs-lookup"><span data-stu-id="8ab6d-140">Specifies multiVm sync status for the policy.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, AzureToAzure, AzureToVMware
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ab6d-141">-NumberOfRecoveryPointsToRetain</span><span class="sxs-lookup"><span data-stu-id="8ab6d-141">-NumberOfRecoveryPointsToRetain</span></span>
<span data-ttu-id="8ab6d-142">Określa punkty odzyskiwania liczb, które mają zostać zachowane.</span><span class="sxs-lookup"><span data-stu-id="8ab6d-142">Specifies the number recovery points to retain.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Default, HyperVToAzure, EnterpriseToEnterprise
Aliases: RecoveryPoints

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ab6d-143">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="8ab6d-143">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="8ab6d-144">Określa identyfikator konta usługi Azure Storage dla lokalizacji docelowej replikacji.</span><span class="sxs-lookup"><span data-stu-id="8ab6d-144">Specifies the Azure storage account ID of the replication target.</span></span> <span data-ttu-id="8ab6d-145">Używane jako docelowe konto magazynu do replikacji, jeśli nie podano elementu alternatywnego podczas włączania replikacji przy użyciu polecenia cmdlet New-AzureRmRecoveryServicesASRReplicationProtectedItem.</span><span class="sxs-lookup"><span data-stu-id="8ab6d-145">Used as the target storage account for replication if an alternate is not provided while enabling replication using the New-AzureRmRecoveryServicesASRReplicationProtectedItem cmdlet.</span></span>


```yaml
Type: System.String
Parameter Sets: Default, HyperVToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ab6d-146">-RecoveryPointRetentionInHours</span><span class="sxs-lookup"><span data-stu-id="8ab6d-146">-RecoveryPointRetentionInHours</span></span>
<span data-ttu-id="8ab6d-147">Czas w godzinach na zachowanie punktów odzyskiwania po utworzeniu.</span><span class="sxs-lookup"><span data-stu-id="8ab6d-147">Time in hours to retain recovery points after creation.</span></span>

```yaml
Type: System.Int32
Parameter Sets: VMwareToAzure, AzureToAzure, AzureToVMware
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ab6d-148">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="8ab6d-148">-ReplicaDeletion</span></span>
<span data-ttu-id="8ab6d-149">Określa, czy maszyna wirtualna repliki ma zostać usunięta podczas wyłączania replikacji z witryny zarządzanej programu VMM do innej.</span><span class="sxs-lookup"><span data-stu-id="8ab6d-149">Specifies if the replica virtual machine should be deleted on disabling replication from a VMM managed site to another.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:
Accepted values: Required, NotRequired

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ab6d-150">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="8ab6d-150">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="8ab6d-151">Określa interwał częstotliwości replikacji w sekundach.</span><span class="sxs-lookup"><span data-stu-id="8ab6d-151">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="8ab6d-152">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="8ab6d-152">Valid values are:</span></span>

- <span data-ttu-id="8ab6d-153">30</span><span class="sxs-lookup"><span data-stu-id="8ab6d-153">30</span></span>
- <span data-ttu-id="8ab6d-154">300</span><span class="sxs-lookup"><span data-stu-id="8ab6d-154">300</span></span>
- <span data-ttu-id="8ab6d-155">900</span><span class="sxs-lookup"><span data-stu-id="8ab6d-155">900</span></span>

```yaml
Type: System.String
Parameter Sets: Default, HyperVToAzure, EnterpriseToEnterprise
Aliases:
Accepted values: 30, 300, 900

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ab6d-156">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="8ab6d-156">-ReplicationMethod</span></span>
<span data-ttu-id="8ab6d-157">Określa metodę replikacji.</span><span class="sxs-lookup"><span data-stu-id="8ab6d-157">Specifies the replication method.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:
Accepted values: Online, Offline

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ab6d-158">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="8ab6d-158">-ReplicationPort</span></span>
<span data-ttu-id="8ab6d-159">Określa port wykorzystywany do replikacji.</span><span class="sxs-lookup"><span data-stu-id="8ab6d-159">Specifies the port used for replication.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ab6d-160">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="8ab6d-160">-ReplicationStartTime</span></span>
<span data-ttu-id="8ab6d-161">Określa czas rozpoczęcia replikacji.</span><span class="sxs-lookup"><span data-stu-id="8ab6d-161">Specifies the replication start time.</span></span>
<span data-ttu-id="8ab6d-162">Od początku zadania nie może on być późniejszy niż 24 godziny.</span><span class="sxs-lookup"><span data-stu-id="8ab6d-162">It must be no later than 24-hours from the start of the job.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: Default, HyperVToAzure, EnterpriseToEnterprise
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ab6d-163">-RPOWarningThresholdInMinutes</span><span class="sxs-lookup"><span data-stu-id="8ab6d-163">-RPOWarningThresholdInMinutes</span></span>
<span data-ttu-id="8ab6d-164">Wartość progowa punktu odzyskiwania w minutach, w którym należy ostrzec.</span><span class="sxs-lookup"><span data-stu-id="8ab6d-164">The RPO threshold value in minutes to warn on.</span></span>

```yaml
Type: System.Int32
Parameter Sets: VMwareToAzure, AzureToVMware
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ab6d-165">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="8ab6d-165">-VmmToVmm</span></span>
<span data-ttu-id="8ab6d-166">Parametr Switch wskazujący, że zasady specfied są używane do replikowania zarządzanych maszyn wirtualnych funkcji Hyper-V programu VMM między dwiema lokacjami funkcji Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="8ab6d-166">Switch parameter indicating that the specfied policy is used to replicate VMM managed Hyper-V virtual machines between two Hyper-V sites.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ab6d-167">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="8ab6d-167">-VMwareToAzure</span></span>
<span data-ttu-id="8ab6d-168">Parametr Switch wskazujący, że zasady specfied są używane do replikowania maszyn wirtualnych VMware na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="8ab6d-168">Switch parameter indicating that the specfied policy is used to replicate VMware virtual machines to Azure.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: VMwareToAzure
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ab6d-169">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8ab6d-169">-Confirm</span></span>
<span data-ttu-id="8ab6d-170">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ab6d-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ab6d-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ab6d-171">-WhatIf</span></span>
<span data-ttu-id="8ab6d-172">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ab6d-172">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8ab6d-173">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8ab6d-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ab6d-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ab6d-174">CommonParameters</span></span>
<span data-ttu-id="8ab6d-175">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ab6d-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ab6d-176">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ab6d-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ab6d-177">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8ab6d-177">INPUTS</span></span>

### <span data-ttu-id="8ab6d-178">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="8ab6d-178">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="8ab6d-179">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8ab6d-179">OUTPUTS</span></span>

### <span data-ttu-id="8ab6d-180">System. Object</span><span class="sxs-lookup"><span data-stu-id="8ab6d-180">System.Object</span></span>

## <span data-ttu-id="8ab6d-181">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8ab6d-181">NOTES</span></span>

## <span data-ttu-id="8ab6d-182">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8ab6d-182">RELATED LINKS</span></span>
