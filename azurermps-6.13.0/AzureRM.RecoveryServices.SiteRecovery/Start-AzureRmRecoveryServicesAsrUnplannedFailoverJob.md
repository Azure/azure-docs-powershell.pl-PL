---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/start-azurermrecoveryservicesasrunplannedfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob.md
ms.openlocfilehash: b7a9dffe443ca7603b8b5a3bdd100560d83a498e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526121"
---
# <span data-ttu-id="27a2f-101">Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="27a2f-101">Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob</span></span>

## <span data-ttu-id="27a2f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="27a2f-102">SYNOPSIS</span></span>
<span data-ttu-id="27a2f-103">Rozpoczyna nieplanowaną operację pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="27a2f-103">Starts a unplanned failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="27a2f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="27a2f-104">SYNTAX</span></span>

### <span data-ttu-id="27a2f-105">ByRPIObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="27a2f-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27a2f-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="27a2f-106">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27a2f-107">ByRPIObjectWithRecoveryTag</span><span class="sxs-lookup"><span data-stu-id="27a2f-107">ByRPIObjectWithRecoveryTag</span></span>
```
Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] -RecoveryTag <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27a2f-108">Opis</span><span class="sxs-lookup"><span data-stu-id="27a2f-108">DESCRIPTION</span></span>
<span data-ttu-id="27a2f-109">Polecenie cmdlet **Start-AzureRmRecoveryServicesAsrTestFailoverJob** rozpoczyna test pracy awaryjnej w trybie failover witryny usługi Azure chronionej przed replikacją lub planem odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="27a2f-109">The **Start-AzureRmRecoveryServicesAsrTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="27a2f-110">Możesz sprawdzić, czy zadanie powiodło się przy użyciu Get-AzureRmRecoveryServicesAsrJob polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27a2f-110">You can check whether the job succeeded by using the Get-AzureRmRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="27a2f-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="27a2f-111">EXAMPLES</span></span>

### <span data-ttu-id="27a2f-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="27a2f-112">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery -VMNetwork $TestRecoveryNetwork
```

<span data-ttu-id="27a2f-113">Rozpoczyna operację testowej pracy w trybie failover dla planu odzyskiwania z określonymi parametrami i zwraca zadanie ASR używane do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="27a2f-113">Starts the test failover operation for the recovery plan with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="27a2f-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="27a2f-114">PARAMETERS</span></span>

### <span data-ttu-id="27a2f-115">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="27a2f-115">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="27a2f-116">Określa ścieżkę pliku podstawowego certyfikatu szyfrowania danych dla trybu failover elementu chronionego.</span><span class="sxs-lookup"><span data-stu-id="27a2f-116">Specifies the data encryption primary certificate file path for failover of Protected Item.</span></span>

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

### <span data-ttu-id="27a2f-117">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="27a2f-117">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="27a2f-118">Określa ścieżkę pliku pomocniczego certyfikatu szyfrowania danych dla trybu failover elementu chronionego.</span><span class="sxs-lookup"><span data-stu-id="27a2f-118">Specifies the data encryption secondary certificate file path for failover of Protected Item.</span></span>

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

### <span data-ttu-id="27a2f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27a2f-119">-DefaultProfile</span></span>
<span data-ttu-id="27a2f-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="27a2f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="27a2f-121">-Direction</span><span class="sxs-lookup"><span data-stu-id="27a2f-121">-Direction</span></span>
<span data-ttu-id="27a2f-122">Określa kierunek pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="27a2f-122">Specifies the failover direction.</span></span>
<span data-ttu-id="27a2f-123">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="27a2f-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="27a2f-124">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="27a2f-124">PrimaryToRecovery</span></span>
- <span data-ttu-id="27a2f-125">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="27a2f-125">RecoveryToPrimary</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27a2f-126">-PerformSourceSideAction</span><span class="sxs-lookup"><span data-stu-id="27a2f-126">-PerformSourceSideAction</span></span>
<span data-ttu-id="27a2f-127">Wykonaj operację po stronie źródłowej przed rozpoczęciem nieplanowanego przełączania awaryjnego.</span><span class="sxs-lookup"><span data-stu-id="27a2f-127">Perform operation in source side before starting unplanned failover.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: PerformSourceSideActions

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27a2f-128">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="27a2f-128">-RecoveryPlan</span></span>
<span data-ttu-id="27a2f-129">Określa obiekt planu odzyskiwania ASR.</span><span class="sxs-lookup"><span data-stu-id="27a2f-129">Specifies an ASR recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="27a2f-130">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="27a2f-130">-RecoveryPoint</span></span>
<span data-ttu-id="27a2f-131">Umożliwia określenie niestandardowego punktu odzyskiwania do trybu failover chronionej maszyny.</span><span class="sxs-lookup"><span data-stu-id="27a2f-131">Specifies a custom recovery point to failover the protected machine to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint
Parameter Sets: ByRPIObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27a2f-132">-RecoveryTag</span><span class="sxs-lookup"><span data-stu-id="27a2f-132">-RecoveryTag</span></span>
<span data-ttu-id="27a2f-133">Określa tag odzyskiwania do przełączenia do trybu failover.</span><span class="sxs-lookup"><span data-stu-id="27a2f-133">Specifies the recovery tag to failover to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPObject
Aliases:
Accepted values: Latest, LatestAvailable, LatestAvailableApplicationConsistent, LatestAvailableCrashConsistent, Latest, LatestAvailable, LatestAvailableApplicationConsistent, LatestAvailableCrashConsistent

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByRPIObjectWithRecoveryTag
Aliases:
Accepted values: Latest, LatestAvailable, LatestAvailableApplicationConsistent, LatestAvailableCrashConsistent, Latest, LatestAvailable, LatestAvailableApplicationConsistent, LatestAvailableCrashConsistent

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27a2f-134">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="27a2f-134">-ReplicationProtectedItem</span></span>
<span data-ttu-id="27a2f-135">Określa element chroniony replikacji odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="27a2f-135">Specifies an azure site recovery replication protected item.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject, ByRPIObjectWithRecoveryTag
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="27a2f-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="27a2f-136">-Confirm</span></span>
<span data-ttu-id="27a2f-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27a2f-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27a2f-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27a2f-138">-WhatIf</span></span>
<span data-ttu-id="27a2f-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27a2f-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="27a2f-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="27a2f-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27a2f-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27a2f-141">CommonParameters</span></span>
<span data-ttu-id="27a2f-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27a2f-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27a2f-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27a2f-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27a2f-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="27a2f-144">INPUTS</span></span>

### <span data-ttu-id="27a2f-145">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="27a2f-145">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="27a2f-146">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="27a2f-146">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="27a2f-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="27a2f-147">OUTPUTS</span></span>

### <span data-ttu-id="27a2f-148">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="27a2f-148">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="27a2f-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="27a2f-149">NOTES</span></span>

## <span data-ttu-id="27a2f-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="27a2f-150">RELATED LINKS</span></span>

[<span data-ttu-id="27a2f-151">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="27a2f-151">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)
