---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: c893d256351473aa1d840cf1a7e62a960300bdf6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716765"
---
# <span data-ttu-id="46268-101">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="46268-101">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="46268-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="46268-102">SYNOPSIS</span></span>
<span data-ttu-id="46268-103">Pobiera mapowania kontenerów ochrony usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="46268-103">Gets Azure Site Recovery Protection Container mappings.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46268-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="46268-104">SYNTAX</span></span>

### <span data-ttu-id="46268-105">ByObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="46268-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainerMapping -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46268-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="46268-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name <String>
 -ProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46268-107">Opis</span><span class="sxs-lookup"><span data-stu-id="46268-107">DESCRIPTION</span></span>
<span data-ttu-id="46268-108">Polecenie cmdlet **Get-AzureRmRecoveryServicesAsrProtectionContainerMapping** pobiera informacje o kontenerze ochrony do mapowań zasad replikacji (skojarzeń) w magazynie dla określonego kontenera ochrony przed ASR.</span><span class="sxs-lookup"><span data-stu-id="46268-108">The **Get-AzureRmRecoveryServicesAsrProtectionContainerMapping** cmdlet gets information about the protection container to replication policy mappings(association) in the vault for the specified ASR protection container.</span></span>

## <span data-ttu-id="46268-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="46268-109">EXAMPLES</span></span>

### <span data-ttu-id="46268-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="46268-110">Example 1</span></span>
```
PS C:\> $ProtectionContainerMappings = Get-AzureRmRecoveryServicesAsrProtectionContainerMapping -ProtectionContainer $Container
```

<span data-ttu-id="46268-111">Lista mapowań kontenerów ochrony dla kontenera.</span><span class="sxs-lookup"><span data-stu-id="46268-111">List of protection container mappings for container.</span></span>

### <span data-ttu-id="46268-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="46268-112">Example 2</span></span>
```
PS C:\> $ProtectionContainerMappings = Get-AzureRmRecoveryServicesAsrProtectionContainerMapping -ProtectionContainer $Container -Name $PrimaryProtectionContainerMapping

Name                                  : pcmmapping
ID                                    : /Subscriptions/xxxxxxxxxxxx/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/IbizaV2ATest/replicationFabrics/d011a5abf48190235963ee3a88ad188ee6bca8a4c6cd0c8d7ce5d439aa77ffd9/replica
                                        tionProtectionContainers/cloud_5dc96260-9f00-42e4-aca7-24ad27fc2078/replicationProtectionContainerMappings/pcmmapping
Health                                : Normal
HealthErrorDetails                    : {}
PolicyFriendlyName                    : V2aTestPolicy
PolicyId                              : /Subscriptions/xxxxxxxxxxxx/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/IbizaV2ATest/replicationPolicies/V2aTestPolicy
SourceFabricFriendlyName              : V2A-W2K12-400
SourceProtectionContainerFriendlyName : V2A-W2K12-400
State                                 : Paired
TargetFabricFriendlyName              : Microsoft Azure
TargetProtectionContainerFriendlyName : Microsoft Azure
TargetProtectionContainerId           : Microsoft Azure
```

<span data-ttu-id="46268-113">Pobiera wszystkie mapowania kontenerów zabezpieczeń dla określonego kontenera ochrony.</span><span class="sxs-lookup"><span data-stu-id="46268-113">Gets all protection container mappings for the specified protection container.</span></span>

## <span data-ttu-id="46268-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="46268-114">PARAMETERS</span></span>

### <span data-ttu-id="46268-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46268-115">-DefaultProfile</span></span>
<span data-ttu-id="46268-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="46268-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="46268-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="46268-117">-Name</span></span>
<span data-ttu-id="46268-118">Określa nazwę mapowania kontenera ochrony do pobrania.</span><span class="sxs-lookup"><span data-stu-id="46268-118">Specifies the name of the protection container mapping to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46268-119">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="46268-119">-ProtectionContainer</span></span>
<span data-ttu-id="46268-120">Pobierz mapowania kontenera ochrony odpowiadające określonemu obiektowi kontenera ochrony przed ASR.</span><span class="sxs-lookup"><span data-stu-id="46268-120">Get protection container mappings corresponding to the specified ASR protection container object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46268-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46268-121">CommonParameters</span></span>
<span data-ttu-id="46268-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46268-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46268-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46268-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46268-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="46268-124">INPUTS</span></span>

### <span data-ttu-id="46268-125">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="46268-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="46268-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="46268-126">OUTPUTS</span></span>

### <span data-ttu-id="46268-127">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainerMapping, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="46268-127">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="46268-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="46268-128">NOTES</span></span>

## <span data-ttu-id="46268-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="46268-129">RELATED LINKS</span></span>

[<span data-ttu-id="46268-130">Nowe — AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="46268-130">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./New-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="46268-131">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="46268-131">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)
