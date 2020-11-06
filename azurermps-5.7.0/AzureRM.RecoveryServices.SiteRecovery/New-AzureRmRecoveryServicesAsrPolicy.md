---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 691c1d822df332bb9a3e89b218ed2c7ba1166f38
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526654"
---
# <span data-ttu-id="8e5cb-101">New-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="8e5cb-101">New-AzureRmRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="8e5cb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8e5cb-102">SYNOPSIS</span></span>
<span data-ttu-id="8e5cb-103">Tworzy zasady replikacji odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8e5cb-103">Creates an Azure Site Recovery replication policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8e5cb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8e5cb-104">SYNTAX</span></span>

### <span data-ttu-id="8e5cb-105">HyperVToAzure (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8e5cb-105">HyperVToAzure (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrPolicy [-HyperVToAzure] -Name <String> -ReplicationProvider <String>
 -ReplicationFrequencyInSeconds <String> [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>]
 [-RecoveryAzureStorageAccountId <String>] [-Encryption <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e5cb-106">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="8e5cb-106">VMwareToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrPolicy [-VMwareToAzure] -Name <String> -RecoveryPointRetentionInHours <Int32>
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-MultiVmSyncStatus <String>]
 -RPOWarningThresholdInMinutes <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8e5cb-107">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="8e5cb-107">AzureToVMware</span></span>
