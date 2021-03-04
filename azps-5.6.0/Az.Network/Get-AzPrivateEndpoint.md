---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpoint.md
ms.openlocfilehash: 09bd7f919b953c4df09293a75c2c893df4a01b96
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954225"
---
# <span data-ttu-id="ef619-101">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="ef619-101">Get-AzPrivateEndpoint</span></span>

## <span data-ttu-id="ef619-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef619-102">SYNOPSIS</span></span>
<span data-ttu-id="ef619-103">Uzyskiwanie prywatnego punktu końcowego</span><span class="sxs-lookup"><span data-stu-id="ef619-103">Get a private endpoint</span></span>

## <span data-ttu-id="ef619-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ef619-104">SYNTAX</span></span>

### <span data-ttu-id="ef619-105">NoExpand (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="ef619-105">NoExpand (Default)</span></span>
```
Get-AzPrivateEndpoint [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ef619-106">Rozwiń</span><span class="sxs-lookup"><span data-stu-id="ef619-106">Expand</span></span>
```
Get-AzPrivateEndpoint -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef619-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="ef619-107">DESCRIPTION</span></span>
<span data-ttu-id="ef619-108">Polecenie **cmdlet Get-AzPrivateEndpoint** pobiera co najmniej jeden prywatny punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="ef619-108">The **Get-AzPrivateEndpoint** cmdlet gets one or more private endpoints.</span></span>

## <span data-ttu-id="ef619-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ef619-109">EXAMPLES</span></span>

### <span data-ttu-id="ef619-110">Przykład 1. Pobieranie prywatnego punktu końcowego</span><span class="sxs-lookup"><span data-stu-id="ef619-110">Example 1: Retrieve a private endpoint</span></span>
```powershell
Get-AzPrivateEndpoint -Name MyPrivateEndpoint1 -ResourceGroupName TestResourceGroup

Name                                : MyPrivateEndpoint1
ResourceGroupName                   : TestResourceGroup
Location                            : eastus2euap
Id                                  : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/provi
                                      ders/Microsoft.Network/privateEndpoints/MyPrivateEndpoint1
Etag                                : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState                   : Succeeded
Subnet                              : {
                                        "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork1/subnets/backendSubnet",
                                      }
NetworkInterfaces                   : [
                                        {

                                          "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/networkInterfaces/MyNic1",
                                        }
                                      ]
PrivateLinkServiceConnections       : []
ManualPrivateLinkServiceConnections : [
                                        {
                                          "Name": "MyPrivateLinkServiceConnection",
                                          "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/privateEndpoints/MyPrivateEndpoint1/manualPrivateLinkServi
                                      ceConnections/MyPrivateLinkServiceConnection",
                                          "PrivateLinkServiceId": "/subscriptions/00000000-0000-0000-0000-000000000000/
                                      resourceGroups/TestResourceGroup/providers/Microsoft.Network/priv
                                      ateLinkServices/MyPrivateLinkService",
                                          "PrivateLinkServiceConnectionState": {
                                            "Status": "Pending",
                                            "Description": "Awaiting approval"
                                          }
                                        }
                                      ]
```

<span data-ttu-id="ef619-111">To polecenie pobiera prywatny punkt końcowy o nazwie MyPrivateEndpoint1 w grupie zasobów TestResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ef619-111">This command gets the private endpoint named MyPrivateEndpoint1 in the resource group TestResourceGroup</span></span>

### <span data-ttu-id="ef619-112">Przykład 2. Lista wszystkich prywatnych punktów końcowych w grupie ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ef619-112">Example 2: List all private endpoints in ResourceGroup</span></span>
```powershell
Get-AzPrivateEndpoint -ResourceGroupName TestResourceGroup

Name                                : MyPrivateEndpoint1
ResourceGroupName                   : TestResourceGroup
Location                            : eastus2euap
Id                                  : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/provi
                                      ders/Microsoft.Network/privateEndpoints/MyPrivateEndpoint1
Etag                                : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState                   : Succeeded
Subnet                              : {
                                        "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork1/subnets/backendSubnet",
                                      }
NetworkInterfaces                   : [
                                        {

                                          "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/networkInterfaces/MyNic1",
                                        }
                                      ]
PrivateLinkServiceConnections       : []
ManualPrivateLinkServiceConnections : [
                                        {
                                          "Name": "MyPrivateLinkServiceConnection",
                                          "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/privateEndpoints/MyPrivateEndpoint1/manualPrivateLinkServi
                                      ceConnections/MyPrivateLinkServiceConnection",
                                          "PrivateLinkServiceId": "/subscriptions/00000000-0000-0000-0000-000000000000/
                                      resourceGroups/TestResourceGroup/providers/Microsoft.Network/priv
                                      ateLinkServices/MyPrivateLinkService",
                                          "PrivateLinkServiceConnectionState": {
                                            "Status": "Pending",
                                            "Description": "Awaiting approval"
                                          }
                                        }
                                      ]
```

<span data-ttu-id="ef619-113">To polecenie pobiera wszystkie prywatne punkty końcowe w grupie zasobów TestResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ef619-113">This command gets all of private end points in the resource group TestResourceGroup</span></span>

## <span data-ttu-id="ef619-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ef619-114">PARAMETERS</span></span>

### <span data-ttu-id="ef619-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef619-115">-DefaultProfile</span></span>
<span data-ttu-id="ef619-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ef619-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef619-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="ef619-117">-ExpandResource</span></span>
<span data-ttu-id="ef619-118">Odwołanie do zasobu do rozwinięcia.</span><span class="sxs-lookup"><span data-stu-id="ef619-118">The resource reference to be expanded.</span></span>

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

### <span data-ttu-id="ef619-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ef619-119">-Name</span></span>
<span data-ttu-id="ef619-120">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="ef619-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef619-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef619-121">-ResourceGroupName</span></span>
<span data-ttu-id="ef619-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ef619-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### <span data-ttu-id="ef619-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef619-123">CommonParameters</span></span>
<span data-ttu-id="ef619-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef619-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef619-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ef619-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef619-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ef619-126">INPUTS</span></span>

### <span data-ttu-id="ef619-127">System.String</span><span class="sxs-lookup"><span data-stu-id="ef619-127">System.String</span></span>

## <span data-ttu-id="ef619-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ef619-128">OUTPUTS</span></span>

### <span data-ttu-id="ef619-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ef619-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="ef619-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ef619-130">NOTES</span></span>

## <span data-ttu-id="ef619-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ef619-131">RELATED LINKS</span></span>

[<span data-ttu-id="ef619-132">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="ef619-132">New-AzPrivateEndpoint</span></span>](./New-AzPrivateEndpoint.md)

[<span data-ttu-id="ef619-133">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="ef619-133">Remove-AzPrivateEndpoint</span></span>](./Remove-AzPrivateEndpoint.md)