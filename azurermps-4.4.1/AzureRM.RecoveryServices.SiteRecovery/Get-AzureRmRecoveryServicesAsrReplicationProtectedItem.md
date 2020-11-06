---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: fbd2f518d3bdcf64599e32b55cdb9f416c29be21
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553788"
---
# <span data-ttu-id="ff3d0-101">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="ff3d0-101">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="ff3d0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ff3d0-102">SYNOPSIS</span></span>
<span data-ttu-id="ff3d0-103">Pobiera właściwości elementów chronionych replikacji odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ff3d0-103">Gets the properties of an Azure Site Recovery Replication Protected Items.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff3d0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ff3d0-104">SYNTAX</span></span>

### <span data-ttu-id="ff3d0-105">ByObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ff3d0-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectionContainer <ASRProtectionContainer>
 [<CommonParameters>]
```

### <span data-ttu-id="ff3d0-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="ff3d0-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -Name <String>
 -ProtectionContainer <ASRProtectionContainer> [<CommonParameters>]
```

### <span data-ttu-id="ff3d0-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="ff3d0-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -FriendlyName <String>
 -ProtectionContainer <ASRProtectionContainer> [<CommonParameters>]
```

### <span data-ttu-id="ff3d0-108">ByProtectableItemObject</span><span class="sxs-lookup"><span data-stu-id="ff3d0-108">ByProtectableItemObject</span></span>
```
Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem <ASRProtectableItem>
 [<CommonParameters>]
```

## <span data-ttu-id="ff3d0-109">Opis</span><span class="sxs-lookup"><span data-stu-id="ff3d0-109">DESCRIPTION</span></span>
<span data-ttu-id="ff3d0-110">Polecenie cmdlet **Get-AzureRmRecoveryServicesAsrReplicationProtectedItem** pobiera właściwości wszystkich lub określonego elementu chronionego replikacji ASR z określonego kontenera ochrony przed ASR.</span><span class="sxs-lookup"><span data-stu-id="ff3d0-110">The **Get-AzureRmRecoveryServicesAsrReplicationProtectedItem** cmdlet gets the properties of all or the specified ASR replication protected item from the specified ASR protection container.</span></span>

## <span data-ttu-id="ff3d0-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ff3d0-111">EXAMPLES</span></span>

### <span data-ttu-id="ff3d0-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ff3d0-112">Example 1</span></span>
```
PS C:\> $ReplicationProtectedItems = Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectionContainer $PrimaryContainer
```

<span data-ttu-id="ff3d0-113">Wyświetla wszystkie elementy chronione replikacji w określonym kontenerze ochrony przed ASR.</span><span class="sxs-lookup"><span data-stu-id="ff3d0-113">Lists all replication protected items in the specified ASR protection container.</span></span>

## <span data-ttu-id="ff3d0-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ff3d0-114">PARAMETERS</span></span>

### <span data-ttu-id="ff3d0-115">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="ff3d0-115">-FriendlyName</span></span>
<span data-ttu-id="ff3d0-116">Określa przyjazną nazwę elementu chronionego replikacją, który należy pobrać.</span><span class="sxs-lookup"><span data-stu-id="ff3d0-116">Specifies the friendly name of the replication protected item to get.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff3d0-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ff3d0-117">-Name</span></span>
<span data-ttu-id="ff3d0-118">Określa nazwę elementu chronionego replikacją, który ma zostać wyświetlony.</span><span class="sxs-lookup"><span data-stu-id="ff3d0-118">Specifies the name of the replication protected item to get.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff3d0-119">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="ff3d0-119">-ProtectableItem</span></span>
<span data-ttu-id="ff3d0-120">Określa obiekt elementu z ochroną przed ASR.</span><span class="sxs-lookup"><span data-stu-id="ff3d0-120">Specifies an ASR protectable item object.</span></span> <span data-ttu-id="ff3d0-121">Polecenie cmdlet umożliwia pobieranie elementu chronionego replikacji ASR odpowiadającego określonemu elementowi umożliwiającemu ochronę przed ASR, jeśli element jest chroniony.</span><span class="sxs-lookup"><span data-stu-id="ff3d0-121">The cmdlet gets the ASR replication protected item corresponding to the specified ASR protectable item if the item is protected.</span></span>

```yaml
Type: ASRProtectableItem
Parameter Sets: ByProtectableItemObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff3d0-122">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="ff3d0-122">-ProtectionContainer</span></span>
<span data-ttu-id="ff3d0-123">Określa obiekt kontenera ochrony przed Autoodzyskiwaniem kontenera ochrony ASR, który odpowiada elementowi chronionej replikacji.</span><span class="sxs-lookup"><span data-stu-id="ff3d0-123">Specifies the ASR protection container object of the ASR protection container corresponding to the replication protected item.</span></span> 

```yaml
Type: ASRProtectionContainer
Parameter Sets: ByObject, ByObjectWithName, ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff3d0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff3d0-124">CommonParameters</span></span>
<span data-ttu-id="ff3d0-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff3d0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff3d0-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff3d0-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff3d0-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ff3d0-127">INPUTS</span></span>

### <span data-ttu-id="ff3d0-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="ff3d0-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>
<span data-ttu-id="ff3d0-129">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="ff3d0-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="ff3d0-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ff3d0-130">OUTPUTS</span></span>

### <span data-ttu-id="ff3d0-131">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="ff3d0-131">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="ff3d0-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ff3d0-132">NOTES</span></span>

## <span data-ttu-id="ff3d0-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ff3d0-133">RELATED LINKS</span></span>

[<span data-ttu-id="ff3d0-134">Nowe — AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="ff3d0-134">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="ff3d0-135">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="ff3d0-135">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="ff3d0-136">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="ff3d0-136">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)