```
New-AzureRmRecoveryServicesAsrPolicy [-AzureToVMware] -Name <String> -RecoveryPointRetentionInHours <Int32>
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-MultiVmSyncStatus <String>]
 -RPOWarningThresholdInMinutes <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8e5cb-108">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="8e5cb-108">AzureToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrPolicy [-AzureToAzure] -Name <String> -RecoveryPointRetentionInHours <Int32>
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-MultiVmSyncStatus <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e5cb-109">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="8e5cb-109">EnterpriseToEnterprise</span></span>
```
New-AzureRmRecoveryServicesAsrPolicy [-VmmToVmm] -Name <String> -ReplicationProvider <String>
 [-ReplicationMethod <String>] -ReplicationFrequencyInSeconds <String>
 [-NumberOfRecoveryPointsToRetain <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-Compression <String>] -ReplicationPort <UInt16> [-Authentication <String>]
 [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e5cb-110">Opis</span><span class="sxs-lookup"><span data-stu-id="8e5cb-110">DESCRIPTION</span></span>
<span data-ttu-id="8e5cb-111">Polecenie cmdlet **New-AzureRmRecoveryServicesAsrPolicy** tworzy zasady replikacji odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8e5cb-111">The **New-AzureRmRecoveryServicesAsrPolicy** cmdlet creates an Azure Site Recovery replication policy.</span></span>
<span data-ttu-id="8e5cb-112">Zasady replikacji są używane do określania ustawień replikacji, takich jak częstotliwość replikacji i liczba punktów odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="8e5cb-112">The replication policy is used to specify replication settings such as the replication frequency and number of recovery points.</span></span>

## <span data-ttu-id="8e5cb-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8e5cb-113">EXAMPLES</span></span>

### <span data-ttu-id="8e5cb-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8e5cb-114">Example 1</span></span>
```
PS C:\> New-AzureRmRecoveryServicesAsrPolicy -Name "abc" -ReplicationProvider HyperVReplicaAzure -ReplicationFrequencyInSeconds 30 -NumberOfRecoveryPointsToRetain 10
```

<span data-ttu-id="8e5cb-115">Rozpoczyna operację tworzenia zasad replikacji przy użyciu określonych parametrów i zwraca zadanie ASR używane do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="8e5cb-115">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="8e5cb-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="8e5cb-116">Example 2</span></span>
```
PS C:\> New-AzureRmRecoveryServicesAsrPolicy -Name "abc122" -ReplicationProvider HyperVReplica2012R2 -ReplicationFrequencyInSeconds 300 -ReplicationPort 211

Name             : 1c609a5b-324e-461c-866f-ad58f944df25
ID               : /Subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationJobs/1c609a5b-324e-461c-866f-ad58f944df25
Type             :
JobType          : AddProtectionProfile
DisplayName      : Create replication policy
ClientRequestId  : b10c83ee-fee2-42d4-ad1d-dfc3e166faab ActivityId: 67e8453c-fae0-465f-801c-dfa2e6e6ee23
State            : Succeeded
StateDescription : Completed
StartTime        : 8/29/2017 10:18:10 AM
EndTime          : 8/29/2017 10:18:11 AM
TargetObjectId   : bb8e8c57-221d-5668-9d82-b15a3e19a6a3
TargetObjectType : ProtectionProfile
TargetObjectName : abc122
AllowedActions   :
Tasks            : {Prerequisites check for creating the replication policy, Creating the replication policy}
Errors           : {}
```

<span data-ttu-id="8e5cb-117">Rozpoczyna operację tworzenia zasad replikacji przy użyciu określonych parametrów i zwraca zadanie ASR używane do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="8e5cb-117">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="8e5cb-118">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="8e5cb-118">Example 3</span></span>
```
PS C:\> New-AzureRmRecoveryServicesAsrPolicy -Name $policyName1 -ReplicationProvider InMageAzureV2 -RecoveryPoints 40  -RPOWarningThresholdInMinutes 5 -ApplicationConsistentSnapshotFrequencyInMinutes 15
Name             : ed69e451-878b-4f19-9c0f-73184be05eaf
ID               : /Subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationJobs/ed69e451-878b-4f19-9c0f-73184be05eaf
Type             :
JobType          :
DisplayName      :
ClientRequestId  : d8922fa2-303c-4eb4-b556-e07969ea6fba ActivityId: 9e946cdf-2351-44c2-9aef-70ef2eab29b4
State            : NotStarted
StateDescription : NotStarted
StartTime        :
EndTime          :
TargetObjectId   :
TargetObjectType :
TargetObjectName :
AllowedActions   :
Tasks            : {}
Errors           : {}
```

### <span data-ttu-id="8e5cb-119">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="8e5cb-119">Example 4</span></span>
```
PS C:\>  $Job = New-AzureRmRecoveryServicesAsrPolicy -Name $TestPolicy1 -AzureToAzure -RecoveryPointRetentionInHours 10  -ApplicationConsistentSnapshotFrequencyInHours 5 
PS C:\>  Get-AsrJob -name $Job.id
```

<span data-ttu-id="8e5cb-120">Rozpoczyna operację tworzenia zasad replikacji przy użyciu określonych parametrów i zwraca zadanie ASR używane do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="8e5cb-120">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="8e5cb-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8e5cb-121">PARAMETERS</span></span>

### <span data-ttu-id="8e5cb-122">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="8e5cb-122">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="8e5cb-123">Określa częstotliwość (w godzinach) tworzenia spójnych punktów odzyskiwania aplikacji.</span><span class="sxs-lookup"><span data-stu-id="8e5cb-123">Specifies the frequency(in hours) at which to create application consistent recovery points.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e5cb-124">— Uwierzytelnianie</span><span class="sxs-lookup"><span data-stu-id="8e5cb-124">-Authentication</span></span>
<span data-ttu-id="8e5cb-125">Określa typ użytego uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="8e5cb-125">Specifies the type of authentication used.</span></span>
<span data-ttu-id="8e5cb-126">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="8e5cb-126">Valid values are:</span></span>

- <span data-ttu-id="8e5cb-127">Dyplom</span><span class="sxs-lookup"><span data-stu-id="8e5cb-127">Certificate</span></span>
-  <span data-ttu-id="8e5cb-128">Mechanizmu</span><span class="sxs-lookup"><span data-stu-id="8e5cb-128">Kerberos</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise
Aliases:
Accepted values: Certificate, Kerberos

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e5cb-129">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="8e5cb-129">-AzureToAzure</span></span>
<span data-ttu-id="8e5cb-130">Parametr Switch określający, że tworzone zasady replikacji będą używane do replikowania maszyn wirtualnych platformy Azure między dwoma regionami platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8e5cb-130">Switch parameter specifying that the replication policy being created will be used to replicated Azure virtual machines between two Azure regions.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e5cb-131">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="8e5cb-131">-AzureToVMware</span></span>
<span data-ttu-id="8e5cb-132">Parametr Switch wskazujący, że tworzone zasady replikacji będą używane do wycofywania replikacji na maszynach wirtualnych VMware i serwerach fizycznych uruchomionych na platformie Azure z powrotem do lokalnej witryny programu VMware.</span><span class="sxs-lookup"><span data-stu-id="8e5cb-132">Switch parameter specifying that the replication policy being created will be used to reverse replicate failed over VMware virtual machines and Physical servers running in Azure back to an on-premises VMware site.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AzureToVMware
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e5cb-133">-Compression</span><span class="sxs-lookup"><span data-stu-id="8e5cb-133">-Compression</span></span>
<span data-ttu-id="8e5cb-134">Określa, czy kompresja powinna być włączona.</span><span class="sxs-lookup"><span data-stu-id="8e5cb-134">Specifies if compression should be enabled.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e5cb-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8e5cb-135">-Confirm</span></span>
<span data-ttu-id="8e5cb-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e5cb-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e5cb-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e5cb-137">-DefaultProfile</span></span>
<span data-ttu-id="8e5cb-138">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8e5cb-138">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e5cb-139">— Szyfrowanie</span><span class="sxs-lookup"><span data-stu-id="8e5cb-139">-Encryption</span></span>
<span data-ttu-id="8e5cb-140">Określa, czy szyfrowanie ma być włączone, czy wyłączone.</span><span class="sxs-lookup"><span data-stu-id="8e5cb-140">Specifies if encryption should be enabled or disabled.</span></span>

```yaml
Type: String
Parameter Sets: HyperVToAzure
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e5cb-141">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="8e5cb-141">-HyperVToAzure</span></span>
<span data-ttu-id="8e5cb-142">Parametr Przełącz określający zasady do replikowania maszyn wirtualnych funkcji Hyper-V na platformie Azure</span><span class="sxs-lookup"><span data-stu-id="8e5cb-142">Switch parameter to specify policy is to be used to replicate Hyper-V virtual machines to Azure</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: HyperVToAzure
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e5cb-143">-MultiVmSyncStatus</span><span class="sxs-lookup"><span data-stu-id="8e5cb-143">-MultiVmSyncStatus</span></span>
<span data-ttu-id="8e5cb-144">Określa stan synchronizacji multiVm dla zasad.</span><span class="sxs-lookup"><span data-stu-id="8e5cb-144">Specifies multiVm sync status for the policy.</span></span>

```yaml
Type: String
Parameter Sets: VMwareToAzure, AzureToVMware, AzureToAzure
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e5cb-145">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8e5cb-145">-Name</span></span>
<span data-ttu-id="8e5cb-146">Określa nazwę zasad replikacji ASR.</span><span class="sxs-lookup"><span data-stu-id="8e5cb-146">Specifies the name of the ASR replication policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e5cb-147">-NumberOfRecoveryPointsToRetain</span><span class="sxs-lookup"><span data-stu-id="8e5cb-147">-NumberOfRecoveryPointsToRetain</span></span>
<span data-ttu-id="8e5cb-148">Określa punkty odzyskiwania liczb, które mają zostać zachowane.</span><span class="sxs-lookup"><span data-stu-id="8e5cb-148">Specifies the number recovery points to retain.</span></span>

```yaml
Type: Int32
Parameter Sets: HyperVToAzure, EnterpriseToEnterprise
Aliases: RecoveryPoints

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e5cb-149">-RPOWarningThresholdInMinutes</span><span class="sxs-lookup"><span data-stu-id="8e5cb-149">-RPOWarningThresholdInMinutes</span></span>
<span data-ttu-id="8e5cb-150">Wartość progowa punktu odzyskiwania w minutach, w którym należy ostrzec.</span><span class="sxs-lookup"><span data-stu-id="8e5cb-150">The RPO threshold value in minutes to warn on.</span></span>

```yaml
Type: Int32
Parameter Sets: VMwareToAzure, AzureToVMware
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e5cb-151">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="8e5cb-151">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="8e5cb-152">Określa identyfikator konta usługi Azure Storage, do którego mają być replikowane dane.</span><span class="sxs-lookup"><span data-stu-id="8e5cb-152">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: String
Parameter Sets: HyperVToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e5cb-153">-RecoveryPointRetentionInHours</span><span class="sxs-lookup"><span data-stu-id="8e5cb-153">-RecoveryPointRetentionInHours</span></span>
<span data-ttu-id="8e5cb-154">Zachowanie punktów odzyskiwania dla danego czasu w godzinach.</span><span class="sxs-lookup"><span data-stu-id="8e5cb-154">Retain the recovery points for given time in hours.</span></span>

```yaml
Type: Int32
Parameter Sets: VMwareToAzure, AzureToVMware, AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e5cb-155">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="8e5cb-155">-ReplicaDeletion</span></span>
<span data-ttu-id="8e5cb-156">Określa, czy maszyna wirtualna repliki ma zostać usunięta podczas wyłączania replikacji z witryny zarządzanej programu VMM do innej.</span><span class="sxs-lookup"><span data-stu-id="8e5cb-156">Specifies if the replica virtual machine should be deleted on disabling replication from a VMM managed site to another.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise
Aliases:
Accepted values: Required, NotRequired

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e5cb-157">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="8e5cb-157">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="8e5cb-158">Określa interwał częstotliwości replikacji w sekundach.</span><span class="sxs-lookup"><span data-stu-id="8e5cb-158">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="8e5cb-159">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="8e5cb-159">Valid values are:</span></span>

- <span data-ttu-id="8e5cb-160">30</span><span class="sxs-lookup"><span data-stu-id="8e5cb-160">30</span></span>
- <span data-ttu-id="8e5cb-161">300</span><span class="sxs-lookup"><span data-stu-id="8e5cb-161">300</span></span>
- <span data-ttu-id="8e5cb-162">900</span><span class="sxs-lookup"><span data-stu-id="8e5cb-162">900</span></span>

```yaml
Type: String
Parameter Sets: HyperVToAzure, EnterpriseToEnterprise
Aliases:
Accepted values: 30, 300, 900

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e5cb-163">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="8e5cb-163">-ReplicationMethod</span></span>
<span data-ttu-id="8e5cb-164">Określa metodę replikacji.</span><span class="sxs-lookup"><span data-stu-id="8e5cb-164">Specifies the replication method.</span></span>
<span data-ttu-id="8e5cb-165">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="8e5cb-165">Valid values are:</span></span>

- <span data-ttu-id="8e5cb-166">Ekran</span><span class="sxs-lookup"><span data-stu-id="8e5cb-166">Online</span></span>
- <span data-ttu-id="8e5cb-167">Pracy</span><span class="sxs-lookup"><span data-stu-id="8e5cb-167">Offline</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise
Aliases:
Accepted values: Online, Offline

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e5cb-168">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="8e5cb-168">-ReplicationPort</span></span>
<span data-ttu-id="8e5cb-169">Określa port wykorzystywany do replikacji.</span><span class="sxs-lookup"><span data-stu-id="8e5cb-169">Specifies the port used for replication.</span></span>

```yaml
Type: UInt16
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e5cb-170">-ReplicationProvider</span><span class="sxs-lookup"><span data-stu-id="8e5cb-170">-ReplicationProvider</span></span>
<span data-ttu-id="8e5cb-171">Określa dostawcę replikacji dla zasad.</span><span class="sxs-lookup"><span data-stu-id="8e5cb-171">Specifies the replication provider for the policy.</span></span>

```yaml
Type: String
Parameter Sets: HyperVToAzure, EnterpriseToEnterprise
Aliases:
Accepted values: HyperVReplica2012R2, HyperVReplica2012, HyperVReplicaAzure

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e5cb-172">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="8e5cb-172">-ReplicationStartTime</span></span>
<span data-ttu-id="8e5cb-173">Określa czas rozpoczęcia replikacji.</span><span class="sxs-lookup"><span data-stu-id="8e5cb-173">Specifies the replication start time.</span></span>
<span data-ttu-id="8e5cb-174">Od początku zadania nie może on być późniejszy niż 24 godziny.</span><span class="sxs-lookup"><span data-stu-id="8e5cb-174">It must be no later than 24-hours from the start of the job.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: HyperVToAzure, EnterpriseToEnterprise
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e5cb-175">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="8e5cb-175">-VMwareToAzure</span></span>
<span data-ttu-id="8e5cb-176">Parametr Switch określający, że tworzone zasady replikacji będą używane do replikowania maszyn wirtualnych VMware i/lub fizycznych serwerów na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="8e5cb-176">Switch parameter specifying that the replication policy being created will be used to replicate VMware virtual machines and/or Physical servers to Azure.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: VMwareToAzure
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e5cb-177">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="8e5cb-177">-VmmToVmm</span></span>
<span data-ttu-id="8e5cb-178">Parametr Przełącz określający zasady do replikowania między witrynami funkcji Hyper-V zarządzanych przez serwer programu VMM.</span><span class="sxs-lookup"><span data-stu-id="8e5cb-178">Switch parameter to specify policy is to be used to replicate between Hyper-V sites managed by a VMM server.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e5cb-179">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e5cb-179">-WhatIf</span></span>
<span data-ttu-id="8e5cb-180">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e5cb-180">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8e5cb-181">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8e5cb-181">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e5cb-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e5cb-182">CommonParameters</span></span>
<span data-ttu-id="8e5cb-183">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e5cb-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e5cb-184">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e5cb-184">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e5cb-185">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8e5cb-185">INPUTS</span></span>

### <span data-ttu-id="8e5cb-186">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="8e5cb-186">None</span></span>

## <span data-ttu-id="8e5cb-187">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8e5cb-187">OUTPUTS</span></span>

### <span data-ttu-id="8e5cb-188">System. Object</span><span class="sxs-lookup"><span data-stu-id="8e5cb-188">System.Object</span></span>

## <span data-ttu-id="8e5cb-189">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8e5cb-189">NOTES</span></span>

## <span data-ttu-id="8e5cb-190">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8e5cb-190">RELATED LINKS</span></span>

[<span data-ttu-id="8e5cb-191">Get-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="8e5cb-191">Get-AzureRmRecoveryServicesAsrPolicy</span></span>](./Get-AzureRmRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="8e5cb-192">Remove-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="8e5cb-192">Remove-AzureRmRecoveryServicesAsrPolicy</span></span>](./Remove-AzureRmRecoveryServicesAsrPolicy.md)
