---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 6db09c69d112e2638026fde97d586f7945f0508e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501391"
---
# <span data-ttu-id="5f130-101">Get-AzRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="5f130-101">Get-AzRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="5f130-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5f130-102">SYNOPSIS</span></span>
<span data-ttu-id="5f130-103">Pobiera kontenery ochrony ASR w magazynie usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="5f130-103">Gets ASR protection containers in the Recovery Services vault.</span></span>

## <span data-ttu-id="5f130-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5f130-104">SYNTAX</span></span>

### <span data-ttu-id="5f130-105">ByFabricObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5f130-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrProtectionContainer -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5f130-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="5f130-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrProtectionContainer -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f130-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="5f130-107">ByObjectWithFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrProtectionContainer -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f130-108">Opis</span><span class="sxs-lookup"><span data-stu-id="5f130-108">DESCRIPTION</span></span>
<span data-ttu-id="5f130-109">Polecenie cmdlet **Get-AzRecoveryServicesAsrProtectionContainer** pobiera kontenery ochrona przed odzyskiwaniem witryny platformy Azure w magazynie usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="5f130-109">The **Get-AzRecoveryServicesAsrProtectionContainer** cmdlet gets Azure Site Recovery protection containers in the Recovery Services vault.</span></span>
<span data-ttu-id="5f130-110">Kontener ochrony to logiczny kontener umożliwiający ochronę (odnalezionych) i obiektów chronionych, takich jak maszyny wirtualne.</span><span class="sxs-lookup"><span data-stu-id="5f130-110">A protection container is a logical container for protectable(discovered) and protected objects such as virtual machines.</span></span>
<span data-ttu-id="5f130-111">Zasady replikacji definiują ustawienia replikacji dla elementów chronionych i mogą być skojarzone z kontenerem ochrony i stosowane do elementów podlegających ochronie.</span><span class="sxs-lookup"><span data-stu-id="5f130-111">Replication policies define replication settings for protected items and can be associated with a protection container and applied to a protectable item.</span></span>

## <span data-ttu-id="5f130-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5f130-112">EXAMPLES</span></span>

### <span data-ttu-id="5f130-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5f130-113">Example 1</span></span>
```
PS C:\> $ProtectionContainers = Get-AzRecoveryServicesAsrProtectionContainer -Fabric $fabric
```

<span data-ttu-id="5f130-114">Lista kontenerów ochrony w programie Fabric $fabric.</span><span class="sxs-lookup"><span data-stu-id="5f130-114">List of protection container in fabric $fabric.</span></span>

### <span data-ttu-id="5f130-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="5f130-115">Example 2</span></span>
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

<span data-ttu-id="5f130-116">Kontener ochrony w programie Fabric $fabric o nazwie.</span><span class="sxs-lookup"><span data-stu-id="5f130-116">Protection container in fabric $fabric with name.</span></span>

### <span data-ttu-id="5f130-117">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="5f130-117">Example 3</span></span>
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

<span data-ttu-id="5f130-118">Kontener ochrony w programie Fabric $fabric z przyjazną nazwą.</span><span class="sxs-lookup"><span data-stu-id="5f130-118">Protection container in fabric $fabric with friendly Name.</span></span>

## <span data-ttu-id="5f130-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5f130-119">PARAMETERS</span></span>

### <span data-ttu-id="5f130-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f130-120">-DefaultProfile</span></span>
<span data-ttu-id="5f130-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5f130-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="5f130-122">-Fabric</span><span class="sxs-lookup"><span data-stu-id="5f130-122">-Fabric</span></span>
<span data-ttu-id="5f130-123">Odszukaj kontener Ochrona w określonej sieci szkieletowej ASR.</span><span class="sxs-lookup"><span data-stu-id="5f130-123">Look for the protection container in the specified ASR fabric.</span></span>

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

### <span data-ttu-id="5f130-124">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="5f130-124">-FriendlyName</span></span>
<span data-ttu-id="5f130-125">Określa przyjazną nazwę kontenera ochrony przed Autoodzyskiwaniem, który ma zostać wyszukany.</span><span class="sxs-lookup"><span data-stu-id="5f130-125">Specifies the friendly name of the ASR protection container to look for.</span></span>

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

### <span data-ttu-id="5f130-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5f130-126">-Name</span></span>
<span data-ttu-id="5f130-127">Określa nazwę kontenera ochrony przed Autoodzyskiwaniem, który ma zostać wyszukany.</span><span class="sxs-lookup"><span data-stu-id="5f130-127">Specifies the name of the ASR protection container to look for.</span></span>

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

### <span data-ttu-id="5f130-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f130-128">CommonParameters</span></span>
<span data-ttu-id="5f130-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f130-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f130-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5f130-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f130-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5f130-131">INPUTS</span></span>

### <span data-ttu-id="5f130-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="5f130-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="5f130-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5f130-133">OUTPUTS</span></span>

### <span data-ttu-id="5f130-134">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="5f130-134">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="5f130-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5f130-135">NOTES</span></span>

## <span data-ttu-id="5f130-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5f130-136">RELATED LINKS</span></span>
