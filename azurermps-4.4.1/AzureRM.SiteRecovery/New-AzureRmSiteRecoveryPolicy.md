---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 85C543FE-BBC1-4A1B-9974-1D3BF520085C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryPolicy.md
ms.openlocfilehash: e876e1a7beeee19cd68ac629eb08d48356f98da8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718975"
---
# <span data-ttu-id="a5177-101">New-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="a5177-101">New-AzureRmSiteRecoveryPolicy</span></span>

## <span data-ttu-id="a5177-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a5177-102">SYNOPSIS</span></span>
<span data-ttu-id="a5177-103">Tworzy zasady replikacji odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="a5177-103">Creates a Site Recovery replication policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5177-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a5177-104">SYNTAX</span></span>

### <span data-ttu-id="a5177-105">EnterpriseToAzure (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a5177-105">EnterpriseToAzure (Default)</span></span>
```
New-AzureRmSiteRecoveryPolicy -Name <String> -ReplicationProvider <String>
 -ReplicationFrequencyInSeconds <String> [-RecoveryPoints <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>]
 [-RecoveryAzureStorageAccountId <String>] [-Encryption <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a5177-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="a5177-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmSiteRecoveryPolicy -Name <String> -ReplicationProvider <String> [-ReplicationMethod <String>]
 -ReplicationFrequencyInSeconds <String> [-RecoveryPoints <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] -ReplicationPort <UInt16>
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5177-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a5177-107">DESCRIPTION</span></span>
<span data-ttu-id="a5177-108">Polecenie cmdlet **New-AzureRmSiteRecoveryPolicy** tworzy zasady replikacji odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a5177-108">The **New-AzureRmSiteRecoveryPolicy** cmdlet creates an Azure Site Recovery replication policy.</span></span>
<span data-ttu-id="a5177-109">Zasady replikacji są używane do określania ustawień replikacji, takich jak częstotliwość replikacji i liczba punktów odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="a5177-109">The replication policy is used to specify replication settings such as the replication frequency and number of recovery points.</span></span>

## <span data-ttu-id="a5177-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a5177-110">EXAMPLES</span></span>

## <span data-ttu-id="a5177-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a5177-111">PARAMETERS</span></span>

### <span data-ttu-id="a5177-112">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="a5177-112">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="a5177-113">Określa częstotliwość spójnej migawki aplikacji w godzinach.</span><span class="sxs-lookup"><span data-stu-id="a5177-113">Specifies the frequency of the application consistent snapshot in hours.</span></span>

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

### <span data-ttu-id="a5177-114">— Uwierzytelnianie</span><span class="sxs-lookup"><span data-stu-id="a5177-114">-Authentication</span></span>
<span data-ttu-id="a5177-115">Określa typ użytego uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="a5177-115">Specifies the type of authentication used.</span></span>
<span data-ttu-id="a5177-116">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="a5177-116">Valid values are:</span></span>

- <span data-ttu-id="a5177-117">Dyplom</span><span class="sxs-lookup"><span data-stu-id="a5177-117">Certificate</span></span>
-  <span data-ttu-id="a5177-118">Mechanizmu</span><span class="sxs-lookup"><span data-stu-id="a5177-118">Kerberos</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise
Aliases: 
Accepted values: Certificate, Kerberos

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5177-119">-Compression</span><span class="sxs-lookup"><span data-stu-id="a5177-119">-Compression</span></span>
```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5177-120">— Szyfrowanie</span><span class="sxs-lookup"><span data-stu-id="a5177-120">-Encryption</span></span>
```yaml
Type: System.String
Parameter Sets: EnterpriseToAzure
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5177-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a5177-121">-Name</span></span>
<span data-ttu-id="a5177-122">Określa przyjazną nazwę identyfikującą zasady replikacji odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="a5177-122">Specifies a friendly name which identifies the Site Recovery replication policy.</span></span>

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

### <span data-ttu-id="a5177-123">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="a5177-123">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="a5177-124">Określa identyfikator konta usługi Azure Storage dla lokalizacji docelowej replikacji.</span><span class="sxs-lookup"><span data-stu-id="a5177-124">Specifies the Azure storage account ID of the replication target.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5177-125">-RecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="a5177-125">-RecoveryPoints</span></span>
<span data-ttu-id="a5177-126">Określa liczbę godzin do przechowywania punktów odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="a5177-126">Specifies the number of hours to retain recovery points.</span></span>

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

### <span data-ttu-id="a5177-127">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="a5177-127">-ReplicaDeletion</span></span>
```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise
Aliases: 
Accepted values: Required, NotRequired

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5177-128">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="a5177-128">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="a5177-129">Określa interwał częstotliwości replikacji w sekundach.</span><span class="sxs-lookup"><span data-stu-id="a5177-129">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="a5177-130">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="a5177-130">Valid values are:</span></span>

