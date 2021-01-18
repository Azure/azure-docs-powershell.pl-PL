---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskAccess.md
ms.openlocfilehash: 69f83b7c98850ba74476e6d81803e748f48bea6a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504138"
---
# <span data-ttu-id="e36cd-101">Get-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="e36cd-101">Get-AzDiskAccess</span></span>

## <span data-ttu-id="e36cd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e36cd-102">SYNOPSIS</span></span>
<span data-ttu-id="e36cd-103">Pobiera właściwości dostępu do dysku</span><span class="sxs-lookup"><span data-stu-id="e36cd-103">Gets the properties of Disk Accesses</span></span>

## <span data-ttu-id="e36cd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e36cd-104">SYNTAX</span></span>

### <span data-ttu-id="e36cd-105">DefaultParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e36cd-105">DefaultParameterSet (Default)</span></span>
```
Get-AzDiskAccess [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e36cd-106">ResourceIDParameterSet</span><span class="sxs-lookup"><span data-stu-id="e36cd-106">ResourceIDParameterSet</span></span>
```
Get-AzDiskAccess [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e36cd-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e36cd-107">DESCRIPTION</span></span>
<span data-ttu-id="e36cd-108">Polecenie cmdlet **Get-AzDiskAccess** pobiera właściwości dostępu do dysku</span><span class="sxs-lookup"><span data-stu-id="e36cd-108">The **Get-AzDiskAccess** cmdlet gets the properties of Disk Accesses</span></span>

## <span data-ttu-id="e36cd-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e36cd-109">EXAMPLES</span></span>

### <span data-ttu-id="e36cd-110">Przykład 1: Używanie domyślnego zestawu parametrów</span><span class="sxs-lookup"><span data-stu-id="e36cd-110">Example 1: Using Default Parameter Set</span></span> 
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

<span data-ttu-id="e36cd-111">To polecenie pobiera właściwości zasobu dostępu do dysku o nazwie "DiskAccess01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="e36cd-111">This command gets the properties of a Disk Access resource named 'DiskAccess01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="e36cd-112">Przykład 2: Get-AzDiskAccess według grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="e36cd-112">Example 2: Get-AzDiskAccess by Resource Group</span></span>
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

<span data-ttu-id="e36cd-113">To polecenie pobiera właściwości wszystkich operacji dostępu do dysku w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="e36cd-113">This command gets the properties of all disk accesses in the resource group 'ResourceGroup01'.</span></span>


### <span data-ttu-id="e36cd-114">Przykład 3: uzyskiwanie dostępu do wszystkich dysków</span><span class="sxs-lookup"><span data-stu-id="e36cd-114">Example 3: Getting all Disk Access</span></span>
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

<span data-ttu-id="e36cd-115">To polecenie pobiera właściwości wszystkich odpraw dostępu do dysku w ramach abonamentu.</span><span class="sxs-lookup"><span data-stu-id="e36cd-115">This command gets the properties of all disk accesses under the subscription.</span></span>

### <span data-ttu-id="e36cd-116">Przykład 4: uzyskiwanie dostępu do wszystkich dysków za pomocą znaku wieloznacznego</span><span class="sxs-lookup"><span data-stu-id="e36cd-116">Example 4: Get all Disk Access using Wildcard Character</span></span>
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

<span data-ttu-id="e36cd-117">To polecenie pobiera właściwości wszystkich dostępów do dysku pod nazwą subskrypcji rozpoczynającą się od "DiskAccessMicrosoft".</span><span class="sxs-lookup"><span data-stu-id="e36cd-117">This command gets the properties of all disk accesses under the subscription name starting with 'DiskAccessMicrosoft'.</span></span>

### <span data-ttu-id="e36cd-118">Przykład 5: uzyskaj dostęp do dysku przy użyciu ResourceId.</span><span class="sxs-lookup"><span data-stu-id="e36cd-118">Example 5: Get Disk Access using ResourceId.</span></span>
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

<span data-ttu-id="e36cd-119">To polecenie pobiera właściwości dostępu do dysku z danym identyfikatorem ResourceId.</span><span class="sxs-lookup"><span data-stu-id="e36cd-119">This command gets the properties of a Disk Access with the given ResourceId.</span></span>


## <span data-ttu-id="e36cd-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e36cd-120">PARAMETERS</span></span>

### <span data-ttu-id="e36cd-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e36cd-121">-DefaultProfile</span></span>
<span data-ttu-id="e36cd-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e36cd-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e36cd-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e36cd-123">-Name</span></span>
<span data-ttu-id="e36cd-124">Określa nazwę dostępu do dysku.</span><span class="sxs-lookup"><span data-stu-id="e36cd-124">Specifies the name of a disk access.</span></span>

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

### <span data-ttu-id="e36cd-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e36cd-125">-ResourceGroupName</span></span>
<span data-ttu-id="e36cd-126">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e36cd-126">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="e36cd-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e36cd-127">-ResourceId</span></span>
<span data-ttu-id="e36cd-128">Identyfikator zasobu w celu uzyskania dostępu do dysku.</span><span class="sxs-lookup"><span data-stu-id="e36cd-128">Resource ID for your disk access.</span></span>

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

### <span data-ttu-id="e36cd-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e36cd-129">CommonParameters</span></span>
<span data-ttu-id="e36cd-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e36cd-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e36cd-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e36cd-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e36cd-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e36cd-132">INPUTS</span></span>

### <span data-ttu-id="e36cd-133">System. String</span><span class="sxs-lookup"><span data-stu-id="e36cd-133">System.String</span></span>

## <span data-ttu-id="e36cd-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e36cd-134">OUTPUTS</span></span>

### <span data-ttu-id="e36cd-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span><span class="sxs-lookup"><span data-stu-id="e36cd-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span></span>

## <span data-ttu-id="e36cd-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e36cd-136">NOTES</span></span>

## <span data-ttu-id="e36cd-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e36cd-137">RELATED LINKS</span></span>
