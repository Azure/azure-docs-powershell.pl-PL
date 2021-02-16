---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 45D55DC9-0027-4EB9-B2F7-9ABF6685E6B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzAvailabilitySet.md
ms.openlocfilehash: d01919008adf8c15fa9b4a0c8144e279a3997a92
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195066"
---
# <span data-ttu-id="17090-101">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="17090-101">Get-AzAvailabilitySet</span></span>

## <span data-ttu-id="17090-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17090-102">SYNOPSIS</span></span>
<span data-ttu-id="17090-103">Pobiera zestawy dostępności platformy Azure w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="17090-103">Gets Azure availability sets in a resource group.</span></span>

## <span data-ttu-id="17090-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="17090-104">SYNTAX</span></span>

```
Get-AzAvailabilitySet [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17090-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="17090-105">DESCRIPTION</span></span>
<span data-ttu-id="17090-106">Polecenie **cmdlet Get-AzAvailabilitySet** pobiera zestawy dostępności platformy Azure w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="17090-106">The **Get-AzAvailabilitySet** cmdlet gets Azure availability sets in a resource group.</span></span>
<span data-ttu-id="17090-107">Możesz określić nazwę konkretnego zestawu dostępności do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="17090-107">You can specify the name of a specific availability set to get.</span></span>

## <span data-ttu-id="17090-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="17090-108">EXAMPLES</span></span>

### <span data-ttu-id="17090-109">Przykład 1. Uzyskiwanie określonego zestawu dostępności</span><span class="sxs-lookup"><span data-stu-id="17090-109">Example 1: Get a specific availability set</span></span>
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"

ResourceGroupName         : ResourceGroup11
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet03
Name                      : AvailabilitySet03
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []
```

<span data-ttu-id="17090-110">To polecenie pobiera zestaw dostępności o nazwie AvailabilitySet03 w grupie zasobów o nazwie ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="17090-110">This command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="17090-111">Przykład 2. Uzyskiwanie wszystkich zestawów dostępności</span><span class="sxs-lookup"><span data-stu-id="17090-111">Example 2: Get all availability sets</span></span>
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11"

ResourceGroupName         : ResourceGroup11
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet02
Name                      : AvailabilitySet02
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []


ResourceGroupName         : ResourceGroup11
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet03
Name                      : AvailabilitySet03
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []

ResourceGroupName         : ResourceGroup11
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet10
Name                      : AvailabilitySet10
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []
```

<span data-ttu-id="17090-112">To polecenie pobiera wszystkie zestawy dostępności w grupie zasobów o nazwie Grupa Zasobów11.</span><span class="sxs-lookup"><span data-stu-id="17090-112">This command gets all the availability sets in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="17090-113">Przykład 3. Uzyskiwanie wszystkich zestawów dostępności za pomocą filtrowania</span><span class="sxs-lookup"><span data-stu-id="17090-113">Example 3: Get all availability sets with filtering</span></span>
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup1*" -Name "AvailabilitySet0*"

ResourceGroupName         : ResourceGroup11
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet02
Name                      : AvailabilitySet02
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []


ResourceGroupName         : ResourceGroup11
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet03
Name                      : AvailabilitySet03
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []
```

<span data-ttu-id="17090-114">To polecenie pobiera wszystkie zestawy dostępności w grupie zasobów o nazwie ResourceGroup11, których nazwy zaczynają się od "AvailabilitySet0".</span><span class="sxs-lookup"><span data-stu-id="17090-114">This command gets all the availability sets in the resource group named ResourceGroup11 that start with "AvailabilitySet0".</span></span>

### <span data-ttu-id="17090-115">Przykład 4. Uzyskiwanie wszystkich zestawów dostępności z nazwą rozpoczynającą się od zestawu dostępności</span><span class="sxs-lookup"><span data-stu-id="17090-115">Example 4: Get all availability sets with name starting with AvailabilitySet0</span></span>
```
PS C:\> Get-AzAvailabilitySet -Name AvailabilitySet0*

ResourceGroupName         : ResourceGroup11
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet02
Name                      : AvailabilitySet02
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []


ResourceGroupName         : ResourceGroup12
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup12/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet03
Name                      : AvailabilitySet03
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []
```

<span data-ttu-id="17090-116">To polecenie pobiera wszystkie zestawy dostępności, które zaczynają się od "AvailabilitySet0".</span><span class="sxs-lookup"><span data-stu-id="17090-116">This command gets all the availability sets that start with "AvailabilitySet0".</span></span>

## <span data-ttu-id="17090-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="17090-117">PARAMETERS</span></span>

### <span data-ttu-id="17090-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17090-118">-DefaultProfile</span></span>
<span data-ttu-id="17090-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="17090-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="17090-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="17090-120">-Name</span></span>
<span data-ttu-id="17090-121">Określa nazwę zestawu dostępności, który otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17090-121">Specifies the name of an availability set that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="17090-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17090-122">-ResourceGroupName</span></span>
<span data-ttu-id="17090-123">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="17090-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="17090-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17090-124">CommonParameters</span></span>
<span data-ttu-id="17090-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17090-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17090-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="17090-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17090-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="17090-127">INPUTS</span></span>

### <span data-ttu-id="17090-128">System.String</span><span class="sxs-lookup"><span data-stu-id="17090-128">System.String</span></span>

## <span data-ttu-id="17090-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="17090-129">OUTPUTS</span></span>

### <span data-ttu-id="17090-130">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="17090-130">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="17090-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="17090-131">NOTES</span></span>

## <span data-ttu-id="17090-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="17090-132">RELATED LINKS</span></span>

[<span data-ttu-id="17090-133">New-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="17090-133">New-AzAvailabilitySet</span></span>](./New-AzAvailabilitySet.md)

[<span data-ttu-id="17090-134">Remove-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="17090-134">Remove-AzAvailabilitySet</span></span>](./Remove-AzAvailabilitySet.md)


