---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/new-azrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: f9fe364f680722b1fc34398f0e31a24f53a352ef
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102016145"
---
# <span data-ttu-id="15d73-101">New-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="15d73-101">New-AzRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="15d73-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15d73-102">SYNOPSIS</span></span>
<span data-ttu-id="15d73-103">Tworzy mapowanie kontenera usługi Azure Site Recovery Protection przez skojarzenie określonych zasad replikacji z określonym kontenerem ochrony usługi ASR.</span><span class="sxs-lookup"><span data-stu-id="15d73-103">Creates an Azure Site Recovery Protection Container mapping by associating the specified replication policy to the specified ASR protection container.</span></span>

## <span data-ttu-id="15d73-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="15d73-104">SYNTAX</span></span>

### <span data-ttu-id="15d73-105">EnterpriseToAzure (domyślne)</span><span class="sxs-lookup"><span data-stu-id="15d73-105">EnterpriseToAzure (Default)</span></span>
```
New-AzRecoveryServicesAsrProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15d73-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="15d73-106">EnterpriseToEnterprise</span></span>
```
New-AzRecoveryServicesAsrProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15d73-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="15d73-107">DESCRIPTION</span></span>
<span data-ttu-id="15d73-108">Polecenie cmdlet **New-AzRecoveryServicesAsrProtectionContainerMapping** tworzy mapowanie kontenera ochrony przed odzyskiwaniem witryn platformy Azure przez skojarzenie określonych zasad replikacji z określonym kontenerem ochrony.</span><span class="sxs-lookup"><span data-stu-id="15d73-108">The **New-AzRecoveryServicesAsrProtectionContainerMapping** cmdlet creates an Azure Site Recovery Protection Container mapping by associating the specified replication policy to the specified protection container.</span></span>

## <span data-ttu-id="15d73-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="15d73-109">EXAMPLES</span></span>

### <span data-ttu-id="15d73-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="15d73-110">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesAsrProtectionContainerMapping -Name $ContainerMappingName -Policy $ProtectionProfile -PrimaryProtectionContainer $PrimaryContainer -RecoveryProtectionContainer $RecoveryContainer

Name             : 1f32fee1-05d0-4c11-a997-1618e14b4dab
ID               : /Subscriptions/xxxxxxxxxxxx/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/IbizaV2ATest/replicationJobs/1f32fee1-05d0-4c11-a997-1618e14b4dab
Type             :
JobType          :
DisplayName      :
ClientRequestId  : 2870d5ab-f9be-405e-87d5-5bf20387c623 ActivityId: 24b28fc5-509b-4ad3-92c0-c8bb7ced7fb6
State            : NotStarted
StateDescription : NotStarted
StartTime        :
EndTime          :
TargetObjectId   :
TargetObjectType :
TargetObjectName :
AllowedActions   :
Tasks            : {}
Errors           : {}
```

<span data-ttu-id="15d73-111">Rozpoczyna tworzenie mapowania kontenerów ochrony z określonymi parametrami i zwraca zadanie asr służące do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="15d73-111">Starts the creation of the protection container mapping with the specified parameters, and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="15d73-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="15d73-112">Example 2</span></span>
```
PS C:\> New-AzRecoveryServicesAsrProtectionContainerMapping -Name $PrimaryProtectionContainerMapping -policy $Policy1 -PrimaryProtectionContainer $pc

Name             : 1f32fee1-05d0-4c11-a997-1618e14b4dab
ID               : /Subscriptions/xxxxxxxxxxxx/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/IbizaV2ATest/replicationJobs/1f32fee1-05d0-4c11-a997-1618e14b4dab
Type             :
JobType          :
DisplayName      :
ClientRequestId  : 2870d5ab-f9be-405e-87d5-5bf20387c623 ActivityId: 24b28fc5-509b-4ad3-92c0-c8bb7ced7fb6
State            : NotStarted
StateDescription : NotStarted
StartTime        :
EndTime          :
TargetObjectId   :
TargetObjectType :
TargetObjectName :
AllowedActions   :
Tasks            : {}
Errors           : {}
```

<span data-ttu-id="15d73-113">Rozpoczyna tworzenie mapowania kontenerów ochrony z określonymi parametrami i zwraca zadanie asr służące do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="15d73-113">Starts the creation of the protection container mapping with the specified parameters, and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="15d73-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="15d73-114">PARAMETERS</span></span>

### <span data-ttu-id="15d73-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15d73-115">-DefaultProfile</span></span>
<span data-ttu-id="15d73-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="15d73-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="15d73-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="15d73-117">-Name</span></span>
<span data-ttu-id="15d73-118">Określa nazwę mapowania kontenera ochrony.</span><span class="sxs-lookup"><span data-stu-id="15d73-118">Specifies the name of the Protection Container mapping.</span></span>

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

### <span data-ttu-id="15d73-119">— Zasady</span><span class="sxs-lookup"><span data-stu-id="15d73-119">-Policy</span></span>
<span data-ttu-id="15d73-120">Określa obiekt zasad replikacji asr dla zasad replikacji, który ma być używany podczas mapowania.</span><span class="sxs-lookup"><span data-stu-id="15d73-120">Specifies the ASR replication policy object for the replication policy to be used in the mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="15d73-121">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="15d73-121">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="15d73-122">Określa obiekt kontenera ochrony przed asr dla podstawowego kontenera ochrony, który ma być używany w mapowaniu.</span><span class="sxs-lookup"><span data-stu-id="15d73-122">Specifies the ASR protection container object for the  primary protection container to be used in the mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15d73-123">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="15d73-123">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="15d73-124">Określa obiekt kontenera ochrony usługi ASR dla kontenera ochrony odzyskiwania, który ma być używany w mapowaniu (używany w przypadku replikowania do lokalizacji odzyskiwania, która nie jest platformą Azure).</span><span class="sxs-lookup"><span data-stu-id="15d73-124">Specifies the ASR protection container object for the  recovery protection container to be used in the mapping (used if replicating to a recovery location that is not Azure.)</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15d73-125">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="15d73-125">-Confirm</span></span>
<span data-ttu-id="15d73-126">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="15d73-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15d73-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15d73-127">-WhatIf</span></span>
<span data-ttu-id="15d73-128">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="15d73-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="15d73-129">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="15d73-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15d73-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15d73-130">CommonParameters</span></span>
<span data-ttu-id="15d73-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15d73-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15d73-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="15d73-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15d73-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="15d73-133">INPUTS</span></span>

### <span data-ttu-id="15d73-134">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="15d73-134">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="15d73-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="15d73-135">OUTPUTS</span></span>

### <span data-ttu-id="15d73-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="15d73-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="15d73-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="15d73-137">NOTES</span></span>

## <span data-ttu-id="15d73-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="15d73-138">RELATED LINKS</span></span>

[<span data-ttu-id="15d73-139">Get-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="15d73-139">Get-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./Get-AzRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="15d73-140">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="15d73-140">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./Remove-AzRecoveryServicesAsrProtectionContainerMapping.md)
