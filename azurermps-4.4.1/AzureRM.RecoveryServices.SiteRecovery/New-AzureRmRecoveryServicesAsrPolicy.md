---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: a0a55ad071a21f7924eb5a4115a7699fc6690060
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543091"
---
# <span data-ttu-id="7ab42-101">New-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="7ab42-101">New-AzureRmRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="7ab42-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7ab42-102">SYNOPSIS</span></span>
<span data-ttu-id="7ab42-103">Tworzy zasady replikacji odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7ab42-103">Creates an Azure Site Recovery replication policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7ab42-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7ab42-104">SYNTAX</span></span>

### <span data-ttu-id="7ab42-105">EnterpriseToAzure (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7ab42-105">EnterpriseToAzure (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrPolicy -Name <String> -ReplicationProvider <String>
 -ReplicationFrequencyInSeconds <String> [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>]
 [-RecoveryAzureStorageAccountId <String>] [-Encryption <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ab42-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="7ab42-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmRecoveryServicesAsrPolicy -Name <String> -ReplicationProvider <String> [-ReplicationMethod <String>]
 -ReplicationFrequencyInSeconds <String> [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] -ReplicationPort <UInt16>
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7ab42-107">Opis</span><span class="sxs-lookup"><span data-stu-id="7ab42-107">DESCRIPTION</span></span>
<span data-ttu-id="7ab42-108">Polecenie cmdlet **New-AzureRmRecoveryServicesAsrPolicy** tworzy zasady replikacji odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7ab42-108">The **New-AzureRmRecoveryServicesAsrPolicy** cmdlet creates an Azure Site Recovery replication policy.</span></span>
<span data-ttu-id="7ab42-109">Zasady replikacji są używane do określania ustawień replikacji, takich jak częstotliwość replikacji i liczba punktów odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="7ab42-109">The replication policy is used to specify replication settings such as the replication frequency and number of recovery points.</span></span>

## <span data-ttu-id="7ab42-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7ab42-110">EXAMPLES</span></span>

### <span data-ttu-id="7ab42-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7ab42-111">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name $PolicyName -Policy $ProtectionProfile -PrimaryProtectionContainer $PrimaryContainer -RecoveryProtectionContainer $RecoveryContainer
```

<span data-ttu-id="7ab42-112">Rozpoczyna operację tworzenia zasad replikacji przy użyciu określonych parametrów i zwraca zadanie ASR używane do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="7ab42-112">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="7ab42-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7ab42-113">PARAMETERS</span></span>

### <span data-ttu-id="7ab42-114">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="7ab42-114">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="7ab42-115">Określa częstotliwość (w godzinach) tworzenia spójnych punktów odzyskiwania aplikacji.</span><span class="sxs-lookup"><span data-stu-id="7ab42-115">Specifies the frequency(in hours) at which to create application consistent recovery points.</span></span>

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

### <span data-ttu-id="7ab42-116">— Uwierzytelnianie</span><span class="sxs-lookup"><span data-stu-id="7ab42-116">-Authentication</span></span>
<span data-ttu-id="7ab42-117">Określa typ użytego uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="7ab42-117">Specifies the type of authentication used.</span></span>
<span data-ttu-id="7ab42-118">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="7ab42-118">Valid values are:</span></span>

- <span data-ttu-id="7ab42-119">Dyplom</span><span class="sxs-lookup"><span data-stu-id="7ab42-119">Certificate</span></span>
-  <span data-ttu-id="7ab42-120">Mechanizmu</span><span class="sxs-lookup"><span data-stu-id="7ab42-120">Kerberos</span></span>

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

### <span data-ttu-id="7ab42-121">-Compression</span><span class="sxs-lookup"><span data-stu-id="7ab42-121">-Compression</span></span>
<span data-ttu-id="7ab42-122">Określa, czy kompresja powinna być włączona.</span><span class="sxs-lookup"><span data-stu-id="7ab42-122">Specifies if compression should be enabled.</span></span>

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

### <span data-ttu-id="7ab42-123">— Szyfrowanie</span><span class="sxs-lookup"><span data-stu-id="7ab42-123">-Encryption</span></span>
<span data-ttu-id="7ab42-124">Określa, czy szyfrowanie ma być włączone, czy wyłączone.</span><span class="sxs-lookup"><span data-stu-id="7ab42-124">Specifies if encryption should be enabled or disabled.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ab42-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7ab42-125">-Name</span></span>
<span data-ttu-id="7ab42-126">Określa nazwę zasad replikacji ASR.</span><span class="sxs-lookup"><span data-stu-id="7ab42-126">Specifies the name of the ASR replication policy.</span></span>

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

### <span data-ttu-id="7ab42-127">-NumberOfRecoveryPointsToRetain</span><span class="sxs-lookup"><span data-stu-id="7ab42-127">-NumberOfRecoveryPointsToRetain</span></span>
<span data-ttu-id="7ab42-128">Określa punkty odzyskiwania liczb, które mają zostać zachowane.</span><span class="sxs-lookup"><span data-stu-id="7ab42-128">Specifies the number recovery points to retain.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: RecoveryPoints

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ab42-129">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="7ab42-129">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="7ab42-130">Określa identyfikator konta usługi Azure Storage dla lokalizacji docelowej replikacji.</span><span class="sxs-lookup"><span data-stu-id="7ab42-130">Specifies the Azure storage account ID of the replication target.</span></span> <span data-ttu-id="7ab42-131">Używane jako docelowe konto magazynu do replikacji, jeśli nie podano elementu alternatywnego podczas włączania replikacji przy użyciu polecenia cmdlet New-AzureRmRecoveryServicesASRReplicationProtectedItem.</span><span class="sxs-lookup"><span data-stu-id="7ab42-131">Used as the target storage account for replication if an alternate is not provided while enabling replication using the New-AzureRmRecoveryServicesASRReplicationProtectedItem cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ab42-132">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="7ab42-132">-ReplicaDeletion</span></span>
<span data-ttu-id="7ab42-133">Określa, czy maszyna wirtualna repliki ma zostać usunięta podczas wyłączania replikacji z witryny zarządzanej programu VMM do innej.</span><span class="sxs-lookup"><span data-stu-id="7ab42-133">Specifies if the replica virtual machine should be deleted on disabling replication from a VMM managed site to another.</span></span>

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

### <span data-ttu-id="7ab42-134">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="7ab42-134">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="7ab42-135">Określa interwał częstotliwości replikacji w sekundach.</span><span class="sxs-lookup"><span data-stu-id="7ab42-135">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="7ab42-136">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="7ab42-136">Valid values are:</span></span>

- <span data-ttu-id="7ab42-137">30</span><span class="sxs-lookup"><span data-stu-id="7ab42-137">30</span></span>
- <span data-ttu-id="7ab42-138">300</span><span class="sxs-lookup"><span data-stu-id="7ab42-138">300</span></span>
- <span data-ttu-id="7ab42-139">900</span><span class="sxs-lookup"><span data-stu-id="7ab42-139">900</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: 30, 300, 900

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ab42-140">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="7ab42-140">-ReplicationMethod</span></span>
<span data-ttu-id="7ab42-141">Określa metodę replikacji.</span><span class="sxs-lookup"><span data-stu-id="7ab42-141">Specifies the replication method.</span></span>
<span data-ttu-id="7ab42-142">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="7ab42-142">Valid values are:</span></span>

- <span data-ttu-id="7ab42-143">Ekran</span><span class="sxs-lookup"><span data-stu-id="7ab42-143">Online</span></span>
- <span data-ttu-id="7ab42-144">Pracy</span><span class="sxs-lookup"><span data-stu-id="7ab42-144">Offline</span></span>

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

### <span data-ttu-id="7ab42-145">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="7ab42-145">-ReplicationPort</span></span>
<span data-ttu-id="7ab42-146">Określa port wykorzystywany do replikacji.</span><span class="sxs-lookup"><span data-stu-id="7ab42-146">Specifies the port used for replication.</span></span>

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

### <span data-ttu-id="7ab42-147">-ReplicationProvider</span><span class="sxs-lookup"><span data-stu-id="7ab42-147">-ReplicationProvider</span></span>
<span data-ttu-id="7ab42-148">Określa dostawcę replikacji.</span><span class="sxs-lookup"><span data-stu-id="7ab42-148">Specifies the replication provider.</span></span>
<span data-ttu-id="7ab42-149">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="7ab42-149">Valid values are:</span></span>

- <span data-ttu-id="7ab42-150">HyperVReplica2012R2</span><span class="sxs-lookup"><span data-stu-id="7ab42-150">HyperVReplica2012R2</span></span>
- <span data-ttu-id="7ab42-151">HyperVReplica2012</span><span class="sxs-lookup"><span data-stu-id="7ab42-151">HyperVReplica2012</span></span>
- <span data-ttu-id="7ab42-152">HyperVReplicaAzure</span><span class="sxs-lookup"><span data-stu-id="7ab42-152">HyperVReplicaAzure</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: HyperVReplica2012R2, HyperVReplica2012, HyperVReplicaAzure

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ab42-153">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="7ab42-153">-ReplicationStartTime</span></span>
<span data-ttu-id="7ab42-154">Określa czas rozpoczęcia replikacji.</span><span class="sxs-lookup"><span data-stu-id="7ab42-154">Specifies the replication start time.</span></span>
<span data-ttu-id="7ab42-155">Od początku zadania nie może on być późniejszy niż 24 godziny.</span><span class="sxs-lookup"><span data-stu-id="7ab42-155">It must be no later than 24-hours from the start of the job.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ab42-156">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7ab42-156">-Confirm</span></span>
<span data-ttu-id="7ab42-157">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ab42-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ab42-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ab42-158">-WhatIf</span></span>
<span data-ttu-id="7ab42-159">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ab42-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7ab42-160">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7ab42-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ab42-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ab42-161">CommonParameters</span></span>
<span data-ttu-id="7ab42-162">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ab42-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ab42-163">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ab42-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ab42-164">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7ab42-164">INPUTS</span></span>

### <span data-ttu-id="7ab42-165">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="7ab42-165">None</span></span>

## <span data-ttu-id="7ab42-166">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7ab42-166">OUTPUTS</span></span>

### <span data-ttu-id="7ab42-167">System. Object</span><span class="sxs-lookup"><span data-stu-id="7ab42-167">System.Object</span></span>

## <span data-ttu-id="7ab42-168">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7ab42-168">NOTES</span></span>

## <span data-ttu-id="7ab42-169">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7ab42-169">RELATED LINKS</span></span>

[<span data-ttu-id="7ab42-170">Get-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="7ab42-170">Get-AzureRmRecoveryServicesAsrPolicy</span></span>](./Get-AzureRmRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="7ab42-171">Remove-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="7ab42-171">Remove-AzureRmRecoveryServicesAsrPolicy</span></span>](./Remove-AzureRmRecoveryServicesAsrPolicy.md)
