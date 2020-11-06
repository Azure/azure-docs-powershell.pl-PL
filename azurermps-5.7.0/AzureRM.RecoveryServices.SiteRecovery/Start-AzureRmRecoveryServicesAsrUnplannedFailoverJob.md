---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/start-azurermrecoveryservicesasrunplannedfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob.md
ms.openlocfilehash: ba31be7094da4c4c17fa8c674728b8c32bfa2b8d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525001"
---
# <span data-ttu-id="d22d2-101">Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="d22d2-101">Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob</span></span>

## <span data-ttu-id="d22d2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d22d2-102">SYNOPSIS</span></span>
<span data-ttu-id="d22d2-103">Rozpoczyna nieplanowaną operację pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="d22d2-103">Starts a unplanned failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d22d2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d22d2-104">SYNTAX</span></span>

### <span data-ttu-id="d22d2-105">ByRPIObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d22d2-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d22d2-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="d22d2-106">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d22d2-107">ByRPIObjectWithRecoveryTag</span><span class="sxs-lookup"><span data-stu-id="d22d2-107">ByRPIObjectWithRecoveryTag</span></span>
```
Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] -RecoveryTag <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d22d2-108">Opis</span><span class="sxs-lookup"><span data-stu-id="d22d2-108">DESCRIPTION</span></span>
<span data-ttu-id="d22d2-109">Polecenie cmdlet **Start-AzureRmRecoveryServicesAsrTestFailoverJob** rozpoczyna test pracy awaryjnej w trybie failover witryny usługi Azure chronionej przed replikacją lub planem odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="d22d2-109">The **Start-AzureRmRecoveryServicesAsrTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="d22d2-110">Możesz sprawdzić, czy zadanie powiodło się przy użyciu Get-AzureRmRecoveryServicesAsrJob polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d22d2-110">You can check whether the job succeeded by using the Get-AzureRmRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="d22d2-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d22d2-111">EXAMPLES</span></span>

### <span data-ttu-id="d22d2-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d22d2-112">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery -VMNetwork $TestRecoveryNetwork
```

<span data-ttu-id="d22d2-113">Rozpoczyna operację testowej pracy w trybie failover dla planu odzyskiwania z określonymi parametrami i zwraca zadanie ASR używane do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="d22d2-113">Starts the test failover operation for the recovery plan with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="d22d2-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d22d2-114">PARAMETERS</span></span>

### <span data-ttu-id="d22d2-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d22d2-115">-Confirm</span></span>
<span data-ttu-id="d22d2-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d22d2-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d22d2-117">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="d22d2-117">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="d22d2-118">Określa ścieżkę pliku podstawowego certyfikatu szyfrowania danych dla trybu failover elementu chronionego.</span><span class="sxs-lookup"><span data-stu-id="d22d2-118">Specifies the data encryption primary certificate file path for failover of Protected Item.</span></span>

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

### <span data-ttu-id="d22d2-119">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="d22d2-119">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="d22d2-120">Określa ścieżkę pliku pomocniczego certyfikatu szyfrowania danych dla trybu failover elementu chronionego.</span><span class="sxs-lookup"><span data-stu-id="d22d2-120">Specifies the data encryption secondary certificate file path for failover of Protected Item.</span></span>

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

### <span data-ttu-id="d22d2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d22d2-121">-DefaultProfile</span></span>
<span data-ttu-id="d22d2-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d22d2-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="d22d2-123">-Direction</span><span class="sxs-lookup"><span data-stu-id="d22d2-123">-Direction</span></span>
<span data-ttu-id="d22d2-124">Określa kierunek pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="d22d2-124">Specifies the failover direction.</span></span>
<span data-ttu-id="d22d2-125">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="d22d2-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d22d2-126">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="d22d2-126">PrimaryToRecovery</span></span>
- <span data-ttu-id="d22d2-127">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="d22d2-127">RecoveryToPrimary</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d22d2-128">-PerformSourceSideAction</span><span class="sxs-lookup"><span data-stu-id="d22d2-128">-PerformSourceSideAction</span></span>
<span data-ttu-id="d22d2-129">Wykonaj operację po stronie źródłowej przed rozpoczęciem nieplanowanego przełączania awaryjnego.</span><span class="sxs-lookup"><span data-stu-id="d22d2-129">Perform operation in source side before starting unplanned failover.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: PerformSourceSideActions

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d22d2-130">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d22d2-130">-RecoveryPlan</span></span>
<span data-ttu-id="d22d2-131">Określa obiekt planu odzyskiwania ASR.</span><span class="sxs-lookup"><span data-stu-id="d22d2-131">Specifies an ASR recovery plan object.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d22d2-132">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="d22d2-132">-RecoveryPoint</span></span>
<span data-ttu-id="d22d2-133">Umożliwia określenie niestandardowego punktu odzyskiwania do trybu failover chronionej maszyny.</span><span class="sxs-lookup"><span data-stu-id="d22d2-133">Specifies a custom recovery point to failover the protected machine to.</span></span>

```yaml
Type: ASRRecoveryPoint
Parameter Sets: ByRPIObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d22d2-134">-RecoveryTag</span><span class="sxs-lookup"><span data-stu-id="d22d2-134">-RecoveryTag</span></span>
<span data-ttu-id="d22d2-135">Określa tag odzyskiwania do przełączenia do trybu failover.</span><span class="sxs-lookup"><span data-stu-id="d22d2-135">Specifies the recovery tag to failover to.</span></span>

```yaml
Type: String
Parameter Sets: ByRPObject
Aliases:
Accepted values: Latest, LatestAvailable, LatestAvailableApplicationConsistent, LatestAvailableCrashConsistent

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByRPIObjectWithRecoveryTag
Aliases:
Accepted values: Latest, LatestAvailable, LatestAvailableApplicationConsistent, LatestAvailableCrashConsistent

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d22d2-136">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="d22d2-136">-ReplicationProtectedItem</span></span>
<span data-ttu-id="d22d2-137">Określa element chroniony replikacji odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d22d2-137">Specifies an azure site recovery replication protected item.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: ByRPIObject, ByRPIObjectWithRecoveryTag
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d22d2-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d22d2-138">-WhatIf</span></span>
<span data-ttu-id="d22d2-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d22d2-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d22d2-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d22d2-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d22d2-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d22d2-141">CommonParameters</span></span>
<span data-ttu-id="d22d2-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d22d2-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d22d2-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d22d2-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d22d2-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d22d2-144">INPUTS</span></span>

### <span data-ttu-id="d22d2-145">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d22d2-145">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="d22d2-146">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="d22d2-146">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="d22d2-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d22d2-147">OUTPUTS</span></span>

### <span data-ttu-id="d22d2-148">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="d22d2-148">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="d22d2-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d22d2-149">NOTES</span></span>

## <span data-ttu-id="d22d2-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d22d2-150">RELATED LINKS</span></span>

[<span data-ttu-id="d22d2-151">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="d22d2-151">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)
