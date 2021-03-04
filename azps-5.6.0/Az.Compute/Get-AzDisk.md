---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDisk.md
ms.openlocfilehash: 58b5e0aad0982b08256694f842e55929ca7dfcc8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969370"
---
# <span data-ttu-id="58edc-101">Get-AzDisk</span><span class="sxs-lookup"><span data-stu-id="58edc-101">Get-AzDisk</span></span>

## <span data-ttu-id="58edc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58edc-102">SYNOPSIS</span></span>
<span data-ttu-id="58edc-103">Pobiera właściwości dysku zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="58edc-103">Gets the properties of a Managed disk.</span></span>

## <span data-ttu-id="58edc-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="58edc-104">SYNTAX</span></span>

```
Get-AzDisk [[-ResourceGroupName] <String>] [[-DiskName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="58edc-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="58edc-105">DESCRIPTION</span></span>
<span data-ttu-id="58edc-106">Polecenie **cmdlet Get-AzCm** pobiera właściwości dysku zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="58edc-106">The **Get-AzDisk** cmdlet gets the properties of a Managed disk.</span></span>

## <span data-ttu-id="58edc-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="58edc-107">EXAMPLES</span></span>

### <span data-ttu-id="58edc-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="58edc-108">Example 1</span></span>
```
PS C:\> Get-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'

ResourceGroupName  : ResourceGroup01
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.DiskSku
Zones              :
TimeCreated        : 6/29/2018 4:26:27 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
DiskIOPSReadWrite  : 500
DiskMBpsReadWrite  : 100
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compu
                     te/disks/Disk01
Name               : Disk01
Type               : Microsoft.Compute/disks
Location           : westus2
Tags               : {}
```

<span data-ttu-id="58edc-109">To polecenie pobiera właściwości dysku o nazwie "Dysk01" w grupie zasobów "Grupa zasobów01".</span><span class="sxs-lookup"><span data-stu-id="58edc-109">This command gets the properties of the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="58edc-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="58edc-110">Example 2</span></span>
```
PS C:\> Get-AzDisk -ResourceGroupName 'ResourceGroup01'

ResourceGroupName  : ResourceGroup01
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.DiskSku
Zones              :
TimeCreated        : 6/29/2018 4:26:27 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
DiskIOPSReadWrite  : 500
DiskMBpsReadWrite  : 100
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compu
                     te/disks/win1_OsDisk_1
Name               : win1_OsDisk_1
Type               : Microsoft.Compute/disks
Location           : westus2
Tags               : {}

ResourceGroupName  : ResourceGroup01
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.DiskSku
Zones              :
TimeCreated        : 6/29/2018 4:27:27 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
DiskIOPSReadWrite  : 500
DiskMBpsReadWrite  : 100
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compu
                     te/disks/win1_OsDisk_2
Name               : win1_OsDisk_2
Type               : Microsoft.Compute/disks
Location           : westus2
Tags               : {}
```

<span data-ttu-id="58edc-111">To polecenie pobiera właściwości wszystkich dysków w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="58edc-111">This command gets the properties of all disks in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="58edc-112">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="58edc-112">Example 3</span></span>
```
PS C:\> Get-AzDisk

ResourceGroupName  : ResourceGroup01
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.DiskSku
Zones              :
TimeCreated        : 6/29/2018 4:26:27 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
DiskIOPSReadWrite  : 500
DiskMBpsReadWrite  : 100
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compu
                     te/disks/win1_OsDisk_1
Name               : win1_OsDisk_1
Type               : Microsoft.Compute/disks
Location           : westus2
Tags               : {}

ResourceGroupName  : ResourceGroup02
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.DiskSku
Zones              :
TimeCreated        : 6/29/2018 4:27:27 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
DiskIOPSReadWrite  : 500
DiskMBpsReadWrite  : 100
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup02/providers/Microsoft.Compu
                     te/disks/win1_OsDisk_2
Name               : win1_OsDisk_2
Type               : Microsoft.Compute/disks
Location           : westus2
Tags               : {}
```

<span data-ttu-id="58edc-113">To polecenie pobiera właściwości wszystkich dysków w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="58edc-113">This command gets the properties of all disks under the subscription.</span></span>

### <span data-ttu-id="58edc-114">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="58edc-114">Example 4</span></span>
```
PS C:\> Get-AzDisk -Name win_OsDisk*

ResourceGroupName  : ResourceGroup01
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.DiskSku
Zones              :
TimeCreated        : 6/29/2018 4:26:27 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
DiskIOPSReadWrite  : 500
DiskMBpsReadWrite  : 100
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compu
                     te/disks/win1_OsDisk_1
Name               : win1_OsDisk_1
Type               : Microsoft.Compute/disks
Location           : westus2
Tags               : {}

ResourceGroupName  : ResourceGroup02
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.DiskSku
Zones              :
TimeCreated        : 6/29/2018 4:27:27 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
DiskIOPSReadWrite  : 500
DiskMBpsReadWrite  : 100
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup02/providers/Microsoft.Compu
                     te/disks/win1_OsDisk_2
Name               : win1_OsDisk_2
Type               : Microsoft.Compute/disks
Location           : westus2
Tags               : {}
```

<span data-ttu-id="58edc-115">To polecenie pobiera właściwości wszystkich dysków pod nazwą subskrypcji, zaczynając od win1_OsDisk.</span><span class="sxs-lookup"><span data-stu-id="58edc-115">This command gets the properties of all disks under the subscription name starting with win1_OsDisk.</span></span>

## <span data-ttu-id="58edc-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="58edc-116">PARAMETERS</span></span>

### <span data-ttu-id="58edc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58edc-117">-DefaultProfile</span></span>
<span data-ttu-id="58edc-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="58edc-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58edc-119">-DiskName</span><span class="sxs-lookup"><span data-stu-id="58edc-119">-DiskName</span></span>
<span data-ttu-id="58edc-120">Określa nazwę dysku.</span><span class="sxs-lookup"><span data-stu-id="58edc-120">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="58edc-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58edc-121">-ResourceGroupName</span></span>
<span data-ttu-id="58edc-122">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="58edc-122">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="58edc-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58edc-123">CommonParameters</span></span>
<span data-ttu-id="58edc-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58edc-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58edc-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="58edc-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58edc-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="58edc-126">INPUTS</span></span>

### <span data-ttu-id="58edc-127">System.String</span><span class="sxs-lookup"><span data-stu-id="58edc-127">System.String</span></span>

## <span data-ttu-id="58edc-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="58edc-128">OUTPUTS</span></span>

### <span data-ttu-id="58edc-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="58edc-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="58edc-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="58edc-130">NOTES</span></span>

## <span data-ttu-id="58edc-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="58edc-131">RELATED LINKS</span></span>
