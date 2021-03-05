---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/start-azrecoveryservicesasrunplannedfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrUnplannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrUnplannedFailoverJob.md
ms.openlocfilehash: fca503fbca9a20d9b6f9e8cb07c5e703e6ecc280
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995289"
---
# <span data-ttu-id="5e9d2-101">Start-AzRecoveryServicesAsrUnplannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="5e9d2-101">Start-AzRecoveryServicesAsrUnplannedFailoverJob</span></span>

## <span data-ttu-id="5e9d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e9d2-102">SYNOPSIS</span></span>
<span data-ttu-id="5e9d2-103">Rozpoczyna niezaplanowaną operację trybu failover.</span><span class="sxs-lookup"><span data-stu-id="5e9d2-103">Starts an unplanned failover operation.</span></span>

## <span data-ttu-id="5e9d2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5e9d2-104">SYNTAX</span></span>

### <span data-ttu-id="5e9d2-105">ByRPIObject (domyślne)</span><span class="sxs-lookup"><span data-stu-id="5e9d2-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e9d2-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="5e9d2-106">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrUnplannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e9d2-107">ByRPIObjectWithRecoveryTag</span><span class="sxs-lookup"><span data-stu-id="5e9d2-107">ByRPIObjectWithRecoveryTag</span></span>
```
Start-AzRecoveryServicesAsrUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] -RecoveryTag <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e9d2-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="5e9d2-108">DESCRIPTION</span></span>
<span data-ttu-id="5e9d2-109">Polecenie cmdlet **Start-AzRecoveryServicesAsrUnplannedFailoverJob** uruchamia niezaplanowane trybu failover elementu chronionego replikacją lub planu odzyskiwania witryny azure.</span><span class="sxs-lookup"><span data-stu-id="5e9d2-109">The **Start-AzRecoveryServicesAsrUnplannedFailoverJob** cmdlet starts unplanned failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="5e9d2-110">Możesz sprawdzić, czy zadanie zakończyło się pomyślnie za pomocą Get-AzRecoveryServicesAsrJob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e9d2-110">You can check whether the job succeeded by using the Get-AzRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="5e9d2-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5e9d2-111">EXAMPLES</span></span>

### <span data-ttu-id="5e9d2-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5e9d2-112">Example 1</span></span>
```powershell
PS C:\> $currentJob = Start-AzRecoveryServicesAsrUnplannedFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery -VMNetwork $RecoveryNetwork
```

<span data-ttu-id="5e9d2-113">Rozpoczyna niezaplanowaną operację trybu failover planu odzyskiwania z określonymi parametrami i zwraca zadanie asr służące do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="5e9d2-113">Starts the unplanned failover operation for the recovery plan with the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="5e9d2-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="5e9d2-114">Example 2</span></span>

<span data-ttu-id="5e9d2-115">Rozpoczyna niezaplanowaną operację trybu failover.</span><span class="sxs-lookup"><span data-stu-id="5e9d2-115">Starts an unplanned failover operation.</span></span> <span data-ttu-id="5e9d2-116">(wygenerowane automatycznie)</span><span class="sxs-lookup"><span data-stu-id="5e9d2-116">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Start-AzRecoveryServicesAsrUnplannedFailoverJob -Direction PrimaryToRecovery -RecoveryPoint $rp[0] -ReplicationProtectedItem $ReplicationProtectedItem
```

## <span data-ttu-id="5e9d2-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5e9d2-117">PARAMETERS</span></span>

### <span data-ttu-id="5e9d2-118">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="5e9d2-118">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="5e9d2-119">Określa ścieżkę pliku podstawowego certyfikatu szyfrowania danych dla trybu failover elementu chronionego.</span><span class="sxs-lookup"><span data-stu-id="5e9d2-119">Specifies the data encryption primary certificate file path for failover of Protected Item.</span></span>

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