- <span data-ttu-id="a5177-131">30</span><span class="sxs-lookup"><span data-stu-id="a5177-131">30</span></span>
- <span data-ttu-id="a5177-132">300</span><span class="sxs-lookup"><span data-stu-id="a5177-132">300</span></span>
- <span data-ttu-id="a5177-133">900</span><span class="sxs-lookup"><span data-stu-id="a5177-133">900</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: 30, 300, 900

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5177-134">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="a5177-134">-ReplicationMethod</span></span>
<span data-ttu-id="a5177-135">Określa metodę replikacji.</span><span class="sxs-lookup"><span data-stu-id="a5177-135">Specifies the replication method.</span></span>
<span data-ttu-id="a5177-136">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="a5177-136">Valid values are:</span></span>

- <span data-ttu-id="a5177-137">Ekran</span><span class="sxs-lookup"><span data-stu-id="a5177-137">Online</span></span>
- <span data-ttu-id="a5177-138">Pracy</span><span class="sxs-lookup"><span data-stu-id="a5177-138">Offline</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise
Aliases: 
Accepted values: Online, Offline

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5177-139">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="a5177-139">-ReplicationPort</span></span>
<span data-ttu-id="a5177-140">Określa port wykorzystywany do replikacji.</span><span class="sxs-lookup"><span data-stu-id="a5177-140">Specifies the port used for replication.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5177-141">-ReplicationProvider</span><span class="sxs-lookup"><span data-stu-id="a5177-141">-ReplicationProvider</span></span>
<span data-ttu-id="a5177-142">Określa dostawcę replikacji.</span><span class="sxs-lookup"><span data-stu-id="a5177-142">Specifies the replication provider.</span></span>
<span data-ttu-id="a5177-143">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="a5177-143">Valid values are:</span></span>

- <span data-ttu-id="a5177-144">HyperVReplica2012R2</span><span class="sxs-lookup"><span data-stu-id="a5177-144">HyperVReplica2012R2</span></span>
- <span data-ttu-id="a5177-145">HyperVReplica2012</span><span class="sxs-lookup"><span data-stu-id="a5177-145">HyperVReplica2012</span></span>
- <span data-ttu-id="a5177-146">HyperVReplicaAzure</span><span class="sxs-lookup"><span data-stu-id="a5177-146">HyperVReplicaAzure</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: HyperVReplica2012R2, HyperVReplica2012, HyperVReplicaAzure

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5177-147">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="a5177-147">-ReplicationStartTime</span></span>
<span data-ttu-id="a5177-148">Określa czas rozpoczęcia replikacji.</span><span class="sxs-lookup"><span data-stu-id="a5177-148">Specifies the replication start time.</span></span>
<span data-ttu-id="a5177-149">Od początku zadania nie może on być późniejszy niż 24 godziny.</span><span class="sxs-lookup"><span data-stu-id="a5177-149">It must be no later than 24-hours from the start of the job.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5177-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5177-150">-DefaultProfile</span></span>
<span data-ttu-id="a5177-151">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a5177-151">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5177-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5177-152">CommonParameters</span></span>
<span data-ttu-id="a5177-153">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5177-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5177-154">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5177-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5177-155">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a5177-155">INPUTS</span></span>

## <span data-ttu-id="a5177-156">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a5177-156">OUTPUTS</span></span>

## <span data-ttu-id="a5177-157">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a5177-157">NOTES</span></span>

## <span data-ttu-id="a5177-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a5177-158">RELATED LINKS</span></span>

[<span data-ttu-id="a5177-159">Get-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="a5177-159">Get-AzureRmSiteRecoveryPolicy</span></span>](./Get-AzureRmSiteRecoveryPolicy.md)

[<span data-ttu-id="a5177-160">Remove-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="a5177-160">Remove-AzureRmSiteRecoveryPolicy</span></span>](./Remove-AzureRmSiteRecoveryPolicy.md)
