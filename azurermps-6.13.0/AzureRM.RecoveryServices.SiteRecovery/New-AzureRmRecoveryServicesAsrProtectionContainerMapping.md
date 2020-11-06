---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 35e338d5e6fd9dccbee1a099bc4dabf234cd8e70
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524313"
---
# <span data-ttu-id="a1388-101">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="a1388-101">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="a1388-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a1388-102">SYNOPSIS</span></span>
<span data-ttu-id="a1388-103">Tworzy mapowanie kontenera ochrony witryny platformy Azure, kojarząc określone zasady replikacji z określonym kontenerem ochrony przed Autoodzyskiwaniem.</span><span class="sxs-lookup"><span data-stu-id="a1388-103">Creates an Azure Site Recovery Protection Container mapping by associating the specified replication policy to the specified ASR protection container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1388-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a1388-104">SYNTAX</span></span>

### <span data-ttu-id="a1388-105">EnterpriseToAzure (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a1388-105">EnterpriseToAzure (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1388-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="a1388-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1388-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a1388-107">DESCRIPTION</span></span>
<span data-ttu-id="a1388-108">Polecenie cmdlet **New-AzureRmRecoveryServicesAsrProtectionContainerMapping** tworzy mapowanie kontenera ochrony usługi Azure Site Recovery, kojarząc określone zasady replikacji z określonym kontenerem ochrony.</span><span class="sxs-lookup"><span data-stu-id="a1388-108">The **New-AzureRmRecoveryServicesAsrProtectionContainerMapping** cmdlet creates an Azure Site Recovery Protection Container mapping by associating the specified replication policy to the specified protection container.</span></span>

## <span data-ttu-id="a1388-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a1388-109">EXAMPLES</span></span>

### <span data-ttu-id="a1388-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a1388-110">Example 1</span></span>
```
PS C:\> New-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name $ContainerMappingName -Policy $ProtectionProfile -PrimaryProtectionContainer $PrimaryContainer -RecoveryProtectionContainer $RecoveryContainer

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

<span data-ttu-id="a1388-111">Rozpoczyna Tworzenie mapowania kontenera ochrony przy użyciu określonych parametrów i zwraca zadanie ASR używane do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="a1388-111">Starts the creation of the protection container mapping with the specified parameters, and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="a1388-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="a1388-112">Example 2</span></span>
```
PS C:\> New-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name $PrimaryProtectionContainerMapping -policy $Policy1 -PrimaryProtectionContainer $pc

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

<span data-ttu-id="a1388-113">Rozpoczyna Tworzenie mapowania kontenera ochrony przy użyciu określonych parametrów i zwraca zadanie ASR używane do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="a1388-113">Starts the creation of the protection container mapping with the specified parameters, and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="a1388-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a1388-114">PARAMETERS</span></span>

### <span data-ttu-id="a1388-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1388-115">-DefaultProfile</span></span>
<span data-ttu-id="a1388-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a1388-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="a1388-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a1388-117">-Name</span></span>
<span data-ttu-id="a1388-118">Określa nazwę mapowania kontenera ochrony.</span><span class="sxs-lookup"><span data-stu-id="a1388-118">Specifies the name of the Protection Container mapping.</span></span>

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

### <span data-ttu-id="a1388-119">-Policy</span><span class="sxs-lookup"><span data-stu-id="a1388-119">-Policy</span></span>
<span data-ttu-id="a1388-120">Określa obiekt zasad replikacji ASR dla zasad replikacji, które mają być używane w mapowaniu.</span><span class="sxs-lookup"><span data-stu-id="a1388-120">Specifies the ASR replication policy object for the replication policy to be used in the mapping.</span></span>

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

### <span data-ttu-id="a1388-121">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="a1388-121">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="a1388-122">Określa obiekt kontenera ochrony przed Autoodzyskiwaniem dla głównego kontenera ochrony, który ma być wykorzystywany w mapowaniu.</span><span class="sxs-lookup"><span data-stu-id="a1388-122">Specifies the ASR protection container object for the  primary protection container to be used in the mapping.</span></span>

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

### <span data-ttu-id="a1388-123">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="a1388-123">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="a1388-124">Określa obiekt kontenera ochrony przed odzyskaniem dla kontenera ochrony przed odzyskiwaniem, który ma być wykorzystywany w mapowaniu (używane w przypadku replikowania do lokalizacji odzyskiwania, która nie jest platformą Azure).</span><span class="sxs-lookup"><span data-stu-id="a1388-124">Specifies the ASR protection container object for the  recovery protection container to be used in the mapping (used if replicating to a recovery location that is not Azure.)</span></span>

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

### <span data-ttu-id="a1388-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a1388-125">-Confirm</span></span>
<span data-ttu-id="a1388-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1388-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1388-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1388-127">-WhatIf</span></span>
<span data-ttu-id="a1388-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1388-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a1388-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a1388-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1388-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1388-130">CommonParameters</span></span>
<span data-ttu-id="a1388-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1388-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1388-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1388-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1388-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a1388-133">INPUTS</span></span>

### <span data-ttu-id="a1388-134">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="a1388-134">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="a1388-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a1388-135">OUTPUTS</span></span>

### <span data-ttu-id="a1388-136">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="a1388-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="a1388-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a1388-137">NOTES</span></span>

## <span data-ttu-id="a1388-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a1388-138">RELATED LINKS</span></span>

[<span data-ttu-id="a1388-139">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="a1388-139">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./Get-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="a1388-140">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="a1388-140">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)
