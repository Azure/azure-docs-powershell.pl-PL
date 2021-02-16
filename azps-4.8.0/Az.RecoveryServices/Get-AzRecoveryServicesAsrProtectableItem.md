---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectableItem.md
ms.openlocfilehash: da9dd3d7b1ed0a54a34fdf5c8a0c9d65b507a07b
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100413986"
---
# <span data-ttu-id="fd3b5-101">Get-AzRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="fd3b5-101">Get-AzRecoveryServicesAsrProtectableItem</span></span>

## <span data-ttu-id="fd3b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd3b5-102">SYNOPSIS</span></span>
<span data-ttu-id="fd3b5-103">Pobierz elementy, które można chronić, w kontenerze ochrony asr.</span><span class="sxs-lookup"><span data-stu-id="fd3b5-103">Get the protectable items in an ASR protection container.</span></span>

## <span data-ttu-id="fd3b5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fd3b5-104">SYNTAX</span></span>

### <span data-ttu-id="fd3b5-105">ByObject (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="fd3b5-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrProtectableItem -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd3b5-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="fd3b5-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrProtectableItem -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd3b5-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="fd3b5-107">ByObjectWithFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrProtectableItem -FriendlyName <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd3b5-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="fd3b5-108">DESCRIPTION</span></span>
<span data-ttu-id="fd3b5-109">Polecenie **cmdlet Get-AzRecoveryServicesAsrProtectableItem** pobiera elementy, które można chronić, w kontenerze Azure Site Recovery Protection Container.</span><span class="sxs-lookup"><span data-stu-id="fd3b5-109">The **Get-AzRecoveryServicesAsrProtectableItem** cmdlet gets the protectable items in an Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="fd3b5-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fd3b5-110">EXAMPLES</span></span>

### <span data-ttu-id="fd3b5-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fd3b5-111">Example 1</span></span>
```
PS C:\> $ProtectableItems = Get-AzRecoveryServicesAsrProtectableItem -ProtectionContainer $Container
```

<span data-ttu-id="fd3b5-112">Pobiera wszystkie elementy, które można chronić, w określonym kontenerze ochrony asr.</span><span class="sxs-lookup"><span data-stu-id="fd3b5-112">Gets all the protectable items in specified ASR protection container.</span></span>

### <span data-ttu-id="fd3b5-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="fd3b5-113">Example 2</span></span>
```
PS C:\> Get-ASRProtectableItem -ProtectionContainer $pc -FriendlyName $piFriendlyName

Disks                         : {}
FabricObjectId                :
FabricSpecificVMDetails       : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificVMDetails
FriendlyName                  : V2A-W2K12-400
ID                            : /Subscriptions/xxxxxxxxxxxx/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/IbizaV2ATest/replicationFabrics/d011a5abf48190235963ee3a88ad188ee6bca8a4c6cd0c8d7ce5d439aa77ffd9/replicationProt
                                ectionContainers/cloud_5dc96260-9f00-42e4-aca7-24ad27fc2078/replicationProtectableItems/22d47502-7df0-11e7-9373-0050568f2e8f
Name                          : 22d47502-7df0-11e7-9373-0050568f2e8f
OS                            : WINDOWS
OSDiskId                      :
OSDiskName                    :
ProtectionContainerId         : cloud_5dc96260-9f00-42e4-aca7-24ad27fc2078
ProtectionReadinessErrors     :
ProtectionStatus              : Unprotected
ReplicationProtectedItemId    :
SupportedReplicationProviders : {InMage, InMageAzureV2}
```

<span data-ttu-id="fd3b5-114">Pobierz elementy, które można chronić, w określonym kontenerze ochrony asr, z nadaną przyjazną nazwą.</span><span class="sxs-lookup"><span data-stu-id="fd3b5-114">Get the protectable items in specified ASR protection container and with given friendly name.</span></span>

### <span data-ttu-id="fd3b5-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="fd3b5-115">Example 3</span></span>
```
PS C:\> Get-ASRProtectableItem -ProtectionContainer $pc -Name $piName

Disks                         : {}
FabricObjectId                :
FabricSpecificVMDetails       : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificVMDetails
FriendlyName                  : V2A-W2K12-400
ID                            : /Subscriptions/xxxxxxxxxxxx/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/IbizaV2ATest/replicationFabrics/d011a5abf48190235963ee3a88ad188ee6bca8a4c6cd0c8d7ce5d439aa77ffd9/replicationProt
                                ectionContainers/cloud_5dc96260-9f00-42e4-aca7-24ad27fc2078/replicationProtectableItems/22d47502-7df0-11e7-9373-0050568f2e8f
Name                          : 22d47502-7df0-11e7-9373-0050568f2e8f
OS                            : WINDOWS
OSDiskId                      :
OSDiskName                    :
ProtectionContainerId         : cloud_5dc96260-9f00-42e4-aca7-24ad27fc2078
ProtectionReadinessErrors     :
ProtectionStatus              : Unprotected
ReplicationProtectedItemId    :
SupportedReplicationProviders : {InMage, InMageAzureV2}
```

<span data-ttu-id="fd3b5-116">Pobiera wszystkie elementy, które można chronić, w określonym kontenerze ochrony asr.</span><span class="sxs-lookup"><span data-stu-id="fd3b5-116">Gets all the protectable items in specified ASR protection container.</span></span>

## <span data-ttu-id="fd3b5-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fd3b5-117">PARAMETERS</span></span>

### <span data-ttu-id="fd3b5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd3b5-118">-DefaultProfile</span></span>
<span data-ttu-id="fd3b5-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="fd3b5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="fd3b5-120">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="fd3b5-120">-FriendlyName</span></span>
<span data-ttu-id="fd3b5-121">Określa przyjazną nazwę elementu, który można chronić przez asr.</span><span class="sxs-lookup"><span data-stu-id="fd3b5-121">Specifies the friendly name of the ASR protectable item.</span></span>

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

### <span data-ttu-id="fd3b5-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="fd3b5-122">-Name</span></span>
<span data-ttu-id="fd3b5-123">Określa nazwę elementu, który można chronić przez asr.</span><span class="sxs-lookup"><span data-stu-id="fd3b5-123">Specifies the name of the ASR protectable item.</span></span>

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

### <span data-ttu-id="fd3b5-124">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="fd3b5-124">-ProtectionContainer</span></span>
<span data-ttu-id="fd3b5-125">Określa obiekt Kontener ochrony przed odzyskiwaniem witryn platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="fd3b5-125">Specifies the Azure Site Recovery Protection Container object.</span></span>

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

### <span data-ttu-id="fd3b5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd3b5-126">CommonParameters</span></span>
<span data-ttu-id="fd3b5-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd3b5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd3b5-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fd3b5-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd3b5-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fd3b5-129">INPUTS</span></span>

### <span data-ttu-id="fd3b5-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="fd3b5-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="fd3b5-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fd3b5-131">OUTPUTS</span></span>

### <span data-ttu-id="fd3b5-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="fd3b5-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="fd3b5-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fd3b5-133">NOTES</span></span>

## <span data-ttu-id="fd3b5-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fd3b5-134">RELATED LINKS</span></span>


