---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/new-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 41d023abbb1eb4453b295e64d1ccfc3b146fb197
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985692"
---
# <span data-ttu-id="6ddcc-101">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6ddcc-101">New-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="6ddcc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ddcc-102">SYNOPSIS</span></span>
<span data-ttu-id="6ddcc-103">Tworzy plan odzyskiwania po stronie asr.</span><span class="sxs-lookup"><span data-stu-id="6ddcc-103">Creates an ASR recovery plan.</span></span>

## <span data-ttu-id="6ddcc-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6ddcc-104">SYNTAX</span></span>

### <span data-ttu-id="6ddcc-105">EnterpriseToEnterprise (domyślne)</span><span class="sxs-lookup"><span data-stu-id="6ddcc-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> -RecoveryFabric <ASRFabric>
 -ReplicationProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ddcc-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="6ddcc-106">EnterpriseToAzure</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> [-Azure]
 -FailoverDeploymentModel <String> -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ddcc-107">AzureZoneToZone</span><span class="sxs-lookup"><span data-stu-id="6ddcc-107">AzureZoneToZone</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> -PrimaryZone <String>
 -RecoveryZone <String> [-AzureZoneToZone] -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ddcc-108">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="6ddcc-108">ByRPFile</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ddcc-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="6ddcc-109">DESCRIPTION</span></span>
<span data-ttu-id="6ddcc-110">Polecenie **cmdlet New-AzRecoveryServicesAsrRecoveryPlan** tworzy plan odzyskiwania witryny platformy Azure w magazynie usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="6ddcc-110">The **New-AzRecoveryServicesAsrRecoveryPlan** cmdlet creates an Azure Site Recovery, recovery plan in the Recovery Services vault.</span></span>

<span data-ttu-id="6ddcc-111">Plan odzyskiwania gromadzi maszyny wirtualne należące do aplikacji w jednostce w celu umożliwienia ich odzyskania razem.</span><span class="sxs-lookup"><span data-stu-id="6ddcc-111">A recovery plan gathers virtual machines belonging to an application into a unit to allow them to be recovered together.</span></span>

## <span data-ttu-id="6ddcc-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6ddcc-112">EXAMPLES</span></span>

### <span data-ttu-id="6ddcc-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6ddcc-113">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrRecoveryPlan -Name $RPName -PrimaryFabric $PrimaryFabric -RecoveryFabric $RecoveryFabric -ReplicationProtectedItem $RPI
```

<span data-ttu-id="6ddcc-114">Rozpoczyna operację tworzenia planu odzyskiwania z określonymi parametrami i zwraca zadanie asr służące do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="6ddcc-114">Starts the recovery plan creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="6ddcc-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="6ddcc-115">Example 2</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrRecoveryPlan -Name $RPName -PrimaryFabric $PrimaryFabric -PrimaryZone $pZone-RecoveryZone $rZone -ReplicationProtectedItem $RPI
```

<span data-ttu-id="6ddcc-116">Rozpoczyna operację tworzenia planu odzyskiwania dla strefy platformy Azure w celu strefy replikowanych elementów i zwraca zadanie asr służące do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="6ddcc-116">Starts the recovery plan creation operation for Azure zone to zone replicated items and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="6ddcc-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6ddcc-117">PARAMETERS</span></span>

