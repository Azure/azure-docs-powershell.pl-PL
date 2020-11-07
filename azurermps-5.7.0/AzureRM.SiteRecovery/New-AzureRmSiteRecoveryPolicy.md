---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 85C543FE-BBC1-4A1B-9974-1D3BF520085C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/new-azurermsiterecoverypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryPolicy.md
ms.openlocfilehash: 65e5e507259198cdacc69ff0764b4f4f18bf9077
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718437"
---
# <span data-ttu-id="075ca-101">New-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="075ca-101">New-AzureRmSiteRecoveryPolicy</span></span>

## <span data-ttu-id="075ca-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="075ca-102">SYNOPSIS</span></span>
<span data-ttu-id="075ca-103">Tworzy zasady replikacji odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="075ca-103">Creates a Site Recovery replication policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="075ca-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="075ca-104">SYNTAX</span></span>

### <span data-ttu-id="075ca-105">EnterpriseToAzure (domyślny)</span><span class="sxs-lookup"><span data-stu-id="075ca-105">EnterpriseToAzure (Default)</span></span>
```
New-AzureRmSiteRecoveryPolicy -Name <String> -ReplicationProvider <String>
 -ReplicationFrequencyInSeconds <String> [-RecoveryPoints <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>]
 [-RecoveryAzureStorageAccountId <String>] [-Encryption <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="075ca-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="075ca-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmSiteRecoveryPolicy -Name <String> -ReplicationProvider <String> [-ReplicationMethod <String>]
 -ReplicationFrequencyInSeconds <String> [-RecoveryPoints <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] -ReplicationPort <UInt16>
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="075ca-107">Opis</span><span class="sxs-lookup"><span data-stu-id="075ca-107">DESCRIPTION</span></span>
<span data-ttu-id="075ca-108">Polecenie cmdlet **New-AzureRmSiteRecoveryPolicy** tworzy zasady replikacji odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="075ca-108">The **New-AzureRmSiteRecoveryPolicy** cmdlet creates an Azure Site Recovery replication policy.</span></span>
<span data-ttu-id="075ca-109">Zasady replikacji są używane do określania ustawień replikacji, takich jak częstotliwość replikacji i liczba punktów odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="075ca-109">The replication policy is used to specify replication settings such as the replication frequency and number of recovery points.</span></span>

## <span data-ttu-id="075ca-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="075ca-110">EXAMPLES</span></span>

## <span data-ttu-id="075ca-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="075ca-111">PARAMETERS</span></span>

### <span data-ttu-id="075ca-112">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="075ca-112">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="075ca-113">Określa częstotliwość spójnej migawki aplikacji w godzinach.</span><span class="sxs-lookup"><span data-stu-id="075ca-113">Specifies the frequency of the application consistent snapshot in hours.</span></span>

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

### <span data-ttu-id="075ca-114">— Uwierzytelnianie</span><span class="sxs-lookup"><span data-stu-id="075ca-114">-Authentication</span></span>
<span data-ttu-id="075ca-115">Określa typ użytego uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="075ca-115">Specifies the type of authentication used.</span></span>
<span data-ttu-id="075ca-116">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="075ca-116">Valid values are:</span></span>

- <span data-ttu-id="075ca-117">Dyplom</span><span class="sxs-lookup"><span data-stu-id="075ca-117">Certificate</span></span>
-  <span data-ttu-id="075ca-118">Mechanizmu</span><span class="sxs-lookup"><span data-stu-id="075ca-118">Kerberos</span></span>

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

### <span data-ttu-id="075ca-119">-Compression</span><span class="sxs-lookup"><span data-stu-id="075ca-119">-Compression</span></span>
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

### <span data-ttu-id="075ca-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="075ca-120">-DefaultProfile</span></span>
<span data-ttu-id="075ca-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="075ca-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="075ca-122">— Szyfrowanie</span><span class="sxs-lookup"><span data-stu-id="075ca-122">-Encryption</span></span>
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

### <span data-ttu-id="075ca-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="075ca-123">-Name</span></span>
<span data-ttu-id="075ca-124">Określa przyjazną nazwę identyfikującą zasady replikacji odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="075ca-124">Specifies a friendly name which identifies the Site Recovery replication policy.</span></span>

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

### <span data-ttu-id="075ca-125">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="075ca-125">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="075ca-126">Określa identyfikator konta usługi Azure Storage dla lokalizacji docelowej replikacji.</span><span class="sxs-lookup"><span data-stu-id="075ca-126">Specifies the Azure storage account ID of the replication target.</span></span>

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

### <span data-ttu-id="075ca-127">-RecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="075ca-127">-RecoveryPoints</span></span>
<span data-ttu-id="075ca-128">Określa liczbę godzin do przechowywania punktów odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="075ca-128">Specifies the number of hours to retain recovery points.</span></span>

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

### <span data-ttu-id="075ca-129">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="075ca-129">-ReplicaDeletion</span></span>
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

### <span data-ttu-id="075ca-130">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="075ca-130">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="075ca-131">Określa interwał częstotliwości replikacji w sekundach.</span><span class="sxs-lookup"><span data-stu-id="075ca-131">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="075ca-132">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="075ca-132">Valid values are:</span></span>

- <span data-ttu-id="075ca-133">30</span><span class="sxs-lookup"><span data-stu-id="075ca-133">30</span></span>
- <span data-ttu-id="075ca-134">300</span><span class="sxs-lookup"><span data-stu-id="075ca-134">300</span></span>
- <span data-ttu-id="075ca-135">900</span><span class="sxs-lookup"><span data-stu-id="075ca-135">900</span></span>

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

### <span data-ttu-id="075ca-136">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="075ca-136">-ReplicationMethod</span></span>
<span data-ttu-id="075ca-137">Określa metodę replikacji.</span><span class="sxs-lookup"><span data-stu-id="075ca-137">Specifies the replication method.</span></span>
<span data-ttu-id="075ca-138">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="075ca-138">Valid values are:</span></span>

- <span data-ttu-id="075ca-139">Ekran</span><span class="sxs-lookup"><span data-stu-id="075ca-139">Online</span></span>
- <span data-ttu-id="075ca-140">Pracy</span><span class="sxs-lookup"><span data-stu-id="075ca-140">Offline</span></span>

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

### <span data-ttu-id="075ca-141">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="075ca-141">-ReplicationPort</span></span>
<span data-ttu-id="075ca-142">Określa port wykorzystywany do replikacji.</span><span class="sxs-lookup"><span data-stu-id="075ca-142">Specifies the port used for replication.</span></span>

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

### <span data-ttu-id="075ca-143">-ReplicationProvider</span><span class="sxs-lookup"><span data-stu-id="075ca-143">-ReplicationProvider</span></span>
<span data-ttu-id="075ca-144">Określa dostawcę replikacji.</span><span class="sxs-lookup"><span data-stu-id="075ca-144">Specifies the replication provider.</span></span>
<span data-ttu-id="075ca-145">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="075ca-145">Valid values are:</span></span>

- <span data-ttu-id="075ca-146">HyperVReplica2012R2</span><span class="sxs-lookup"><span data-stu-id="075ca-146">HyperVReplica2012R2</span></span>
- <span data-ttu-id="075ca-147">HyperVReplica2012</span><span class="sxs-lookup"><span data-stu-id="075ca-147">HyperVReplica2012</span></span>
- <span data-ttu-id="075ca-148">HyperVReplicaAzure</span><span class="sxs-lookup"><span data-stu-id="075ca-148">HyperVReplicaAzure</span></span>

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

### <span data-ttu-id="075ca-149">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="075ca-149">-ReplicationStartTime</span></span>
<span data-ttu-id="075ca-150">Określa czas rozpoczęcia replikacji.</span><span class="sxs-lookup"><span data-stu-id="075ca-150">Specifies the replication start time.</span></span>
<span data-ttu-id="075ca-151">Od początku zadania nie może on być późniejszy niż 24 godziny.</span><span class="sxs-lookup"><span data-stu-id="075ca-151">It must be no later than 24-hours from the start of the job.</span></span>

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

### <span data-ttu-id="075ca-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="075ca-152">CommonParameters</span></span>
<span data-ttu-id="075ca-153">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="075ca-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="075ca-154">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="075ca-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="075ca-155">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="075ca-155">INPUTS</span></span>

### <span data-ttu-id="075ca-156">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="075ca-156">None</span></span>
<span data-ttu-id="075ca-157">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="075ca-157">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="075ca-158">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="075ca-158">OUTPUTS</span></span>

## <span data-ttu-id="075ca-159">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="075ca-159">NOTES</span></span>

## <span data-ttu-id="075ca-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="075ca-160">RELATED LINKS</span></span>

[<span data-ttu-id="075ca-161">Get-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="075ca-161">Get-AzureRmSiteRecoveryPolicy</span></span>](./Get-AzureRmSiteRecoveryPolicy.md)

[<span data-ttu-id="075ca-162">Remove-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="075ca-162">Remove-AzureRmSiteRecoveryPolicy</span></span>](./Remove-AzureRmSiteRecoveryPolicy.md)
