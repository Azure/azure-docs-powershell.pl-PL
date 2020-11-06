---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 302b781ee6af68cb960ab01668147edc56e04284
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550820"
---
# <span data-ttu-id="3ce3b-101">Update-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="3ce3b-101">Update-AzureRmRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="3ce3b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3ce3b-102">SYNOPSIS</span></span>
<span data-ttu-id="3ce3b-103">Aktualizuje zasady replikacji odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3ce3b-103">Updates an Azure Site Recovery replication policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ce3b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3ce3b-104">SYNTAX</span></span>

```
Update-AzureRmRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-ReplicationMethod <String>]
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] [-ReplicationPort <UInt16>]
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-RecoveryAzureStorageAccountId <String>] [-Encryption <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ce3b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3ce3b-105">DESCRIPTION</span></span>
<span data-ttu-id="3ce3b-106">Polecenie cmdlet **Update-AzureRmRecoveryServicesAsrPolicy** aktualizuje określone zasady replikacji odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3ce3b-106">The **Update-AzureRmRecoveryServicesAsrPolicy** cmdlet updates the specified Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="3ce3b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3ce3b-107">EXAMPLES</span></span>

### <span data-ttu-id="3ce3b-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3ce3b-108">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrPolicy -Policy $Policy -ReplicationFrequencyInSeconds 900
```

<span data-ttu-id="3ce3b-109">Rozpoczyna operację aktualizowania zasad replikacji przy użyciu określonych parametrów i zwraca zadanie ASR używane do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="3ce3b-109">Starts the update replication policy operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="3ce3b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3ce3b-110">PARAMETERS</span></span>

### <span data-ttu-id="3ce3b-111">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="3ce3b-111">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="3ce3b-112">Określa częstotliwość (w godzinach) tworzenia spójnych punktów odzyskiwania aplikacji.</span><span class="sxs-lookup"><span data-stu-id="3ce3b-112">Specifies the frequency(in hours) at which to create application consistent recovery points.</span></span>

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

### <span data-ttu-id="3ce3b-113">— Uwierzytelnianie</span><span class="sxs-lookup"><span data-stu-id="3ce3b-113">-Authentication</span></span>
<span data-ttu-id="3ce3b-114">Określa typ użytego uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="3ce3b-114">Specifies the type of authentication used.</span></span>
<span data-ttu-id="3ce3b-115">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="3ce3b-115">Valid values are:</span></span>

- <span data-ttu-id="3ce3b-116">Dyplom</span><span class="sxs-lookup"><span data-stu-id="3ce3b-116">Certificate</span></span>
-  <span data-ttu-id="3ce3b-117">Mechanizmu</span><span class="sxs-lookup"><span data-stu-id="3ce3b-117">Kerberos</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Certificate, Kerberos

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ce3b-118">-Compression</span><span class="sxs-lookup"><span data-stu-id="3ce3b-118">-Compression</span></span>
<span data-ttu-id="3ce3b-119">Określa, czy kompresja powinna być włączona.</span><span class="sxs-lookup"><span data-stu-id="3ce3b-119">Specifies if compression should be enabled.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ce3b-120">— Szyfrowanie</span><span class="sxs-lookup"><span data-stu-id="3ce3b-120">-Encryption</span></span>
<span data-ttu-id="3ce3b-121">Określa, czy szyfrowanie ma być włączone, czy wyłączone.</span><span class="sxs-lookup"><span data-stu-id="3ce3b-121">Specifies if encryption should be enabled or disabled.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ce3b-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3ce3b-122">-InputObject</span></span>
<span data-ttu-id="3ce3b-123">Obiekt wejściowy polecenia cmdlet: określa obiekt zasad replikacji ASR odpowiadający zasadom replikacji, które mają zostać zaktualizowane.</span><span class="sxs-lookup"><span data-stu-id="3ce3b-123">Input object for the cmdlet: Specifies the ASR replication policy object corresponding to the replication policy to be updated.</span></span>

