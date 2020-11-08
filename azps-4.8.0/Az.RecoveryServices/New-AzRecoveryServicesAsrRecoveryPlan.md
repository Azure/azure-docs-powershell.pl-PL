---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 9992c4232bd93e9653f0723911f539b1204ce538
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062541"
---
# <span data-ttu-id="1943f-101">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="1943f-101">New-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="1943f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1943f-102">SYNOPSIS</span></span>
<span data-ttu-id="1943f-103">Tworzy plan odzyskiwania ASR.</span><span class="sxs-lookup"><span data-stu-id="1943f-103">Creates an ASR recovery plan.</span></span>

## <span data-ttu-id="1943f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1943f-104">SYNTAX</span></span>

### <span data-ttu-id="1943f-105">EnterpriseToEnterprise (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1943f-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> -RecoveryFabric <ASRFabric>
 -ReplicationProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1943f-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="1943f-106">EnterpriseToAzure</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> [-Azure]
 -FailoverDeploymentModel <String> -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1943f-107">AzureZoneToZone</span><span class="sxs-lookup"><span data-stu-id="1943f-107">AzureZoneToZone</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> -PrimaryZone <String>
 -RecoveryZone <String> [-AzureZoneToZone] -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1943f-108">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="1943f-108">ByRPFile</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1943f-109">Opis</span><span class="sxs-lookup"><span data-stu-id="1943f-109">DESCRIPTION</span></span>
<span data-ttu-id="1943f-110">Polecenie cmdlet **New-AzRecoveryServicesAsrRecoveryPlan** tworzy usługę Azure Site Recovery, plan odzyskiwania w magazynie usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="1943f-110">The **New-AzRecoveryServicesAsrRecoveryPlan** cmdlet creates an Azure Site Recovery, recovery plan in the Recovery Services vault.</span></span>

<span data-ttu-id="1943f-111">Plan odzyskiwania umożliwia zbieranie maszyn wirtualnych należących do danej aplikacji w jednostce w celu umożliwienia ich odzyskania.</span><span class="sxs-lookup"><span data-stu-id="1943f-111">A recovery plan gathers virtual machines belonging to an application into a unit to allow them to be recovered together.</span></span>

## <span data-ttu-id="1943f-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1943f-112">EXAMPLES</span></span>

### <span data-ttu-id="1943f-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1943f-113">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrRecoveryPlan -Name $RPName -PrimaryFabric $PrimaryFabric -RecoveryFabric $RecoveryFabric -ReplicationProtectedItem $RPI
```

<span data-ttu-id="1943f-114">Rozpoczyna operację tworzenia planu odzyskiwania z określonymi parametrami i zwraca zadanie ASR używane do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="1943f-114">Starts the recovery plan creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="1943f-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="1943f-115">Example 2</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrRecoveryPlan -Name $RPName -PrimaryFabric $PrimaryFabric -PrimaryZone $pZone-RecoveryZone $rZone -ReplicationProtectedItem $RPI
```

<span data-ttu-id="1943f-116">Rozpoczyna operację tworzenia planu odzyskiwania strefy platformy Azure do elementów replikowanych strefy i zwraca zadanie ASR używane do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="1943f-116">Starts the recovery plan creation operation for Azure zone to zone replicated items and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="1943f-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1943f-117">PARAMETERS</span></span>

### <span data-ttu-id="1943f-118">-Azure</span><span class="sxs-lookup"><span data-stu-id="1943f-118">-Azure</span></span>
<span data-ttu-id="1943f-119">Parametr Switch określa scenariusz odzyskiwania po awarii usługi Azure na platformie Azure, Tworzenie planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="1943f-119">Switch parameter specifies the scenario for azure to azure disaster recovery, recovery plan creation.</span></span>

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

### <span data-ttu-id="1943f-120">-AzureZoneToZone</span><span class="sxs-lookup"><span data-stu-id="1943f-120">-AzureZoneToZone</span></span>
<span data-ttu-id="1943f-121">Parametr Switch określa utworzenie replikowanego elementu w strefie platformy Azure do scenariusza Zone.</span><span class="sxs-lookup"><span data-stu-id="1943f-121">Switch parameter specifies creating the replicated item in azure zone to zone scenario.</span></span>

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

