---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskAccess.md
ms.openlocfilehash: 69f83b7c98850ba74476e6d81803e748f48bea6a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969354"
---
# <span data-ttu-id="b399d-101">Get-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="b399d-101">Get-AzDiskAccess</span></span>

## <span data-ttu-id="b399d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b399d-102">SYNOPSIS</span></span>
<span data-ttu-id="b399d-103">Pobiera właściwości dostępu do dysku</span><span class="sxs-lookup"><span data-stu-id="b399d-103">Gets the properties of Disk Accesses</span></span>

## <span data-ttu-id="b399d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b399d-104">SYNTAX</span></span>

### <span data-ttu-id="b399d-105">DefaultParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="b399d-105">DefaultParameterSet (Default)</span></span>
```
Get-AzDiskAccess [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b399d-106">ResourceIDParameterSet</span><span class="sxs-lookup"><span data-stu-id="b399d-106">ResourceIDParameterSet</span></span>
```
Get-AzDiskAccess [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b399d-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="b399d-107">DESCRIPTION</span></span>
<span data-ttu-id="b399d-108">Polecenie **cmdlet Get-AzAccess** pobiera właściwości dostępu dysku</span><span class="sxs-lookup"><span data-stu-id="b399d-108">The **Get-AzDiskAccess** cmdlet gets the properties of Disk Accesses</span></span>

## <span data-ttu-id="b399d-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b399d-109">EXAMPLES</span></span>

### <span data-ttu-id="b399d-110">Przykład 1. Używanie domyślnego zestawu parametrów</span><span class="sxs-lookup"><span data-stu-id="b399d-110">Example 1: Using Default Parameter Set</span></span> 
```
PS C:\> Get-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -Name 'DiskAccess01'

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:02:50 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccess01
Name                       : DiskAccess01
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}
```

<span data-ttu-id="b399d-111">To polecenie pobiera właściwości zasobu dostępu do dysku o nazwie "DiskAccess01" w grupie zasobów "Grupa Zasobów01".</span><span class="sxs-lookup"><span data-stu-id="b399d-111">This command gets the properties of a Disk Access resource named 'DiskAccess01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="b399d-112">Przykład 2. Get-AzDiskAccess według grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="b399d-112">Example 2: Get-AzDiskAccess by Resource Group</span></span>
```
PS C:\> Get-AzDiskAccess -ResourceGroupName 'ResourceGroup01'

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:02:50 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccess01
Name                       : DiskAccess01
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:05:19 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccess02
Name                       : DiskAccess02
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}
```

<span data-ttu-id="b399d-113">To polecenie pobiera właściwości wszystkich dostępu do dysku w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="b399d-113">This command gets the properties of all disk accesses in the resource group 'ResourceGroup01'.</span></span>


### <span data-ttu-id="b399d-114">Przykład 3. Uzyskiwanie dostępu do wszystkich dysków</span><span class="sxs-lookup"><span data-stu-id="b399d-114">Example 3: Getting all Disk Access</span></span>
```
PS C:\> Get-AzDiskAccess

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:02:50 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccess01
Name                       : DiskAccess01
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:05:19 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup21/providers/Microsoft.Compute/diskAccesses/DiskAccess02
Name                       : DiskAccess02
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:05:19 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup08/providers/Microsoft.Compute/diskAccesses/DiskAccess03
Name                       : DiskAccess03
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}
```

<span data-ttu-id="b399d-115">To polecenie pobiera właściwości wszystkich dostępu do dysku w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="b399d-115">This command gets the properties of all disk accesses under the subscription.</span></span>

### <span data-ttu-id="b399d-116">Przykład 4. Uzyskiwanie dostępu do całego dysku przy użyciu symboli wieloznacznych</span><span class="sxs-lookup"><span data-stu-id="b399d-116">Example 4: Get all Disk Access using Wildcard Character</span></span>
```
PS C:\> Get-AzDiskAccess -Name DiskAccessMicrosoft*

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:02:50 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccessMicrosoftAzure
Name                       : DiskAccessMicrosoftAzure
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:05:19 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccessMicrosoftTeams
Name                       : DiskAccessMicrosoftTeams
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}
```

<span data-ttu-id="b399d-117">To polecenie pobiera właściwości wszystkich dostępu do dysku pod nazwą subskrypcji, zaczynając od "DiskAccessMicrosoft".</span><span class="sxs-lookup"><span data-stu-id="b399d-117">This command gets the properties of all disk accesses under the subscription name starting with 'DiskAccessMicrosoft'.</span></span>

### <span data-ttu-id="b399d-118">Przykład 5. Uzyskiwanie dostępu do dysku przy użyciu funkcji ResourceId.</span><span class="sxs-lookup"><span data-stu-id="b399d-118">Example 5: Get Disk Access using ResourceId.</span></span>
```
PS C:\> Get-AzDiskAccess -ResourceId '/subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccess01'

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:02:50 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccess01
Name                       : DiskAccess01
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}
```

<span data-ttu-id="b399d-119">To polecenie pobiera właściwości dostępu do dysku z danym polem ResourceId.</span><span class="sxs-lookup"><span data-stu-id="b399d-119">This command gets the properties of a Disk Access with the given ResourceId.</span></span>


## <span data-ttu-id="b399d-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b399d-120">PARAMETERS</span></span>

### <span data-ttu-id="b399d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b399d-121">-DefaultProfile</span></span>
<span data-ttu-id="b399d-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b399d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b399d-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b399d-123">-Name</span></span>
<span data-ttu-id="b399d-124">Określa nazwę dostępu do dysku.</span><span class="sxs-lookup"><span data-stu-id="b399d-124">Specifies the name of a disk access.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases: diskAccessName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="b399d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b399d-125">-ResourceGroupName</span></span>
<span data-ttu-id="b399d-126">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b399d-126">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="b399d-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b399d-127">-ResourceId</span></span>
<span data-ttu-id="b399d-128">Identyfikator zasobu dla dostępu do dysku.</span><span class="sxs-lookup"><span data-stu-id="b399d-128">Resource ID for your disk access.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIDParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b399d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b399d-129">CommonParameters</span></span>
<span data-ttu-id="b399d-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b399d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b399d-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b399d-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b399d-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b399d-132">INPUTS</span></span>

### <span data-ttu-id="b399d-133">System.String</span><span class="sxs-lookup"><span data-stu-id="b399d-133">System.String</span></span>

## <span data-ttu-id="b399d-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b399d-134">OUTPUTS</span></span>

### <span data-ttu-id="b399d-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span><span class="sxs-lookup"><span data-stu-id="b399d-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span></span>

## <span data-ttu-id="b399d-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b399d-136">NOTES</span></span>

## <span data-ttu-id="b399d-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b399d-137">RELATED LINKS</span></span>
