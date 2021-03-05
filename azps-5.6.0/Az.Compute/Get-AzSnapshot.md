---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzSnapshot.md
ms.openlocfilehash: d66d8355636b31f82dac6c5560383d4749e5d696
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013905"
---
# <span data-ttu-id="59076-101">Get-AzSnapshot</span><span class="sxs-lookup"><span data-stu-id="59076-101">Get-AzSnapshot</span></span>

## <span data-ttu-id="59076-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59076-102">SYNOPSIS</span></span>
<span data-ttu-id="59076-103">Pobiera właściwości migawki</span><span class="sxs-lookup"><span data-stu-id="59076-103">Gets the properties of a snapshot</span></span>

## <span data-ttu-id="59076-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="59076-104">SYNTAX</span></span>

```
Get-AzSnapshot [[-ResourceGroupName] <String>] [[-SnapshotName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59076-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="59076-105">DESCRIPTION</span></span>
<span data-ttu-id="59076-106">Polecenie **cmdlet Get-AzSnapshot** pobiera właściwości migawki.</span><span class="sxs-lookup"><span data-stu-id="59076-106">The **Get-AzSnapshot** cmdlet gets the properties of a snapshot.</span></span>

## <span data-ttu-id="59076-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="59076-107">EXAMPLES</span></span>

### <span data-ttu-id="59076-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="59076-108">Example 1</span></span>
```
PS C:\> Get-AzSnapshot

ResourceGroupName  : ResourceGroupName1
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.SnapshotSku
TimeCreated        : 4/10/2018 7:05:42 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroupName1/providers/Microsoft.Compu
                     te/snapshots/SnapshotName1
Name               : SnapshotName1
Type               : Microsoft.Compute/snapshots
Location           : westus2
Tags               : {}

ResourceGroupName  : ResourceGroupName1
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.SnapshotSku
TimeCreated        : 4/10/2018 7:05:42 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroupName1/providers/Microsoft.Compu
                     te/snapshots/SnapshotName2
Name               : SnapshotName2
Type               : Microsoft.Compute/snapshots
Location           : westus2
Tags               : {}

ResourceGroupName  : ResourceGroupName2
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.SnapshotSku
TimeCreated        : 4/10/2018 7:05:42 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroupName2/providers/Microsoft.Compu
                     te/snapshots/SnapshotName3
Name               : SnapshotName3
Type               : Microsoft.Compute/snapshots
Location           : westus2
Tags               : {}
```

<span data-ttu-id="59076-109">To polecenie pobiera właściwości wszystkich migawek subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="59076-109">This command gets the properties of all snapshots of the subscription.</span></span>

### <span data-ttu-id="59076-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="59076-110">Example 2</span></span>
```
PS C:\> Get-AzSnapshot -ResourceGroupName "ResourceGroupName1"

ResourceGroupName  : ResourceGroupName1
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.SnapshotSku
TimeCreated        : 4/10/2018 7:05:42 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroupName1/providers/Microsoft.Compu
                     te/snapshots/SnapshotName1
Name               : SnapshotName1
Type               : Microsoft.Compute/snapshots
Location           : westus2
Tags               : {}

ResourceGroupName  : ResourceGroupName1
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.SnapshotSku
TimeCreated        : 4/10/2018 7:05:42 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroupName1/providers/Microsoft.Compu
                     te/snapshots/SnapshotName2
Name               : SnapshotName2
Type               : Microsoft.Compute/snapshots
Location           : westus2
Tags               : {}
```

<span data-ttu-id="59076-111">To polecenie pobiera właściwości wszystkich migawek w grupie zasobów o nazwie "ResourceGroupName1"</span><span class="sxs-lookup"><span data-stu-id="59076-111">This command gets the properties of all snapshots in the resource group named "ResourceGroupName1"</span></span>

### <span data-ttu-id="59076-112">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="59076-112">Example 3</span></span>
```
PS C:\> Get-AzSnapshot -ResourceGroupName "ResourceGroupName1" -SnapshotName "SnapshotName1"

ResourceGroupName  : ResourceGroupName1
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.SnapshotSku
TimeCreated        : 4/10/2018 7:05:42 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroupName1/providers/Microsoft.Compu
                     te/snapshots/SnapshotName1
Name               : SnapshotName1
Type               : Microsoft.Compute/snapshots
Location           : westus2
Tags               : {}
```

<span data-ttu-id="59076-113">To polecenie pobiera właściwości migawki o nazwie "SnapshotName1" w grupie zasobów o nazwie "ResourceGroupName1"</span><span class="sxs-lookup"><span data-stu-id="59076-113">This command gets the properties of the snapshot named "SnapshotName1" in the resource group named "ResourceGroupName1"</span></span>

### <span data-ttu-id="59076-114">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="59076-114">Example 4</span></span>
```
PS C:\> Get-AzSnapshot -SnapshotName "SnapshotName*"

ResourceGroupName  : ResourceGroupName1
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.SnapshotSku
TimeCreated        : 4/10/2018 7:05:42 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroupName1/providers/Microsoft.Compu
                     te/snapshots/SnapshotName1
Name               : SnapshotName1
Type               : Microsoft.Compute/snapshots
Location           : westus2
Tags               : {}

ResourceGroupName  : ResourceGroupName1
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.SnapshotSku
TimeCreated        : 4/10/2018 7:05:42 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroupName1/providers/Microsoft.Compu
                     te/snapshots/SnapshotName2
Name               : SnapshotName2
Type               : Microsoft.Compute/snapshots
Location           : westus2
Tags               : {}

ResourceGroupName  : ResourceGroupName2
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.SnapshotSku
TimeCreated        : 4/10/2018 7:05:42 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroupName2/providers/Microsoft.Compu
                     te/snapshots/SnapshotName3
Name               : SnapshotName3
Type               : Microsoft.Compute/snapshots
Location           : westus2
Tags               : {}
```

<span data-ttu-id="59076-115">To polecenie pobiera wszystkie migawki, które zaczynają się od "SnapshotName"</span><span class="sxs-lookup"><span data-stu-id="59076-115">This command gets all snapshots that start with "SnapshotName"</span></span>

## <span data-ttu-id="59076-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="59076-116">PARAMETERS</span></span>

### <span data-ttu-id="59076-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59076-117">-DefaultProfile</span></span>
<span data-ttu-id="59076-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="59076-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59076-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59076-119">-ResourceGroupName</span></span>
<span data-ttu-id="59076-120">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="59076-120">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="59076-121">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="59076-121">-SnapshotName</span></span>
<span data-ttu-id="59076-122">Określa nazwę migawki.</span><span class="sxs-lookup"><span data-stu-id="59076-122">Specifies the name of a snapshot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="59076-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59076-123">CommonParameters</span></span>
<span data-ttu-id="59076-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59076-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59076-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="59076-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59076-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="59076-126">INPUTS</span></span>

### <span data-ttu-id="59076-127">System.String</span><span class="sxs-lookup"><span data-stu-id="59076-127">System.String</span></span>

## <span data-ttu-id="59076-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="59076-128">OUTPUTS</span></span>

### <span data-ttu-id="59076-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="59076-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="59076-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="59076-130">NOTES</span></span>

## <span data-ttu-id="59076-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="59076-131">RELATED LINKS</span></span>