### <span data-ttu-id="1943f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1943f-122">-DefaultProfile</span></span>
<span data-ttu-id="1943f-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1943f-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="1943f-124">-FailoverDeploymentModel</span><span class="sxs-lookup"><span data-stu-id="1943f-124">-FailoverDeploymentModel</span></span>
<span data-ttu-id="1943f-125">Określa model wdrożenia trybu failover (klasyczny lub Menedżer zasobów) elementów chronionych replikacji, które będą częścią tego planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="1943f-125">Specifies the failover deployment model (Classic or Resource Manager) of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="1943f-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1943f-126">-Name</span></span>
<span data-ttu-id="1943f-127">Nazwa planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="1943f-127">Name of the recovery plan.</span></span>

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

### <span data-ttu-id="1943f-128">-Path</span><span class="sxs-lookup"><span data-stu-id="1943f-128">-Path</span></span>
<span data-ttu-id="1943f-129">Określa ścieżkę do pliku JSON definicji planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="1943f-129">Specifies the path to the recovery plan definition json file.</span></span> <span data-ttu-id="1943f-130">Za pomocą notacji JSON z definicji planu odzyskiwania można utworzyć plan odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="1943f-130">A recovery plan definition json can be used to create the recovery plan.</span></span>

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

### <span data-ttu-id="1943f-131">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="1943f-131">-PrimaryFabric</span></span>
<span data-ttu-id="1943f-132">Określa obiekt sieci szkieletowej ASR dla podstawowej sieci szkieletowej ASR elementów chronionych replikacją, które będą częścią tego planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="1943f-132">Specifies the ASR fabric object for the primary ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="1943f-133">-PrimaryZone</span><span class="sxs-lookup"><span data-stu-id="1943f-133">-PrimaryZone</span></span>
<span data-ttu-id="1943f-134">Określa podstawową strefę Availabilty elementów chronionych replikacji, które będą częścią tego planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="1943f-134">Specifies the primary Availabilty zone of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="1943f-135">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="1943f-135">-RecoveryFabric</span></span>
<span data-ttu-id="1943f-136">Określa obiekt sieci szkieletowej ASR dla odtwarzania ASR z elementami chronionymi replikacji, które będą częścią tego planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="1943f-136">Specifies the ASR fabric object for the recovery ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="1943f-137">-RecoveryZone</span><span class="sxs-lookup"><span data-stu-id="1943f-137">-RecoveryZone</span></span>
<span data-ttu-id="1943f-138">Określa podstawową strefę Availabilty elementów chronionych replikacji, które będą częścią tego planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="1943f-138">Specifies the primary Availabilty zone of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="1943f-139">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1943f-139">-ReplicationProtectedItem</span></span>
<span data-ttu-id="1943f-140">Lista elementów chronionych replikacji, które mają zostać dodane do pierwszej grupy planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="1943f-140">The list of replication protected items to add to the first group of the recovery plan.</span></span>

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

### <span data-ttu-id="1943f-141">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1943f-141">-Confirm</span></span>
<span data-ttu-id="1943f-142">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1943f-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1943f-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1943f-143">-WhatIf</span></span>
<span data-ttu-id="1943f-144">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1943f-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1943f-145">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1943f-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1943f-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1943f-146">CommonParameters</span></span>
<span data-ttu-id="1943f-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1943f-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1943f-148">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1943f-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1943f-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1943f-149">INPUTS</span></span>

### <span data-ttu-id="1943f-150">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem []</span><span class="sxs-lookup"><span data-stu-id="1943f-150">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]</span></span>

## <span data-ttu-id="1943f-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1943f-151">OUTPUTS</span></span>

### <span data-ttu-id="1943f-152">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="1943f-152">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="1943f-153">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1943f-153">NOTES</span></span>

## <span data-ttu-id="1943f-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1943f-154">RELATED LINKS</span></span>

[<span data-ttu-id="1943f-155">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="1943f-155">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="1943f-156">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="1943f-156">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="1943f-157">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="1943f-157">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)