### <span data-ttu-id="6ddcc-118">— Azure</span><span class="sxs-lookup"><span data-stu-id="6ddcc-118">-Azure</span></span>
<span data-ttu-id="6ddcc-119">Parametr przełącznika określa scenariusz dla platformy Azure na azure disaster recovery, tworzenia planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="6ddcc-119">Switch parameter specifies the scenario for azure to azure disaster recovery, recovery plan creation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ddcc-120">-AzureZoneToZone</span><span class="sxs-lookup"><span data-stu-id="6ddcc-120">-AzureZoneToZone</span></span>
<span data-ttu-id="6ddcc-121">Parametr przełącznika określa tworzenie replikowanego elementu w strefie platformy Azure do scenariusza strefy.</span><span class="sxs-lookup"><span data-stu-id="6ddcc-121">Switch parameter specifies creating the replicated item in azure zone to zone scenario.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureZoneToZone
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ddcc-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ddcc-122">-DefaultProfile</span></span>
<span data-ttu-id="6ddcc-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6ddcc-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="6ddcc-124">-FailoverDeploymentModel</span><span class="sxs-lookup"><span data-stu-id="6ddcc-124">-FailoverDeploymentModel</span></span>
<span data-ttu-id="6ddcc-125">Określa model wdrażania trybu failover (klasyczny lub menedżer zasobów) elementów chronionych replikacją, które będą częścią tego planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="6ddcc-125">Specifies the failover deployment model (Classic or Resource Manager) of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToAzure
Aliases:
Accepted values: Classic, ResourceManager

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ddcc-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="6ddcc-126">-Name</span></span>
<span data-ttu-id="6ddcc-127">Nazwa planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="6ddcc-127">Name of the recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, AzureZoneToZone
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ddcc-128">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="6ddcc-128">-Path</span></span>
<span data-ttu-id="6ddcc-129">Określa ścieżkę do pliku json definicji planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="6ddcc-129">Specifies the path to the recovery plan definition json file.</span></span> <span data-ttu-id="6ddcc-130">Do utworzenia planu odzyskiwania można użyć definicji planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="6ddcc-130">A recovery plan definition json can be used to create the recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ddcc-131">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="6ddcc-131">-PrimaryFabric</span></span>
<span data-ttu-id="6ddcc-132">Określa obiekt szkieletowy ASR dla podstawowej struktury ASR elementów chronionych replikacją, które będą częścią tego planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="6ddcc-132">Specifies the ASR fabric object for the primary ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, AzureZoneToZone
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ddcc-133">-PrimaryZone</span><span class="sxs-lookup"><span data-stu-id="6ddcc-133">-PrimaryZone</span></span>
<span data-ttu-id="6ddcc-134">Określa podstawową strefę Dostępności elementów chronionych replikacją, które będą częścią tego planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="6ddcc-134">Specifies the primary Availabilty zone of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureZoneToZone
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ddcc-135">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="6ddcc-135">-RecoveryFabric</span></span>
<span data-ttu-id="6ddcc-136">Określa obiekt szkieletowy ASR dla struktury asr odzyskiwania elementów chronionych replikacją, które będą częścią tego planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="6ddcc-136">Specifies the ASR fabric object for the recovery ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ddcc-137">-RecoveryZone</span><span class="sxs-lookup"><span data-stu-id="6ddcc-137">-RecoveryZone</span></span>
<span data-ttu-id="6ddcc-138">Określa podstawową strefę Dostępności elementów chronionych replikacją, które będą częścią tego planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="6ddcc-138">Specifies the primary Availabilty zone of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureZoneToZone
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ddcc-139">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="6ddcc-139">-ReplicationProtectedItem</span></span>
<span data-ttu-id="6ddcc-140">Lista elementów chronionych replikacją do dodania do pierwszej grupy planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="6ddcc-140">The list of replication protected items to add to the first group of the recovery plan.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]
Parameter Sets: AzureZoneToZone
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6ddcc-141">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6ddcc-141">-Confirm</span></span>
<span data-ttu-id="6ddcc-142">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6ddcc-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ddcc-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ddcc-143">-WhatIf</span></span>
<span data-ttu-id="6ddcc-144">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ddcc-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6ddcc-145">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="6ddcc-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ddcc-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ddcc-146">CommonParameters</span></span>
<span data-ttu-id="6ddcc-147">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ddcc-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ddcc-148">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6ddcc-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ddcc-149">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6ddcc-149">INPUTS</span></span>

### <span data-ttu-id="6ddcc-150">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]</span><span class="sxs-lookup"><span data-stu-id="6ddcc-150">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]</span></span>

## <span data-ttu-id="6ddcc-151">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6ddcc-151">OUTPUTS</span></span>

### <span data-ttu-id="6ddcc-152">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="6ddcc-152">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="6ddcc-153">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6ddcc-153">NOTES</span></span>

## <span data-ttu-id="6ddcc-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6ddcc-154">RELATED LINKS</span></span>

[<span data-ttu-id="6ddcc-155">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6ddcc-155">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="6ddcc-156">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6ddcc-156">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="6ddcc-157">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6ddcc-157">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)


