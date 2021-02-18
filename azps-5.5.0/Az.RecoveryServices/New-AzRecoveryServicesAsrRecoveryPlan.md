---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 9992c4232bd93e9653f0723911f539b1204ce538
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192866"
---
# <span data-ttu-id="b033b-101">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b033b-101">New-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="b033b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b033b-102">SYNOPSIS</span></span>
<span data-ttu-id="b033b-103">Tworzy plan odzyskiwania po stronie asr.</span><span class="sxs-lookup"><span data-stu-id="b033b-103">Creates an ASR recovery plan.</span></span>

## <span data-ttu-id="b033b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b033b-104">SYNTAX</span></span>

### <span data-ttu-id="b033b-105">EnterpriseToEnterprise (domyślne)</span><span class="sxs-lookup"><span data-stu-id="b033b-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> -RecoveryFabric <ASRFabric>
 -ReplicationProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b033b-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="b033b-106">EnterpriseToAzure</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> [-Azure]
 -FailoverDeploymentModel <String> -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b033b-107">AzureZoneToZone</span><span class="sxs-lookup"><span data-stu-id="b033b-107">AzureZoneToZone</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> -PrimaryZone <String>
 -RecoveryZone <String> [-AzureZoneToZone] -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b033b-108">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="b033b-108">ByRPFile</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b033b-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="b033b-109">DESCRIPTION</span></span>
<span data-ttu-id="b033b-110">Polecenie **cmdlet New-AzRecoveryServicesAsrRecoveryPlan** tworzy plan odzyskiwania witryny platformy Azure w magazynie usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="b033b-110">The **New-AzRecoveryServicesAsrRecoveryPlan** cmdlet creates an Azure Site Recovery, recovery plan in the Recovery Services vault.</span></span>

<span data-ttu-id="b033b-111">Plan odzyskiwania gromadzi maszyny wirtualne należące do aplikacji do jednostki, aby umożliwić ich odzyskanie razem.</span><span class="sxs-lookup"><span data-stu-id="b033b-111">A recovery plan gathers virtual machines belonging to an application into a unit to allow them to be recovered together.</span></span>

## <span data-ttu-id="b033b-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b033b-112">EXAMPLES</span></span>

### <span data-ttu-id="b033b-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b033b-113">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrRecoveryPlan -Name $RPName -PrimaryFabric $PrimaryFabric -RecoveryFabric $RecoveryFabric -ReplicationProtectedItem $RPI
```

<span data-ttu-id="b033b-114">Rozpoczyna operację tworzenia planu odzyskiwania z określonymi parametrami i zwraca zadanie asr służące do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="b033b-114">Starts the recovery plan creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="b033b-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="b033b-115">Example 2</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrRecoveryPlan -Name $RPName -PrimaryFabric $PrimaryFabric -PrimaryZone $pZone-RecoveryZone $rZone -ReplicationProtectedItem $RPI
```

<span data-ttu-id="b033b-116">Rozpoczyna operację tworzenia planu odzyskiwania dla strefy platformy Azure w celu strefy replikowanych elementów i zwraca zadanie asr służące do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="b033b-116">Starts the recovery plan creation operation for Azure zone to zone replicated items and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="b033b-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b033b-117">PARAMETERS</span></span>

### <span data-ttu-id="b033b-118">— Azure</span><span class="sxs-lookup"><span data-stu-id="b033b-118">-Azure</span></span>
<span data-ttu-id="b033b-119">Parametr przełącznika określa scenariusz dla platformy Azure na azure disaster recovery, tworzenia planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="b033b-119">Switch parameter specifies the scenario for azure to azure disaster recovery, recovery plan creation.</span></span>

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

### <span data-ttu-id="b033b-120">-AzureZoneToZone</span><span class="sxs-lookup"><span data-stu-id="b033b-120">-AzureZoneToZone</span></span>
<span data-ttu-id="b033b-121">Parametr przełącznika określa tworzenie replikowanego elementu w strefie platformy Azure do scenariusza strefy.</span><span class="sxs-lookup"><span data-stu-id="b033b-121">Switch parameter specifies creating the replicated item in azure zone to zone scenario.</span></span>

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

