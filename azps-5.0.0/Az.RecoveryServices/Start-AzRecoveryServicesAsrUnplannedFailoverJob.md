---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrunplannedfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrUnplannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrUnplannedFailoverJob.md
ms.openlocfilehash: 61bb846067127b8e7d0a4deca0dd9a726d9dd1f0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94224885"
---
# <span data-ttu-id="3f139-101">Start-AzRecoveryServicesAsrUnplannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="3f139-101">Start-AzRecoveryServicesAsrUnplannedFailoverJob</span></span>

## <span data-ttu-id="3f139-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3f139-102">SYNOPSIS</span></span>
<span data-ttu-id="3f139-103">Rozpoczyna nieplanowaną operację pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="3f139-103">Starts an unplanned failover operation.</span></span>

## <span data-ttu-id="3f139-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3f139-104">SYNTAX</span></span>

### <span data-ttu-id="3f139-105">ByRPIObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3f139-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f139-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="3f139-106">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrUnplannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f139-107">ByRPIObjectWithRecoveryTag</span><span class="sxs-lookup"><span data-stu-id="3f139-107">ByRPIObjectWithRecoveryTag</span></span>
```
Start-AzRecoveryServicesAsrUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] -RecoveryTag <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f139-108">Opis</span><span class="sxs-lookup"><span data-stu-id="3f139-108">DESCRIPTION</span></span>
<span data-ttu-id="3f139-109">Polecenie cmdlet **Start-AzRecoveryServicesAsrUnplannedFailoverJob** rozpoczyna nieplanowane przejście w tryb pracy awaryjnej w trybie failover replikacji odzyskiwania witryny platformy Azure lub planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="3f139-109">The **Start-AzRecoveryServicesAsrUnplannedFailoverJob** cmdlet starts unplanned failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="3f139-110">Możesz sprawdzić, czy zadanie powiodło się przy użyciu Get-AzRecoveryServicesAsrJob polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f139-110">You can check whether the job succeeded by using the Get-AzRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="3f139-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3f139-111">EXAMPLES</span></span>

### <span data-ttu-id="3f139-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3f139-112">Example 1</span></span>
```powershell
PS C:\> $currentJob = Start-AzRecoveryServicesAsrUnplannedFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery -VMNetwork $RecoveryNetwork
```

<span data-ttu-id="3f139-113">Rozpoczyna nieplanowaną operację pracy awaryjnej dla planu odzyskiwania z określonymi parametrami i zwraca zadanie ASR używane do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="3f139-113">Starts the unplanned failover operation for the recovery plan with the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="3f139-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="3f139-114">Example 2</span></span>

<span data-ttu-id="3f139-115">Rozpoczyna nieplanowaną operację pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="3f139-115">Starts an unplanned failover operation.</span></span> <span data-ttu-id="3f139-116">(autogenerowana)</span><span class="sxs-lookup"><span data-stu-id="3f139-116">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Start-AzRecoveryServicesAsrUnplannedFailoverJob -Direction PrimaryToRecovery -RecoveryPoint $rp[0] -ReplicationProtectedItem $ReplicationProtectedItem
```

## <span data-ttu-id="3f139-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3f139-117">PARAMETERS</span></span>

### <span data-ttu-id="3f139-118">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="3f139-118">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="3f139-119">Określa ścieżkę pliku podstawowego certyfikatu szyfrowania danych dla trybu failover elementu chronionego.</span><span class="sxs-lookup"><span data-stu-id="3f139-119">Specifies the data encryption primary certificate file path for failover of Protected Item.</span></span>

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

### <span data-ttu-id="3f139-120">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="3f139-120">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="3f139-121">Określa ścieżkę pliku pomocniczego certyfikatu szyfrowania danych dla trybu failover elementu chronionego.</span><span class="sxs-lookup"><span data-stu-id="3f139-121">Specifies the data encryption secondary certificate file path for failover of Protected Item.</span></span>

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

### <span data-ttu-id="3f139-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f139-122">-DefaultProfile</span></span>
<span data-ttu-id="3f139-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3f139-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="3f139-124">-Direction</span><span class="sxs-lookup"><span data-stu-id="3f139-124">-Direction</span></span>
<span data-ttu-id="3f139-125">Określa kierunek pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="3f139-125">Specifies the failover direction.</span></span>
<span data-ttu-id="3f139-126">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="3f139-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3f139-127">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="3f139-127">PrimaryToRecovery</span></span>
- <span data-ttu-id="3f139-128">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="3f139-128">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="3f139-129">-PerformSourceSideAction</span><span class="sxs-lookup"><span data-stu-id="3f139-129">-PerformSourceSideAction</span></span>
<span data-ttu-id="3f139-130">Wykonaj operację po stronie źródłowej przed rozpoczęciem nieplanowanego przełączania awaryjnego.</span><span class="sxs-lookup"><span data-stu-id="3f139-130">Perform operation in source side before starting unplanned failover.</span></span>

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

### <span data-ttu-id="3f139-131">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="3f139-131">-RecoveryPlan</span></span>
<span data-ttu-id="3f139-132">Określa obiekt planu odzyskiwania ASR.</span><span class="sxs-lookup"><span data-stu-id="3f139-132">Specifies an ASR recovery plan object.</span></span>

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

### <span data-ttu-id="3f139-133">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="3f139-133">-RecoveryPoint</span></span>
<span data-ttu-id="3f139-134">Umożliwia określenie niestandardowego punktu odzyskiwania do trybu failover chronionej maszyny.</span><span class="sxs-lookup"><span data-stu-id="3f139-134">Specifies a custom recovery point to failover the protected machine to.</span></span>

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

### <span data-ttu-id="3f139-135">-RecoveryTag</span><span class="sxs-lookup"><span data-stu-id="3f139-135">-RecoveryTag</span></span>
<span data-ttu-id="3f139-136">Określa tag odzyskiwania do przełączenia do trybu failover.</span><span class="sxs-lookup"><span data-stu-id="3f139-136">Specifies the recovery tag to failover to.</span></span>

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

### <span data-ttu-id="3f139-137">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="3f139-137">-ReplicationProtectedItem</span></span>
<span data-ttu-id="3f139-138">Określa element chroniony replikacji odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3f139-138">Specifies an azure site recovery replication protected item.</span></span>

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

### <span data-ttu-id="3f139-139">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3f139-139">-Confirm</span></span>
<span data-ttu-id="3f139-140">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f139-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f139-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f139-141">-WhatIf</span></span>
<span data-ttu-id="3f139-142">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f139-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3f139-143">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3f139-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f139-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f139-144">CommonParameters</span></span>
<span data-ttu-id="3f139-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f139-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f139-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3f139-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f139-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3f139-147">INPUTS</span></span>

### <span data-ttu-id="3f139-148">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="3f139-148">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="3f139-149">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="3f139-149">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="3f139-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3f139-150">OUTPUTS</span></span>

### <span data-ttu-id="3f139-151">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="3f139-151">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="3f139-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3f139-152">NOTES</span></span>

## <span data-ttu-id="3f139-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3f139-153">RELATED LINKS</span></span>

[<span data-ttu-id="3f139-154">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="3f139-154">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)
