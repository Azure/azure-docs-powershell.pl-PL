---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrunplannedfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrUnplannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrUnplannedFailoverJob.md
ms.openlocfilehash: 2339ae9dbeb2806acd7701fe3a9733c0eaa31503
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93886585"
---
# <span data-ttu-id="ab2df-101">Start-AzRecoveryServicesAsrUnplannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="ab2df-101">Start-AzRecoveryServicesAsrUnplannedFailoverJob</span></span>

## <span data-ttu-id="ab2df-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ab2df-102">SYNOPSIS</span></span>
<span data-ttu-id="ab2df-103">Rozpoczyna nieplanowaną operację pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="ab2df-103">Starts an unplanned failover operation.</span></span>

## <span data-ttu-id="ab2df-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ab2df-104">SYNTAX</span></span>

### <span data-ttu-id="ab2df-105">ByRPIObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ab2df-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab2df-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="ab2df-106">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrUnplannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab2df-107">ByRPIObjectWithRecoveryTag</span><span class="sxs-lookup"><span data-stu-id="ab2df-107">ByRPIObjectWithRecoveryTag</span></span>
```
Start-AzRecoveryServicesAsrUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] -RecoveryTag <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab2df-108">Opis</span><span class="sxs-lookup"><span data-stu-id="ab2df-108">DESCRIPTION</span></span>
<span data-ttu-id="ab2df-109">Polecenie cmdlet **Start-AzRecoveryServicesAsrUnplannedFailoverJob** rozpoczyna nieplanowane przejście w tryb pracy awaryjnej w trybie failover replikacji odzyskiwania witryny platformy Azure lub planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="ab2df-109">The **Start-AzRecoveryServicesAsrUnplannedFailoverJob** cmdlet starts unplanned failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="ab2df-110">Możesz sprawdzić, czy zadanie powiodło się przy użyciu Get-AzRecoveryServicesAsrJob polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab2df-110">You can check whether the job succeeded by using the Get-AzRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="ab2df-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ab2df-111">EXAMPLES</span></span>

### <span data-ttu-id="ab2df-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ab2df-112">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzRecoveryServicesAsrUnplannedFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery -VMNetwork $RecoveryNetwork
```

<span data-ttu-id="ab2df-113">Rozpoczyna nieplanowaną operację pracy awaryjnej dla planu odzyskiwania z określonymi parametrami i zwraca zadanie ASR używane do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="ab2df-113">Starts the unplanned failover operation for the recovery plan with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="ab2df-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ab2df-114">PARAMETERS</span></span>

### <span data-ttu-id="ab2df-115">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="ab2df-115">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="ab2df-116">Określa ścieżkę pliku podstawowego certyfikatu szyfrowania danych dla trybu failover elementu chronionego.</span><span class="sxs-lookup"><span data-stu-id="ab2df-116">Specifies the data encryption primary certificate file path for failover of Protected Item.</span></span>

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

### <span data-ttu-id="ab2df-117">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="ab2df-117">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="ab2df-118">Określa ścieżkę pliku pomocniczego certyfikatu szyfrowania danych dla trybu failover elementu chronionego.</span><span class="sxs-lookup"><span data-stu-id="ab2df-118">Specifies the data encryption secondary certificate file path for failover of Protected Item.</span></span>

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

### <span data-ttu-id="ab2df-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab2df-119">-DefaultProfile</span></span>
<span data-ttu-id="ab2df-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ab2df-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="ab2df-121">-Direction</span><span class="sxs-lookup"><span data-stu-id="ab2df-121">-Direction</span></span>
<span data-ttu-id="ab2df-122">Określa kierunek pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="ab2df-122">Specifies the failover direction.</span></span>
<span data-ttu-id="ab2df-123">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="ab2df-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ab2df-124">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="ab2df-124">PrimaryToRecovery</span></span>
- <span data-ttu-id="ab2df-125">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="ab2df-125">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="ab2df-126">-PerformSourceSideAction</span><span class="sxs-lookup"><span data-stu-id="ab2df-126">-PerformSourceSideAction</span></span>
<span data-ttu-id="ab2df-127">Wykonaj operację po stronie źródłowej przed rozpoczęciem nieplanowanego przełączania awaryjnego.</span><span class="sxs-lookup"><span data-stu-id="ab2df-127">Perform operation in source side before starting unplanned failover.</span></span>

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

### <span data-ttu-id="ab2df-128">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="ab2df-128">-RecoveryPlan</span></span>
<span data-ttu-id="ab2df-129">Określa obiekt planu odzyskiwania ASR.</span><span class="sxs-lookup"><span data-stu-id="ab2df-129">Specifies an ASR recovery plan object.</span></span>

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

### <span data-ttu-id="ab2df-130">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="ab2df-130">-RecoveryPoint</span></span>
<span data-ttu-id="ab2df-131">Umożliwia określenie niestandardowego punktu odzyskiwania do trybu failover chronionej maszyny.</span><span class="sxs-lookup"><span data-stu-id="ab2df-131">Specifies a custom recovery point to failover the protected machine to.</span></span>

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

### <span data-ttu-id="ab2df-132">-RecoveryTag</span><span class="sxs-lookup"><span data-stu-id="ab2df-132">-RecoveryTag</span></span>
<span data-ttu-id="ab2df-133">Określa tag odzyskiwania do przełączenia do trybu failover.</span><span class="sxs-lookup"><span data-stu-id="ab2df-133">Specifies the recovery tag to failover to.</span></span>

```yaml
Type: System.String
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
Type: System.String
Parameter Sets: ByRPIObjectWithRecoveryTag
Aliases:
Accepted values: Latest, LatestAvailable, LatestAvailableApplicationConsistent, LatestAvailableCrashConsistent

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab2df-134">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="ab2df-134">-ReplicationProtectedItem</span></span>
<span data-ttu-id="ab2df-135">Określa element chroniony replikacji odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ab2df-135">Specifies an azure site recovery replication protected item.</span></span>

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

### <span data-ttu-id="ab2df-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ab2df-136">-Confirm</span></span>
<span data-ttu-id="ab2df-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab2df-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab2df-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab2df-138">-WhatIf</span></span>
<span data-ttu-id="ab2df-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab2df-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ab2df-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ab2df-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab2df-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab2df-141">CommonParameters</span></span>
<span data-ttu-id="ab2df-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab2df-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab2df-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab2df-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab2df-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ab2df-144">INPUTS</span></span>

### <span data-ttu-id="ab2df-145">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="ab2df-145">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="ab2df-146">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="ab2df-146">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="ab2df-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ab2df-147">OUTPUTS</span></span>

### <span data-ttu-id="ab2df-148">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="ab2df-148">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="ab2df-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ab2df-149">NOTES</span></span>

## <span data-ttu-id="ab2df-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ab2df-150">RELATED LINKS</span></span>

[<span data-ttu-id="ab2df-151">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="ab2df-151">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)
