---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpoint.md
ms.openlocfilehash: 11a0b65118fc9b580a885510f1e5ffa337b1d2e0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94225174"
---
# <span data-ttu-id="cf334-101">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="cf334-101">Get-AzPrivateEndpoint</span></span>

## <span data-ttu-id="cf334-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cf334-102">SYNOPSIS</span></span>
<span data-ttu-id="cf334-103">Uzyskiwanie prywatnego punktu końcowego</span><span class="sxs-lookup"><span data-stu-id="cf334-103">Get a private endpoint</span></span>

## <span data-ttu-id="cf334-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cf334-104">SYNTAX</span></span>

### <span data-ttu-id="cf334-105">NOEXPAND (domyślne)</span><span class="sxs-lookup"><span data-stu-id="cf334-105">NoExpand (Default)</span></span>
```
Get-AzPrivateEndpoint [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cf334-106">Większa</span><span class="sxs-lookup"><span data-stu-id="cf334-106">Expand</span></span>
```
Get-AzPrivateEndpoint -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf334-107">Opis</span><span class="sxs-lookup"><span data-stu-id="cf334-107">DESCRIPTION</span></span>
<span data-ttu-id="cf334-108">Polecenie cmdlet **Get-AzPrivateEndpoint** pobiera jeden lub więcej prywatnych punktów końcowych.</span><span class="sxs-lookup"><span data-stu-id="cf334-108">The **Get-AzPrivateEndpoint** cmdlet gets one or more private endpoints.</span></span>

## <span data-ttu-id="cf334-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cf334-109">EXAMPLES</span></span>

### <span data-ttu-id="cf334-110">Przykład 1: pobieranie prywatnego punktu końcowego</span><span class="sxs-lookup"><span data-stu-id="cf334-110">Example 1: Retrieve a private endpoint</span></span>
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

<span data-ttu-id="cf334-111">To polecenie uzyskuje prywatny punkt końcowy o nazwie MyPrivateEndpoint1 w grupie zasób TestResourceGroup</span><span class="sxs-lookup"><span data-stu-id="cf334-111">This command gets the private endpoint named MyPrivateEndpoint1 in the resource group TestResourceGroup</span></span>

### <span data-ttu-id="cf334-112">Przykład 2: wyświetlanie wszystkich prywatnych punktów końcowych w obszarze zasobów</span><span class="sxs-lookup"><span data-stu-id="cf334-112">Example 2: List all private endpoints in ResourceGroup</span></span>
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

<span data-ttu-id="cf334-113">To polecenie powoduje wyświetlenie wszystkich prywatnych punktów końcowych w grupie zasobów TestResourceGroup</span><span class="sxs-lookup"><span data-stu-id="cf334-113">This command gets all of private end points in the resource group TestResourceGroup</span></span>

## <span data-ttu-id="cf334-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cf334-114">PARAMETERS</span></span>

### <span data-ttu-id="cf334-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf334-115">-DefaultProfile</span></span>
<span data-ttu-id="cf334-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cf334-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf334-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="cf334-117">-ExpandResource</span></span>
<span data-ttu-id="cf334-118">Odwołanie do zasobu, które ma zostać rozwinięte.</span><span class="sxs-lookup"><span data-stu-id="cf334-118">The resource reference to be expanded.</span></span>

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

### <span data-ttu-id="cf334-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cf334-119">-Name</span></span>
<span data-ttu-id="cf334-120">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="cf334-120">The resource name.</span></span>

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

### <span data-ttu-id="cf334-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf334-121">-ResourceGroupName</span></span>
<span data-ttu-id="cf334-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cf334-122">The resource group name.</span></span>

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

### <span data-ttu-id="cf334-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf334-123">CommonParameters</span></span>
<span data-ttu-id="cf334-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf334-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf334-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cf334-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf334-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cf334-126">INPUTS</span></span>

### <span data-ttu-id="cf334-127">System. String</span><span class="sxs-lookup"><span data-stu-id="cf334-127">System.String</span></span>

## <span data-ttu-id="cf334-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cf334-128">OUTPUTS</span></span>

### <span data-ttu-id="cf334-129">Microsoft. Azure. Commands. Network. models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cf334-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="cf334-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cf334-130">NOTES</span></span>

## <span data-ttu-id="cf334-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cf334-131">RELATED LINKS</span></span>

[<span data-ttu-id="cf334-132">Nowe — AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="cf334-132">New-AzPrivateEndpoint</span></span>](./New-AzPrivateEndpoint.md)

[<span data-ttu-id="cf334-133">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="cf334-133">Remove-AzPrivateEndpoint</span></span>](./Remove-AzPrivateEndpoint.md)