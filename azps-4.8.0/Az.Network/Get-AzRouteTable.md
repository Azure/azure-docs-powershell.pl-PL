---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4F487FCA-930D-4D56-8D28-7693312E1A01
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteTable.md
ms.openlocfilehash: 613519f6d9d3d2d8ce1c83ff0ad5a2d9421859b8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94219505"
---
# <span data-ttu-id="301b0-101">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="301b0-101">Get-AzRouteTable</span></span>

## <span data-ttu-id="301b0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="301b0-102">SYNOPSIS</span></span>
<span data-ttu-id="301b0-103">Pobiera tabele tras.</span><span class="sxs-lookup"><span data-stu-id="301b0-103">Gets route tables.</span></span>

## <span data-ttu-id="301b0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="301b0-104">SYNTAX</span></span>

### <span data-ttu-id="301b0-105">NOEXPAND (domyślne)</span><span class="sxs-lookup"><span data-stu-id="301b0-105">NoExpand (Default)</span></span>
```
Get-AzRouteTable [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="301b0-106">Większa</span><span class="sxs-lookup"><span data-stu-id="301b0-106">Expand</span></span>
```
Get-AzRouteTable -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="301b0-107">Opis</span><span class="sxs-lookup"><span data-stu-id="301b0-107">DESCRIPTION</span></span>
<span data-ttu-id="301b0-108">Polecenie cmdlet **Get-AzRouteTable** pobiera tabele tras platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="301b0-108">The **Get-AzRouteTable** cmdlet gets Azure route tables.</span></span>
<span data-ttu-id="301b0-109">Możesz skorzystać z jednej tabeli routingu lub pobrać wszystkie tabele tras w grupie zasobów lub w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="301b0-109">You can get a single route table, or get all the route tables in a resource group or in your subscription.</span></span>

## <span data-ttu-id="301b0-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="301b0-110">EXAMPLES</span></span>

### <span data-ttu-id="301b0-111">Przykład 1: pobieranie tabeli tras</span><span class="sxs-lookup"><span data-stu-id="301b0-111">Example 1: Get a route table</span></span>
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

<span data-ttu-id="301b0-112">To polecenie pobiera tabelę tras o nazwie RouteTable01 w grupie zasobów o nazwie ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="301b0-112">This command gets the route table named RouteTable01 in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="301b0-113">Przykład 2: Lista tabel tras przy użyciu filtrowania</span><span class="sxs-lookup"><span data-stu-id="301b0-113">Example 2: List route tables using filtering</span></span>
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

<span data-ttu-id="301b0-114">To polecenie pobiera wszystkie tabele tras, których nazwa zaczyna się od tekstu "routed"</span><span class="sxs-lookup"><span data-stu-id="301b0-114">This command gets all route tables whose name starts with "RouteTable"</span></span>

## <span data-ttu-id="301b0-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="301b0-115">PARAMETERS</span></span>

### <span data-ttu-id="301b0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="301b0-116">-DefaultProfile</span></span>
<span data-ttu-id="301b0-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="301b0-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="301b0-118">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="301b0-118">-ExpandResource</span></span>
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

### <span data-ttu-id="301b0-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="301b0-119">-Name</span></span>
<span data-ttu-id="301b0-120">Określa nazwę tabeli routingu, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="301b0-120">Specifies the name of the route table that this cmdlet gets.</span></span>

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

### <span data-ttu-id="301b0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="301b0-121">-ResourceGroupName</span></span>
<span data-ttu-id="301b0-122">Określa nazwę grupy zasobów zawierającej tabele tras, które są dostępne w tym poleceniu cmdlet.</span><span class="sxs-lookup"><span data-stu-id="301b0-122">Specifies the name of the resource group that contains the route tables that this cmdlet gets.</span></span>

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

### <span data-ttu-id="301b0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="301b0-123">CommonParameters</span></span>
<span data-ttu-id="301b0-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="301b0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="301b0-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="301b0-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="301b0-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="301b0-126">INPUTS</span></span>

### <span data-ttu-id="301b0-127">System. String</span><span class="sxs-lookup"><span data-stu-id="301b0-127">System.String</span></span>

## <span data-ttu-id="301b0-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="301b0-128">OUTPUTS</span></span>

### <span data-ttu-id="301b0-129">Microsoft. Azure. Commands. Network. models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="301b0-129">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="301b0-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="301b0-130">NOTES</span></span>

## <span data-ttu-id="301b0-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="301b0-131">RELATED LINKS</span></span>

[<span data-ttu-id="301b0-132">Nowe — AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="301b0-132">New-AzRouteTable</span></span>](./New-AzRouteTable.md)

[<span data-ttu-id="301b0-133">Remove-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="301b0-133">Remove-AzRouteTable</span></span>](./Remove-AzRouteTable.md)

[<span data-ttu-id="301b0-134">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="301b0-134">Set-AzRouteTable</span></span>](./Set-AzRouteTable.md)


