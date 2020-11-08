---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 3c89133b18f1425f65ab9430765f0a2a9a7cfafe
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94049867"
---
# <span data-ttu-id="8b446-101">Get-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="8b446-101">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="8b446-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8b446-102">SYNOPSIS</span></span>
<span data-ttu-id="8b446-103">Pobiera właściwości elementów chronionych replikacji odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8b446-103">Gets the properties of an Azure Site Recovery Replication Protected Items.</span></span>

## <span data-ttu-id="8b446-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8b446-104">SYNTAX</span></span>

### <span data-ttu-id="8b446-105">ByObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8b446-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrReplicationProtectedItem -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b446-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="8b446-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrReplicationProtectedItem -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b446-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="8b446-107">ByObjectWithFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrReplicationProtectedItem -FriendlyName <String>
 -ProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b446-108">ByProtectableItemObject</span><span class="sxs-lookup"><span data-stu-id="8b446-108">ByProtectableItemObject</span></span>
```
Get-AzRecoveryServicesAsrReplicationProtectedItem -ProtectableItem <ASRProtectableItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b446-109">Opis</span><span class="sxs-lookup"><span data-stu-id="8b446-109">DESCRIPTION</span></span>
<span data-ttu-id="8b446-110">Polecenie cmdlet **Get-AzRecoveryServicesAsrReplicationProtectedItem** pobiera właściwości wszystkich lub określonego elementu chronionego replikacji ASR z określonego kontenera ochrony przed ASR.</span><span class="sxs-lookup"><span data-stu-id="8b446-110">The **Get-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet gets the properties of all or the specified ASR replication protected item from the specified ASR protection container.</span></span>

## <span data-ttu-id="8b446-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8b446-111">EXAMPLES</span></span>

### <span data-ttu-id="8b446-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8b446-112">Example 1</span></span>
```
PS C:\> $ReplicationProtectedItems = Get-AzRecoveryServicesAsrReplicationProtectedItem -ProtectionContainer $PrimaryContainer
```

<span data-ttu-id="8b446-113">Wyświetla wszystkie elementy chronione replikacji w określonym kontenerze ochrony przed ASR.</span><span class="sxs-lookup"><span data-stu-id="8b446-113">Lists all replication protected items in the specified ASR protection container.</span></span>

## <span data-ttu-id="8b446-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8b446-114">PARAMETERS</span></span>

### <span data-ttu-id="8b446-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b446-115">-DefaultProfile</span></span>
<span data-ttu-id="8b446-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8b446-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="8b446-117">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="8b446-117">-FriendlyName</span></span>
<span data-ttu-id="8b446-118">Określa przyjazną nazwę elementu chronionego replikacją, który należy pobrać.</span><span class="sxs-lookup"><span data-stu-id="8b446-118">Specifies the friendly name of the replication protected item to get.</span></span>

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

### <span data-ttu-id="8b446-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8b446-119">-Name</span></span>
<span data-ttu-id="8b446-120">Określa nazwę elementu chronionego replikacją, który ma zostać wyświetlony.</span><span class="sxs-lookup"><span data-stu-id="8b446-120">Specifies the name of the replication protected item to get.</span></span>

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

### <span data-ttu-id="8b446-121">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="8b446-121">-ProtectableItem</span></span>
<span data-ttu-id="8b446-122">Określa obiekt elementu z ochroną przed ASR.</span><span class="sxs-lookup"><span data-stu-id="8b446-122">Specifies an ASR protectable item object.</span></span> <span data-ttu-id="8b446-123">Polecenie cmdlet umożliwia pobieranie elementu chronionego replikacji ASR odpowiadającego określonemu elementowi umożliwiającemu ochronę przed ASR, jeśli element jest chroniony.</span><span class="sxs-lookup"><span data-stu-id="8b446-123">The cmdlet gets the ASR replication protected item corresponding to the specified ASR protectable item if the item is protected.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem
Parameter Sets: ByProtectableItemObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8b446-124">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="8b446-124">-ProtectionContainer</span></span>
<span data-ttu-id="8b446-125">Określa obiekt kontenera ochrony przed Autoodzyskiwaniem kontenera ochrony ASR, który odpowiada elementowi chronionej replikacji.</span><span class="sxs-lookup"><span data-stu-id="8b446-125">Specifies the ASR protection container object of the ASR protection container corresponding to the replication protected item.</span></span> 

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer
Parameter Sets: ByObject, ByObjectWithName, ByObjectWithFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8b446-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b446-126">CommonParameters</span></span>
<span data-ttu-id="8b446-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b446-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b446-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8b446-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b446-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8b446-129">INPUTS</span></span>

### <span data-ttu-id="8b446-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="8b446-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

### <span data-ttu-id="8b446-131">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="8b446-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="8b446-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8b446-132">OUTPUTS</span></span>

### <span data-ttu-id="8b446-133">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="8b446-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="8b446-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8b446-134">NOTES</span></span>

## <span data-ttu-id="8b446-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8b446-135">RELATED LINKS</span></span>

[<span data-ttu-id="8b446-136">Nowe — AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="8b446-136">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="8b446-137">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="8b446-137">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="8b446-138">Set-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="8b446-138">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzRecoveryServicesAsrReplicationProtectedItem.md)
