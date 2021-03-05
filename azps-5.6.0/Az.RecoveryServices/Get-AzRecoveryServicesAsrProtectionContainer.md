---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 1d7f8adfa0db67d66c65c5ac7f3df7c64b665fda
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992503"
---
# <span data-ttu-id="236bb-101">Get-AzRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="236bb-101">Get-AzRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="236bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="236bb-102">SYNOPSIS</span></span>
<span data-ttu-id="236bb-103">Pobiera kontenery ochrony usługi asr w magazynie usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="236bb-103">Gets ASR protection containers in the Recovery Services vault.</span></span>

## <span data-ttu-id="236bb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="236bb-104">SYNTAX</span></span>

### <span data-ttu-id="236bb-105">ByFabricObject (domyślne)</span><span class="sxs-lookup"><span data-stu-id="236bb-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrProtectionContainer -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="236bb-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="236bb-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrProtectionContainer -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="236bb-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="236bb-107">ByObjectWithFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrProtectionContainer -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="236bb-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="236bb-108">DESCRIPTION</span></span>
<span data-ttu-id="236bb-109">Polecenie **cmdlet Get-AzRecoveryServicesAsrProtectionContainer** pobiera kontenery ochrony usługi Azure Site Recovery w magazynie usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="236bb-109">The **Get-AzRecoveryServicesAsrProtectionContainer** cmdlet gets Azure Site Recovery protection containers in the Recovery Services vault.</span></span>
<span data-ttu-id="236bb-110">Kontener ochrony to kontener logiczny dla obiektów chronionych (wykrytych) i chronionych, takich jak maszyny wirtualne.</span><span class="sxs-lookup"><span data-stu-id="236bb-110">A protection container is a logical container for protectable(discovered) and protected objects such as virtual machines.</span></span>
<span data-ttu-id="236bb-111">Zasady replikacji definiują ustawienia replikacji elementów chronionych i mogą być skojarzone z kontenerem ochrony i stosowane do elementu, który można chronić.</span><span class="sxs-lookup"><span data-stu-id="236bb-111">Replication policies define replication settings for protected items and can be associated with a protection container and applied to a protectable item.</span></span>

## <span data-ttu-id="236bb-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="236bb-112">EXAMPLES</span></span>

### <span data-ttu-id="236bb-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="236bb-113">Example 1</span></span>
```
PS C:\> $ProtectionContainers = Get-AzRecoveryServicesAsrProtectionContainer -Fabric $fabric
```

<span data-ttu-id="236bb-114">Lista kontenera ochrony w materiałach $fabric.</span><span class="sxs-lookup"><span data-stu-id="236bb-114">List of protection container in fabric $fabric.</span></span>

### <span data-ttu-id="236bb-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="236bb-115">Example 2</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrProtectionContainer -Name xxxxx  -Fabric $fabric
FriendlyName                : xxxxxxxx
Name                        : xxxxx
ID                          : /Subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxx/replicationFabrics/xxxxxxxxxxxxxxxxxxxxxxxxx/replicationProtectionContainers/xxxxxxxxxxxxxxxxxxxxxxxxx
Type                        : Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers
FabricFriendlyName          : xxxxxxxxxxxxxxxxxxxxxxxxx
FabricType                  : VMware
Role                        : Primary
AvailablePolicies           : {V2aTestPolicy, v2ahydra, v2aswag-failback, v2aswag}
ProtectionContainerMappings : {pcmmapping, v2aPowerold, 636569dc-79bc-4f50-b83d-89f58717f0b2, df7aa204-b0ef-4d62-943e-324551030e5b}
```

<span data-ttu-id="236bb-116">Kontener ochrony z $fabric z imieniem i nazwiskiem.</span><span class="sxs-lookup"><span data-stu-id="236bb-116">Protection container in fabric $fabric with name.</span></span>

### <span data-ttu-id="236bb-117">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="236bb-117">Example 3</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrProtectionContainer -FriendlyName xxxxxxxx  -Fabric $fabric
FriendlyName                : xxxxxxxx
Name                        : xxxxx
ID                          : /Subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxx/replicationFabrics/xxxxxxxxxxxxxxxxxxxxxxxxx/replicationProtectionContainers/xxxxxxxxxxxxxxxxxxxxxxxxx
Type                        : Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers
FabricFriendlyName          : xxxxxxxxxxxxxxxxxxxxxxxxx
FabricType                  : VMware
Role                        : Primary
AvailablePolicies           : {V2aTestPolicy, v2ahydra, v2aswag-failback, v2aswag}
ProtectionContainerMappings : {pcmmapping, v2aPowerold, 636569dc-79bc-4f50-b83d-89f58717f0b2, df7aa204-b0ef-4d62-943e-324551030e5b}
```

<span data-ttu-id="236bb-118">Kontener ochrony w materiałach $fabric z przyjazną nazwą.</span><span class="sxs-lookup"><span data-stu-id="236bb-118">Protection container in fabric $fabric with friendly Name.</span></span>

## <span data-ttu-id="236bb-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="236bb-119">PARAMETERS</span></span>

### <span data-ttu-id="236bb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="236bb-120">-DefaultProfile</span></span>
<span data-ttu-id="236bb-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="236bb-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="236bb-122">— Materiał</span><span class="sxs-lookup"><span data-stu-id="236bb-122">-Fabric</span></span>
<span data-ttu-id="236bb-123">Poszukaj kontenera ochrony w określonym materiału ASR.</span><span class="sxs-lookup"><span data-stu-id="236bb-123">Look for the protection container in the specified ASR fabric.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="236bb-124">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="236bb-124">-FriendlyName</span></span>
<span data-ttu-id="236bb-125">Określa przyjazną nazwę kontenera ochrony asr, który ma być szukać.</span><span class="sxs-lookup"><span data-stu-id="236bb-125">Specifies the friendly name of the ASR protection container to look for.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="236bb-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="236bb-126">-Name</span></span>
<span data-ttu-id="236bb-127">Określa nazwę kontenera ochrony asr, który ma być szukać.</span><span class="sxs-lookup"><span data-stu-id="236bb-127">Specifies the name of the ASR protection container to look for.</span></span>

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

### <span data-ttu-id="236bb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="236bb-128">CommonParameters</span></span>
<span data-ttu-id="236bb-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="236bb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="236bb-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="236bb-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="236bb-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="236bb-131">INPUTS</span></span>

### <span data-ttu-id="236bb-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span><span class="sxs-lookup"><span data-stu-id="236bb-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="236bb-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="236bb-133">OUTPUTS</span></span>

### <span data-ttu-id="236bb-134">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="236bb-134">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="236bb-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="236bb-135">NOTES</span></span>

## <span data-ttu-id="236bb-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="236bb-136">RELATED LINKS</span></span>
