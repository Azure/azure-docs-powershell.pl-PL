---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4F487FCA-930D-4D56-8D28-7693312E1A01
online version: https://docs.microsoft.com/powershell/module/az.network/get-azroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteTable.md
ms.openlocfilehash: 67223e7ac85fa4bf88d2cd275d3d1a032e249edf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954049"
---
# <span data-ttu-id="dd493-101">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="dd493-101">Get-AzRouteTable</span></span>

## <span data-ttu-id="dd493-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd493-102">SYNOPSIS</span></span>
<span data-ttu-id="dd493-103">Pobiera tabele tras.</span><span class="sxs-lookup"><span data-stu-id="dd493-103">Gets route tables.</span></span>

## <span data-ttu-id="dd493-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="dd493-104">SYNTAX</span></span>

### <span data-ttu-id="dd493-105">NoExpand (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="dd493-105">NoExpand (Default)</span></span>
```
Get-AzRouteTable [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dd493-106">Rozwiń</span><span class="sxs-lookup"><span data-stu-id="dd493-106">Expand</span></span>
```
Get-AzRouteTable -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd493-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="dd493-107">DESCRIPTION</span></span>
<span data-ttu-id="dd493-108">Polecenie **cmdlet Get-AzRouteTable** pobiera tabele tras platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="dd493-108">The **Get-AzRouteTable** cmdlet gets Azure route tables.</span></span>
<span data-ttu-id="dd493-109">Możesz pobrać jedną tabelę trasy lub pobrać wszystkie tabele tras w grupie zasobów lub w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="dd493-109">You can get a single route table, or get all the route tables in a resource group or in your subscription.</span></span>

## <span data-ttu-id="dd493-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="dd493-110">EXAMPLES</span></span>

### <span data-ttu-id="dd493-111">Przykład 1. Uzyskiwanie tabeli tras</span><span class="sxs-lookup"><span data-stu-id="dd493-111">Example 1: Get a route table</span></span>
```
PS C:\> Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01"

Name              : routetable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/routetable01
Etag              : W/"db5f4e12-3f34-465b-92dd-0ab3bf6fc274"
ProvisioningState : Succeeded
Tags              : 
Routes            : [
                      {
                        "Name": "route07",
                        "Etag": "W/\"db5f4e12-3f34-465b-92dd-0ab3bf6fc274\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/routetable01/routes/route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      }
                    ] 
Subnets           : []
```

<span data-ttu-id="dd493-112">To polecenie pobiera tabelę tras o nazwie RouteTable01 w grupie zasobów o nazwie ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="dd493-112">This command gets the route table named RouteTable01 in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="dd493-113">Przykład 2. Lista tabel tras przy użyciu filtrowania</span><span class="sxs-lookup"><span data-stu-id="dd493-113">Example 2: List route tables using filtering</span></span>
```
PS C:\> Get-AzRouteTable -Name RouteTable*

Name              : routetable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/routetable01
Etag              : W/"db5f4e12-3f34-465b-92dd-0ab3bf6fc274"
ProvisioningState : Succeeded
Tags              : 
Routes            : [
                      {
                        "Name": "route07",
                        "Etag": "W/\"db5f4e12-3f34-465b-92dd-0ab3bf6fc274\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/routetable01/routes/route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      }
                    ] 
Subnets           : []

Name              : routetable02
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/routetable02
Etag              : W/"db5f4e12-3f34-465b-92dd-0ab3bf6fc274"
ProvisioningState : Succeeded
Tags              : 
Routes            : [
                      {
                        "Name": "route07",
                        "Etag": "W/\"db5f4e12-3f34-465b-92dd-0ab3bf6fc274\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/routetable02/routes/route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      }
                    ] 
Subnets           : []
```

<span data-ttu-id="dd493-114">To polecenie pobiera wszystkie tabele tras, których nazwa zaczyna się od "RouteTable"</span><span class="sxs-lookup"><span data-stu-id="dd493-114">This command gets all route tables whose name starts with "RouteTable"</span></span>

## <span data-ttu-id="dd493-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dd493-115">PARAMETERS</span></span>

### <span data-ttu-id="dd493-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd493-116">-DefaultProfile</span></span>
<span data-ttu-id="dd493-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="dd493-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd493-118">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="dd493-118">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd493-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="dd493-119">-Name</span></span>
<span data-ttu-id="dd493-120">Określa nazwę tabeli trasy, która będzie pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd493-120">Specifies the name of the route table that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="dd493-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd493-121">-ResourceGroupName</span></span>
<span data-ttu-id="dd493-122">Określa nazwę grupy zasobów zawierającej tabele tras, które otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd493-122">Specifies the name of the resource group that contains the route tables that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="dd493-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd493-123">CommonParameters</span></span>
<span data-ttu-id="dd493-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd493-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd493-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dd493-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd493-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dd493-126">INPUTS</span></span>

### <span data-ttu-id="dd493-127">System.String</span><span class="sxs-lookup"><span data-stu-id="dd493-127">System.String</span></span>

## <span data-ttu-id="dd493-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dd493-128">OUTPUTS</span></span>

### <span data-ttu-id="dd493-129">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="dd493-129">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="dd493-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="dd493-130">NOTES</span></span>

## <span data-ttu-id="dd493-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dd493-131">RELATED LINKS</span></span>

[<span data-ttu-id="dd493-132">New-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="dd493-132">New-AzRouteTable</span></span>](./New-AzRouteTable.md)

[<span data-ttu-id="dd493-133">Remove-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="dd493-133">Remove-AzRouteTable</span></span>](./Remove-AzRouteTable.md)

[<span data-ttu-id="dd493-134">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="dd493-134">Set-AzRouteTable</span></span>](./Set-AzRouteTable.md)