### <span data-ttu-id="5e9d2-120">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="5e9d2-120">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="5e9d2-121">Określa ścieżkę pliku pomocniczego certyfikatu szyfrowania danych dla trybu failover elementu chronionego.</span><span class="sxs-lookup"><span data-stu-id="5e9d2-121">Specifies the data encryption secondary certificate file path for failover of Protected Item.</span></span>

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

### <span data-ttu-id="5e9d2-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e9d2-122">-DefaultProfile</span></span>
<span data-ttu-id="5e9d2-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5e9d2-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="5e9d2-124">— Kierunek</span><span class="sxs-lookup"><span data-stu-id="5e9d2-124">-Direction</span></span>
<span data-ttu-id="5e9d2-125">Określa kierunek trybu failover.</span><span class="sxs-lookup"><span data-stu-id="5e9d2-125">Specifies the failover direction.</span></span>
<span data-ttu-id="5e9d2-126">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="5e9d2-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5e9d2-127">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="5e9d2-127">PrimaryToRecovery</span></span>
- <span data-ttu-id="5e9d2-128">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="5e9d2-128">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="5e9d2-129">-PerformSourceSideAction</span><span class="sxs-lookup"><span data-stu-id="5e9d2-129">-PerformSourceSideAction</span></span>
<span data-ttu-id="5e9d2-130">Przed rozpoczęciem niezaplanowanego trybu failover należy wykonać operację po stronie źródłowej.</span><span class="sxs-lookup"><span data-stu-id="5e9d2-130">Perform operation in source side before starting unplanned failover.</span></span>

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

### <span data-ttu-id="5e9d2-131">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="5e9d2-131">-RecoveryPlan</span></span>
<span data-ttu-id="5e9d2-132">Określa obiekt planu odzyskiwania asr.</span><span class="sxs-lookup"><span data-stu-id="5e9d2-132">Specifies an ASR recovery plan object.</span></span>

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

### <span data-ttu-id="5e9d2-133">- RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="5e9d2-133">-RecoveryPoint</span></span>
<span data-ttu-id="5e9d2-134">Określa niestandardowy punkt odzyskiwania dla trybu failover chronionego komputera.</span><span class="sxs-lookup"><span data-stu-id="5e9d2-134">Specifies a custom recovery point to failover the protected machine to.</span></span>

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

### <span data-ttu-id="5e9d2-135">-RecoveryTag</span><span class="sxs-lookup"><span data-stu-id="5e9d2-135">-RecoveryTag</span></span>
<span data-ttu-id="5e9d2-136">Określa tag odzyskiwania do trybu failover.</span><span class="sxs-lookup"><span data-stu-id="5e9d2-136">Specifies the recovery tag to failover to.</span></span>

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

### <span data-ttu-id="5e9d2-137">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="5e9d2-137">-ReplicationProtectedItem</span></span>
<span data-ttu-id="5e9d2-138">Określa element chroniony replikacją odzyskiwania witryn platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5e9d2-138">Specifies an azure site recovery replication protected item.</span></span>

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

### <span data-ttu-id="5e9d2-139">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5e9d2-139">-Confirm</span></span>
<span data-ttu-id="5e9d2-140">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5e9d2-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e9d2-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e9d2-141">-WhatIf</span></span>
<span data-ttu-id="5e9d2-142">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e9d2-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5e9d2-143">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="5e9d2-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e9d2-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e9d2-144">CommonParameters</span></span>
<span data-ttu-id="5e9d2-145">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e9d2-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e9d2-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5e9d2-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e9d2-147">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5e9d2-147">INPUTS</span></span>

### <span data-ttu-id="5e9d2-148">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="5e9d2-148">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="5e9d2-149">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="5e9d2-149">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="5e9d2-150">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5e9d2-150">OUTPUTS</span></span>

### <span data-ttu-id="5e9d2-151">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="5e9d2-151">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="5e9d2-152">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5e9d2-152">NOTES</span></span>

## <span data-ttu-id="5e9d2-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5e9d2-153">RELATED LINKS</span></span>

[<span data-ttu-id="5e9d2-154">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="5e9d2-154">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)
