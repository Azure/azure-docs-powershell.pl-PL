---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: af4dbdbb2741850cdb01eb88e321f80a4844919a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708688"
---
# <span data-ttu-id="c279e-101">Get-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c279e-101">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="c279e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c279e-102">SYNOPSIS</span></span>
<span data-ttu-id="c279e-103">Pobiera właściwości elementów chronionych replikacji odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c279e-103">Gets the properties of an Azure Site Recovery Replication Protected Items.</span></span>

## <span data-ttu-id="c279e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c279e-104">SYNTAX</span></span>

### <span data-ttu-id="c279e-105">ByObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c279e-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrReplicationProtectedItem -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c279e-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="c279e-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrReplicationProtectedItem -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c279e-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="c279e-107">ByObjectWithFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrReplicationProtectedItem -FriendlyName <String>
 -ProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c279e-108">ByProtectableItemObject</span><span class="sxs-lookup"><span data-stu-id="c279e-108">ByProtectableItemObject</span></span>
```
Get-AzRecoveryServicesAsrReplicationProtectedItem -ProtectableItem <ASRProtectableItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c279e-109">Opis</span><span class="sxs-lookup"><span data-stu-id="c279e-109">DESCRIPTION</span></span>
<span data-ttu-id="c279e-110">Polecenie cmdlet **Get-AzRecoveryServicesAsrReplicationProtectedItem** pobiera właściwości wszystkich lub określonego elementu chronionego replikacji ASR z określonego kontenera ochrony przed ASR.</span><span class="sxs-lookup"><span data-stu-id="c279e-110">The **Get-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet gets the properties of all or the specified ASR replication protected item from the specified ASR protection container.</span></span>

## <span data-ttu-id="c279e-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c279e-111">EXAMPLES</span></span>

### <span data-ttu-id="c279e-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c279e-112">Example 1</span></span>
```
PS C:\> $ReplicationProtectedItems = Get-AzRecoveryServicesAsrReplicationProtectedItem -ProtectionContainer $PrimaryContainer
```

<span data-ttu-id="c279e-113">Wyświetla wszystkie elementy chronione replikacji w określonym kontenerze ochrony przed ASR.</span><span class="sxs-lookup"><span data-stu-id="c279e-113">Lists all replication protected items in the specified ASR protection container.</span></span>

## <span data-ttu-id="c279e-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c279e-114">PARAMETERS</span></span>

### <span data-ttu-id="c279e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c279e-115">-DefaultProfile</span></span>
<span data-ttu-id="c279e-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c279e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="c279e-117">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="c279e-117">-FriendlyName</span></span>
<span data-ttu-id="c279e-118">Określa przyjazną nazwę elementu chronionego replikacją, który należy pobrać.</span><span class="sxs-lookup"><span data-stu-id="c279e-118">Specifies the friendly name of the replication protected item to get.</span></span>

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

### <span data-ttu-id="c279e-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c279e-119">-Name</span></span>
<span data-ttu-id="c279e-120">Określa nazwę elementu chronionego replikacją, który ma zostać wyświetlony.</span><span class="sxs-lookup"><span data-stu-id="c279e-120">Specifies the name of the replication protected item to get.</span></span>

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

### <span data-ttu-id="c279e-121">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="c279e-121">-ProtectableItem</span></span>
<span data-ttu-id="c279e-122">Określa obiekt elementu z ochroną przed ASR.</span><span class="sxs-lookup"><span data-stu-id="c279e-122">Specifies an ASR protectable item object.</span></span> <span data-ttu-id="c279e-123">Polecenie cmdlet umożliwia pobieranie elementu chronionego replikacji ASR odpowiadającego określonemu elementowi umożliwiającemu ochronę przed ASR, jeśli element jest chroniony.</span><span class="sxs-lookup"><span data-stu-id="c279e-123">The cmdlet gets the ASR replication protected item corresponding to the specified ASR protectable item if the item is protected.</span></span>

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

### <span data-ttu-id="c279e-124">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="c279e-124">-ProtectionContainer</span></span>
<span data-ttu-id="c279e-125">Określa obiekt kontenera ochrony przed Autoodzyskiwaniem kontenera ochrony ASR, który odpowiada elementowi chronionej replikacji.</span><span class="sxs-lookup"><span data-stu-id="c279e-125">Specifies the ASR protection container object of the ASR protection container corresponding to the replication protected item.</span></span> 

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

### <span data-ttu-id="c279e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c279e-126">CommonParameters</span></span>
<span data-ttu-id="c279e-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c279e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c279e-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c279e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c279e-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c279e-129">INPUTS</span></span>

### <span data-ttu-id="c279e-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="c279e-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

### <span data-ttu-id="c279e-131">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="c279e-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="c279e-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c279e-132">OUTPUTS</span></span>

### <span data-ttu-id="c279e-133">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c279e-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="c279e-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c279e-134">NOTES</span></span>

## <span data-ttu-id="c279e-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c279e-135">RELATED LINKS</span></span>

[<span data-ttu-id="c279e-136">Nowe — AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c279e-136">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="c279e-137">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c279e-137">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="c279e-138">Set-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c279e-138">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzRecoveryServicesAsrReplicationProtectedItem.md)