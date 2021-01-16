---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectableItem.md
ms.openlocfilehash: c9c50e26e99493fb693b8bded693bceb24f5a40f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364772"
---
# <span data-ttu-id="793a0-101">Get-AzRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="793a0-101">Get-AzRecoveryServicesAsrProtectableItem</span></span>

## <span data-ttu-id="793a0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="793a0-102">SYNOPSIS</span></span>
<span data-ttu-id="793a0-103">Pobierz elementy do ochrony w kontenerze ochrona przed Autoodzyskiwaniem.</span><span class="sxs-lookup"><span data-stu-id="793a0-103">Get the protectable items in an ASR protection container.</span></span>

## <span data-ttu-id="793a0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="793a0-104">SYNTAX</span></span>

### <span data-ttu-id="793a0-105">ByObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="793a0-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrProtectableItem -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="793a0-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="793a0-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrProtectableItem -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="793a0-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="793a0-107">ByObjectWithFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrProtectableItem -FriendlyName <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="793a0-108">Opis</span><span class="sxs-lookup"><span data-stu-id="793a0-108">DESCRIPTION</span></span>
<span data-ttu-id="793a0-109">Polecenie cmdlet **Get-AzRecoveryServicesAsrProtectableItem** Pobiera elementy, które należy chronić w kontenerze ochrona odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="793a0-109">The **Get-AzRecoveryServicesAsrProtectableItem** cmdlet gets the protectable items in an Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="793a0-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="793a0-110">EXAMPLES</span></span>

### <span data-ttu-id="793a0-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="793a0-111">Example 1</span></span>
```
PS C:\> $ProtectableItems = Get-AzRecoveryServicesAsrProtectableItem -ProtectionContainer $Container
```

<span data-ttu-id="793a0-112">Pobiera wszystkie elementy chronione w określonym kontenerze ochrony przed ASR.</span><span class="sxs-lookup"><span data-stu-id="793a0-112">Gets all the protectable items in specified ASR protection container.</span></span>

### <span data-ttu-id="793a0-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="793a0-113">Example 2</span></span>
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

<span data-ttu-id="793a0-114">Pobierz elementy, które mają być chronione w określonym kontenerze ochrona przed ASR, i podano przyjazną nazwę.</span><span class="sxs-lookup"><span data-stu-id="793a0-114">Get the protectable items in specified ASR protection container and with given friendly name.</span></span>

### <span data-ttu-id="793a0-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="793a0-115">Example 3</span></span>
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

<span data-ttu-id="793a0-116">Pobiera wszystkie elementy chronione w określonym kontenerze ochrony przed ASR.</span><span class="sxs-lookup"><span data-stu-id="793a0-116">Gets all the protectable items in specified ASR protection container.</span></span>

## <span data-ttu-id="793a0-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="793a0-117">PARAMETERS</span></span>

### <span data-ttu-id="793a0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="793a0-118">-DefaultProfile</span></span>
<span data-ttu-id="793a0-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="793a0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="793a0-120">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="793a0-120">-FriendlyName</span></span>
<span data-ttu-id="793a0-121">Określa przyjazną nazwę elementu z możliwością ochrony przed ASR.</span><span class="sxs-lookup"><span data-stu-id="793a0-121">Specifies the friendly name of the ASR protectable item.</span></span>

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

### <span data-ttu-id="793a0-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="793a0-122">-Name</span></span>
<span data-ttu-id="793a0-123">Określa nazwę elementu do ochrony przed ASR.</span><span class="sxs-lookup"><span data-stu-id="793a0-123">Specifies the name of the ASR protectable item.</span></span>

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

### <span data-ttu-id="793a0-124">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="793a0-124">-ProtectionContainer</span></span>
<span data-ttu-id="793a0-125">Określa obiekt kontenera ochrony przed odzyskiwaniem witryny Azure.</span><span class="sxs-lookup"><span data-stu-id="793a0-125">Specifies the Azure Site Recovery Protection Container object.</span></span>

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

### <span data-ttu-id="793a0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="793a0-126">CommonParameters</span></span>
<span data-ttu-id="793a0-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="793a0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="793a0-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="793a0-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="793a0-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="793a0-129">INPUTS</span></span>

### <span data-ttu-id="793a0-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="793a0-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="793a0-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="793a0-131">OUTPUTS</span></span>

### <span data-ttu-id="793a0-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="793a0-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="793a0-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="793a0-133">NOTES</span></span>

## <span data-ttu-id="793a0-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="793a0-134">RELATED LINKS</span></span>

[<span data-ttu-id="793a0-135">Get-AzRecoveryServicesAsrProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="793a0-135">Get-AzRecoveryServicesAsrProtectionEntity</span></span>](./Get-AzRecoveryServicesAsrProtectionEntity.md)

[<span data-ttu-id="793a0-136">Set-AzRecoveryServicesAsrProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="793a0-136">Set-AzRecoveryServicesAsrProtectionEntity</span></span>](./Set-AzRecoveryServicesAsrProtectionEntity.md)