```yaml
Type: ASRPolicy
Parameter Sets: (All)
Aliases: Policy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3ce3b-124">-NumberOfRecoveryPointsToRetain</span><span class="sxs-lookup"><span data-stu-id="3ce3b-124">-NumberOfRecoveryPointsToRetain</span></span>
<span data-ttu-id="3ce3b-125">Określa punkty odzyskiwania liczb, które mają zostać zachowane.</span><span class="sxs-lookup"><span data-stu-id="3ce3b-125">Specifies the number recovery points to retain.</span></span>

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

### <span data-ttu-id="3ce3b-126">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="3ce3b-126">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="3ce3b-127">Określa identyfikator konta usługi Azure Storage dla lokalizacji docelowej replikacji.</span><span class="sxs-lookup"><span data-stu-id="3ce3b-127">Specifies the Azure storage account ID of the replication target.</span></span> <span data-ttu-id="3ce3b-128">Używane jako docelowe konto magazynu do replikacji, jeśli nie podano elementu alternatywnego podczas włączania replikacji przy użyciu polecenia cmdlet New-AzureRmRecoveryServicesASRReplicationProtectedItem.</span><span class="sxs-lookup"><span data-stu-id="3ce3b-128">Used as the target storage account for replication if an alternate is not provided while enabling replication using the New-AzureRmRecoveryServicesASRReplicationProtectedItem cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ce3b-129">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="3ce3b-129">-ReplicaDeletion</span></span>
<span data-ttu-id="3ce3b-130">Określa, czy maszyna wirtualna repliki ma zostać usunięta podczas wyłączania replikacji z witryny zarządzanej programu VMM do innej.</span><span class="sxs-lookup"><span data-stu-id="3ce3b-130">Specifies if the replica virtual machine should be deleted on disabling replication from a VMM managed site to another.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Required, NotRequired

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ce3b-131">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="3ce3b-131">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="3ce3b-132">Określa interwał częstotliwości replikacji w sekundach.</span><span class="sxs-lookup"><span data-stu-id="3ce3b-132">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="3ce3b-133">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="3ce3b-133">Valid values are:</span></span>

- <span data-ttu-id="3ce3b-134">30</span><span class="sxs-lookup"><span data-stu-id="3ce3b-134">30</span></span>
- <span data-ttu-id="3ce3b-135">300</span><span class="sxs-lookup"><span data-stu-id="3ce3b-135">300</span></span>
- <span data-ttu-id="3ce3b-136">900</span><span class="sxs-lookup"><span data-stu-id="3ce3b-136">900</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: 30, 300, 900

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ce3b-137">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="3ce3b-137">-ReplicationMethod</span></span>
<span data-ttu-id="3ce3b-138">Określa metodę replikacji.</span><span class="sxs-lookup"><span data-stu-id="3ce3b-138">Specifies the replication method.</span></span>
<span data-ttu-id="3ce3b-139">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="3ce3b-139">Valid values are:</span></span>

- <span data-ttu-id="3ce3b-140">Ekran</span><span class="sxs-lookup"><span data-stu-id="3ce3b-140">Online</span></span>
- <span data-ttu-id="3ce3b-141">Pracy</span><span class="sxs-lookup"><span data-stu-id="3ce3b-141">Offline</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Online, Offline

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ce3b-142">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="3ce3b-142">-ReplicationPort</span></span>
<span data-ttu-id="3ce3b-143">Określa port wykorzystywany do replikacji.</span><span class="sxs-lookup"><span data-stu-id="3ce3b-143">Specifies the port used for replication.</span></span>

```yaml
Type: UInt16
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ce3b-144">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="3ce3b-144">-ReplicationStartTime</span></span>
<span data-ttu-id="3ce3b-145">Określa czas rozpoczęcia replikacji.</span><span class="sxs-lookup"><span data-stu-id="3ce3b-145">Specifies the replication start time.</span></span>
<span data-ttu-id="3ce3b-146">Od początku zadania nie może on być późniejszy niż 24 godziny.</span><span class="sxs-lookup"><span data-stu-id="3ce3b-146">It must be no later than 24-hours from the start of the job.</span></span>

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

### <span data-ttu-id="3ce3b-147">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3ce3b-147">-Confirm</span></span>
<span data-ttu-id="3ce3b-148">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ce3b-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ce3b-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ce3b-149">-WhatIf</span></span>
<span data-ttu-id="3ce3b-150">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ce3b-150">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3ce3b-151">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3ce3b-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ce3b-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ce3b-152">CommonParameters</span></span>
<span data-ttu-id="3ce3b-153">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ce3b-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ce3b-154">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ce3b-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ce3b-155">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3ce3b-155">INPUTS</span></span>

### <span data-ttu-id="3ce3b-156">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="3ce3b-156">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="3ce3b-157">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3ce3b-157">OUTPUTS</span></span>

### <span data-ttu-id="3ce3b-158">System. Object</span><span class="sxs-lookup"><span data-stu-id="3ce3b-158">System.Object</span></span>

## <span data-ttu-id="3ce3b-159">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3ce3b-159">NOTES</span></span>

## <span data-ttu-id="3ce3b-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3ce3b-160">RELATED LINKS</span></span>

