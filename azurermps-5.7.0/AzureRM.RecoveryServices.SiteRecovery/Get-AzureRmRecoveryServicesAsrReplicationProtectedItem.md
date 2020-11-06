---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 90b615edefe860e084de0040a13c1ba5a1ff39ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542404"
---
# <span data-ttu-id="3f6a1-101">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="3f6a1-101">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="3f6a1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3f6a1-102">SYNOPSIS</span></span>
<span data-ttu-id="3f6a1-103">Pobiera właściwości elementów chronionych replikacji odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3f6a1-103">Gets the properties of an Azure Site Recovery Replication Protected Items.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f6a1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3f6a1-104">SYNTAX</span></span>

### <span data-ttu-id="3f6a1-105">ByObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3f6a1-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3f6a1-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="3f6a1-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -Name <String>
 -ProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3f6a1-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="3f6a1-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -FriendlyName <String>
 -ProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3f6a1-108">ByProtectableItemObject</span><span class="sxs-lookup"><span data-stu-id="3f6a1-108">ByProtectableItemObject</span></span>
```
Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem <ASRProtectableItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f6a1-109">Opis</span><span class="sxs-lookup"><span data-stu-id="3f6a1-109">DESCRIPTION</span></span>
<span data-ttu-id="3f6a1-110">Polecenie cmdlet **Get-AzureRmRecoveryServicesAsrReplicationProtectedItem** pobiera właściwości wszystkich lub określonego elementu chronionego replikacji ASR z określonego kontenera ochrony przed ASR.</span><span class="sxs-lookup"><span data-stu-id="3f6a1-110">The **Get-AzureRmRecoveryServicesAsrReplicationProtectedItem** cmdlet gets the properties of all or the specified ASR replication protected item from the specified ASR protection container.</span></span>

## <span data-ttu-id="3f6a1-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3f6a1-111">EXAMPLES</span></span>

### <span data-ttu-id="3f6a1-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3f6a1-112">Example 1</span></span>
```
PS C:\> $ReplicationProtectedItems = Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectionContainer $PrimaryContainer
```

<span data-ttu-id="3f6a1-113">Wyświetla wszystkie elementy chronione replikacji w określonym kontenerze ochrony przed ASR.</span><span class="sxs-lookup"><span data-stu-id="3f6a1-113">Lists all replication protected items in the specified ASR protection container.</span></span>

## <span data-ttu-id="3f6a1-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3f6a1-114">PARAMETERS</span></span>

### <span data-ttu-id="3f6a1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f6a1-115">-DefaultProfile</span></span>
<span data-ttu-id="3f6a1-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3f6a1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f6a1-117">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="3f6a1-117">-FriendlyName</span></span>
<span data-ttu-id="3f6a1-118">Określa przyjazną nazwę elementu chronionego replikacją, który należy pobrać.</span><span class="sxs-lookup"><span data-stu-id="3f6a1-118">Specifies the friendly name of the replication protected item to get.</span></span>

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

### <span data-ttu-id="3f6a1-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3f6a1-119">-Name</span></span>
<span data-ttu-id="3f6a1-120">Określa nazwę elementu chronionego replikacją, który ma zostać wyświetlony.</span><span class="sxs-lookup"><span data-stu-id="3f6a1-120">Specifies the name of the replication protected item to get.</span></span>

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

### <span data-ttu-id="3f6a1-121">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="3f6a1-121">-ProtectableItem</span></span>
<span data-ttu-id="3f6a1-122">Określa obiekt elementu z ochroną przed ASR.</span><span class="sxs-lookup"><span data-stu-id="3f6a1-122">Specifies an ASR protectable item object.</span></span> <span data-ttu-id="3f6a1-123">Polecenie cmdlet umożliwia pobieranie elementu chronionego replikacji ASR odpowiadającego określonemu elementowi umożliwiającemu ochronę przed ASR, jeśli element jest chroniony.</span><span class="sxs-lookup"><span data-stu-id="3f6a1-123">The cmdlet gets the ASR replication protected item corresponding to the specified ASR protectable item if the item is protected.</span></span>

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

### <span data-ttu-id="3f6a1-124">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="3f6a1-124">-ProtectionContainer</span></span>
<span data-ttu-id="3f6a1-125">Określa obiekt kontenera ochrony przed Autoodzyskiwaniem kontenera ochrony ASR, który odpowiada elementowi chronionej replikacji.</span><span class="sxs-lookup"><span data-stu-id="3f6a1-125">Specifies the ASR protection container object of the ASR protection container corresponding to the replication protected item.</span></span> 

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

### <span data-ttu-id="3f6a1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f6a1-126">CommonParameters</span></span>
<span data-ttu-id="3f6a1-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f6a1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f6a1-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f6a1-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f6a1-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3f6a1-129">INPUTS</span></span>

### <span data-ttu-id="3f6a1-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="3f6a1-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>
<span data-ttu-id="3f6a1-131">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="3f6a1-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="3f6a1-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3f6a1-132">OUTPUTS</span></span>

### <span data-ttu-id="3f6a1-133">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="3f6a1-133">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="3f6a1-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3f6a1-134">NOTES</span></span>

## <span data-ttu-id="3f6a1-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3f6a1-135">RELATED LINKS</span></span>

[<span data-ttu-id="3f6a1-136">Nowe — AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="3f6a1-136">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="3f6a1-137">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="3f6a1-137">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="3f6a1-138">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="3f6a1-138">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)
