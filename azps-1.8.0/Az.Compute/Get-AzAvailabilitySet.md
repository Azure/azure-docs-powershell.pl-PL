---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 45D55DC9-0027-4EB9-B2F7-9ABF6685E6B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzAvailabilitySet.md
ms.openlocfilehash: 1ebb43f11d0286ca3fef4ab136c9e5a1e6ee031d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710329"
---
# <span data-ttu-id="47fc7-101">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="47fc7-101">Get-AzAvailabilitySet</span></span>

## <span data-ttu-id="47fc7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="47fc7-102">SYNOPSIS</span></span>
<span data-ttu-id="47fc7-103">Pobiera zestawy dostępności platformy Azure w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="47fc7-103">Gets Azure availability sets in a resource group.</span></span>

## <span data-ttu-id="47fc7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="47fc7-104">SYNTAX</span></span>

```
Get-AzAvailabilitySet [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47fc7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="47fc7-105">DESCRIPTION</span></span>
<span data-ttu-id="47fc7-106">Polecenie cmdlet **Get-AzAvailabilitySet** pobiera zestawy dostępności platformy Azure w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="47fc7-106">The **Get-AzAvailabilitySet** cmdlet gets Azure availability sets in a resource group.</span></span>
<span data-ttu-id="47fc7-107">Możesz określić nazwę określonego zestawu dostępności, aby uzyskać dostęp.</span><span class="sxs-lookup"><span data-stu-id="47fc7-107">You can specify the name of a specific availability set to get.</span></span>

## <span data-ttu-id="47fc7-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="47fc7-108">EXAMPLES</span></span>

### <span data-ttu-id="47fc7-109">Przykład 1: uzyskiwanie określonego zestawu dostępności</span><span class="sxs-lookup"><span data-stu-id="47fc7-109">Example 1: Get a specific availability set</span></span>
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

<span data-ttu-id="47fc7-110">To polecenie pobiera zestaw dostępności o nazwie AvailablitySet03 w grupie zasobów o nazwie ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="47fc7-110">This command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="47fc7-111">Przykład 2: pobieranie wszystkich zestawów dostępności</span><span class="sxs-lookup"><span data-stu-id="47fc7-111">Example 2: Get all availability sets</span></span>
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

<span data-ttu-id="47fc7-112">To polecenie pobiera wszystkie zestawy dostępności w grupie zasobów o nazwie ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="47fc7-112">This command gets all the availability sets in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="47fc7-113">Przykład 3: pobieranie wszystkich zestawów dostępności przy użyciu filtrowania</span><span class="sxs-lookup"><span data-stu-id="47fc7-113">Example 3: Get all availability sets with filtering</span></span>
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

<span data-ttu-id="47fc7-114">To polecenie pobiera wszystkie zestawy dostępności w grupie zasobów o nazwie ResourceGroup11, których nazwa rozpoczyna się od "AvailabilitySet0".</span><span class="sxs-lookup"><span data-stu-id="47fc7-114">This command gets all the availability sets in the resource group named ResourceGroup11 that start with "AvailabilitySet0".</span></span>

### <span data-ttu-id="47fc7-115">Przykład 4: pobieranie wszystkich zestawów dostępności o nazwie rozpoczynającej się od AvailabilitySet0</span><span class="sxs-lookup"><span data-stu-id="47fc7-115">Example 4: Get all availability sets with name starting with AvailabilitySet0</span></span>
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

<span data-ttu-id="47fc7-116">To polecenie pobiera wszystkie zestawy dostępności rozpoczynające się od "AvailabilitySet0".</span><span class="sxs-lookup"><span data-stu-id="47fc7-116">This command gets all the availability sets that start with "AvailabilitySet0".</span></span>

## <span data-ttu-id="47fc7-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="47fc7-117">PARAMETERS</span></span>

### <span data-ttu-id="47fc7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47fc7-118">-DefaultProfile</span></span>
<span data-ttu-id="47fc7-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="47fc7-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47fc7-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="47fc7-120">-Name</span></span>
<span data-ttu-id="47fc7-121">Określa nazwę zestawu dostępności, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47fc7-121">Specifies the name of an availability set that this cmdlet gets.</span></span>

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

### <span data-ttu-id="47fc7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47fc7-122">-ResourceGroupName</span></span>
<span data-ttu-id="47fc7-123">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="47fc7-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="47fc7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47fc7-124">CommonParameters</span></span>
<span data-ttu-id="47fc7-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47fc7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47fc7-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="47fc7-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47fc7-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="47fc7-127">INPUTS</span></span>

### <span data-ttu-id="47fc7-128">System. String</span><span class="sxs-lookup"><span data-stu-id="47fc7-128">System.String</span></span>

## <span data-ttu-id="47fc7-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="47fc7-129">OUTPUTS</span></span>

### <span data-ttu-id="47fc7-130">Microsoft. Azure. Commands. COMPUTE. models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="47fc7-130">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="47fc7-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="47fc7-131">NOTES</span></span>

## <span data-ttu-id="47fc7-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="47fc7-132">RELATED LINKS</span></span>

[<span data-ttu-id="47fc7-133">Nowe — AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="47fc7-133">New-AzAvailabilitySet</span></span>](./New-AzAvailabilitySet.md)

[<span data-ttu-id="47fc7-134">Remove-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="47fc7-134">Remove-AzAvailabilitySet</span></span>](./Remove-AzAvailabilitySet.md)