### <span data-ttu-id="b033b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b033b-122">-DefaultProfile</span></span>
<span data-ttu-id="b033b-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b033b-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="b033b-124">-FailoverDeploymentModel</span><span class="sxs-lookup"><span data-stu-id="b033b-124">-FailoverDeploymentModel</span></span>
<span data-ttu-id="b033b-125">Określa model wdrażania trybu failover (Klasyczny lub Menedżer zasobów) elementów chronionych replikacją, które będą częścią tego planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="b033b-125">Specifies the failover deployment model (Classic or Resource Manager) of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="b033b-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b033b-126">-Name</span></span>
<span data-ttu-id="b033b-127">Nazwa planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="b033b-127">Name of the recovery plan.</span></span>

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

### <span data-ttu-id="b033b-128">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="b033b-128">-Path</span></span>
<span data-ttu-id="b033b-129">Określa ścieżkę do pliku json definicji planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="b033b-129">Specifies the path to the recovery plan definition json file.</span></span> <span data-ttu-id="b033b-130">Do utworzenia planu odzyskiwania można użyć definicji planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="b033b-130">A recovery plan definition json can be used to create the recovery plan.</span></span>

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

### <span data-ttu-id="b033b-131">- PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="b033b-131">-PrimaryFabric</span></span>
<span data-ttu-id="b033b-132">Określa obiekt szkieletowy ASR dla podstawowej struktury ASR elementów chronionych replikacją, które będą częścią tego planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="b033b-132">Specifies the ASR fabric object for the primary ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="b033b-133">-PrimaryZone</span><span class="sxs-lookup"><span data-stu-id="b033b-133">-PrimaryZone</span></span>
<span data-ttu-id="b033b-134">Określa podstawową strefę Dostępności elementów chronionych replikacją, które będą częścią tego planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="b033b-134">Specifies the primary Availabilty zone of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="b033b-135">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="b033b-135">-RecoveryFabric</span></span>
<span data-ttu-id="b033b-136">Określa obiekt szkieletowy ASR dla struktury asr odzyskiwania elementów chronionych replikacją, które będą częścią tego planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="b033b-136">Specifies the ASR fabric object for the recovery ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="b033b-137">-RecoveryZone</span><span class="sxs-lookup"><span data-stu-id="b033b-137">-RecoveryZone</span></span>
<span data-ttu-id="b033b-138">Określa podstawową strefę Dostępności elementów chronionych replikacją, które będą częścią tego planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="b033b-138">Specifies the primary Availabilty zone of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="b033b-139">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="b033b-139">-ReplicationProtectedItem</span></span>
<span data-ttu-id="b033b-140">Lista elementów chronionych replikacją do dodania do pierwszej grupy planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="b033b-140">The list of replication protected items to add to the first group of the recovery plan.</span></span>

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

### <span data-ttu-id="b033b-141">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b033b-141">-Confirm</span></span>
<span data-ttu-id="b033b-142">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b033b-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b033b-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b033b-143">-WhatIf</span></span>
<span data-ttu-id="b033b-144">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b033b-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b033b-145">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b033b-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b033b-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b033b-146">CommonParameters</span></span>
<span data-ttu-id="b033b-147">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b033b-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b033b-148">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b033b-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b033b-149">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b033b-149">INPUTS</span></span>

### <span data-ttu-id="b033b-150">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]</span><span class="sxs-lookup"><span data-stu-id="b033b-150">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]</span></span>

## <span data-ttu-id="b033b-151">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b033b-151">OUTPUTS</span></span>

### <span data-ttu-id="b033b-152">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="b033b-152">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="b033b-153">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b033b-153">NOTES</span></span>

## <span data-ttu-id="b033b-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b033b-154">RELATED LINKS</span></span>

[<span data-ttu-id="b033b-155">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b033b-155">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="b033b-156">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b033b-156">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="b033b-157">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b033b-157">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)


