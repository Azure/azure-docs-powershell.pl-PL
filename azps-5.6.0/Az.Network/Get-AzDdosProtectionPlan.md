---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azddosprotectionplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzDdosProtectionPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzDdosProtectionPlan.md
ms.openlocfilehash: 2b5cc008e96d12828d5f834fd5fa4a30f83ea70f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967953"
---
# <span data-ttu-id="d1457-101">Get-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="d1457-101">Get-AzDdosProtectionPlan</span></span>

## <span data-ttu-id="d1457-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1457-102">SYNOPSIS</span></span>
<span data-ttu-id="d1457-103">Otrzymuje plan ochrony przed DDoS.</span><span class="sxs-lookup"><span data-stu-id="d1457-103">Gets a DDoS protection plan.</span></span>

## <span data-ttu-id="d1457-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d1457-104">SYNTAX</span></span>

```
Get-AzDdosProtectionPlan [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d1457-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d1457-105">DESCRIPTION</span></span>
<span data-ttu-id="d1457-106">Polecenie cmdlet Get-AzDdosProtectionPlan otrzymuje plan ochrony przed DDoS.</span><span class="sxs-lookup"><span data-stu-id="d1457-106">The Get-AzDdosProtectionPlan cmdlet gets a DDoS protection plan.</span></span>

## <span data-ttu-id="d1457-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d1457-107">EXAMPLES</span></span>

### <span data-ttu-id="d1457-108">Przykład 1. Uzyskiwanie określonego planu ochrony przed DDoS</span><span class="sxs-lookup"><span data-stu-id="d1457-108">Example 1: Get a specific DDoS protection plan</span></span>
```
D:\> Get-AzDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlanName


Name              : DdosProtectionPlanName
Id                : /subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/ddosProtectionPlans/DdosProtectionPlanName
Etag              : W/"a20e5592-9b51-423b-9758-b00cd322f744"
ProvisioningState : Succeeded
VirtualNetworks   : [
                      {
                        "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName"
                      }
                    ]
```

<span data-ttu-id="d1457-109">W tym przypadku należy określić zarówno atrybuty **ResourceGroupName,** jak i **Name,** odpowiadające odpowiednio grupie zasobów i nazwie planu ochrony przed DDoS.</span><span class="sxs-lookup"><span data-stu-id="d1457-109">In this case, we need to specify both **ResourceGroupName** and **Name** attributes, which correspond to the resource group and the name of the DDoS protection plan, respectively.</span></span>

### <span data-ttu-id="d1457-110">Przykład 2. Uzyskiwanie wszystkich planów ochrony przed DDoS w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="d1457-110">Example 2: Get all DDoS protection plans in a resource group</span></span>
```
D:\> Get-AzDdosProtectionPlan -ResourceGroupName ResourceGroupName


Name              : DdosProtectionPlanName
Id                : /subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/ddosProtectionPlans/DdosProtectionPlanName
Etag              : W/"a20e5592-9b51-423b-9758-b00cd322f744"
ProvisioningState : Succeeded
VirtualNetworks   : [
                      {
                        "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName"
                      }
                    ]
```

<span data-ttu-id="d1457-111">W tym scenariuszu określamy tylko parametr **ResourceGroupName,** aby uzyskać listę planów ochrony przed DDoS.</span><span class="sxs-lookup"><span data-stu-id="d1457-111">In this scenario, we only specify the parameter **ResourceGroupName** to get a list of DDoS protection plans.</span></span>

### <span data-ttu-id="d1457-112">Przykład 3. Uzyskiwanie wszystkich planów ochrony przed DDoS w ramach subskrypcji</span><span class="sxs-lookup"><span data-stu-id="d1457-112">Example 3: Get all DDoS protection plans in a subscription</span></span>
```
D:\> Get-AzDdosProtectionPlan


Name              : DdosProtectionPlanName
Id                : /subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/ddosProtectionPlans/DdosProtectionPlanName
Etag              : W/"a20e5592-9b51-423b-9758-b00cd322f744"
ProvisioningState : Succeeded
VirtualNetworks   : [
                      {
                        "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName"
                      }
                    ]
```

<span data-ttu-id="d1457-113">W tym miejscu nie określamy żadnych parametrów w celu uzyskania listy wszystkich planów ochrony przed DDoS w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d1457-113">Here, we do not specify any parameters to get a list of all DDoS protection plans in a subscription.</span></span>

### <span data-ttu-id="d1457-114">Przykład 4. Uzyskiwanie wszystkich planów ochrony przed DDoS w ramach subskrypcji</span><span class="sxs-lookup"><span data-stu-id="d1457-114">Example 4: Get all DDoS protection plans in a subscription</span></span>
```
D:\> Get-AzDdosProtectionPlan -Name test*


Name              : test1
Id                : /subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/ddosProtectionPlans/test1
Etag              : W/"a20e5592-9b51-423b-9758-b00cd322f744"
ProvisioningState : Succeeded
VirtualNetworks   : [
                      {
                        "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName"
                      }
                    ]

Name              : test2
Id                : /subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/ddosProtectionPlans/test2
Etag              : W/"a20e5592-9b51-423b-9758-b00cd322f744"
ProvisioningState : Succeeded
VirtualNetworks   : [
                      {
                        "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName"
                      }
                    ]
```

<span data-ttu-id="d1457-115">To polecenie cmdlet zwraca wszystkie Plany DdosProtection, które zaczynają się od "testu".</span><span class="sxs-lookup"><span data-stu-id="d1457-115">This cmdlet returns all DdosProtectionPlans that start with "test".</span></span>

## <span data-ttu-id="d1457-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d1457-116">PARAMETERS</span></span>

### <span data-ttu-id="d1457-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1457-117">-DefaultProfile</span></span>
<span data-ttu-id="d1457-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d1457-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1457-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d1457-119">-Name</span></span>
<span data-ttu-id="d1457-120">Określa nazwę planu ochrony przed DDoS.</span><span class="sxs-lookup"><span data-stu-id="d1457-120">Specifies the name of the DDoS protection plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="d1457-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1457-121">-ResourceGroupName</span></span>
<span data-ttu-id="d1457-122">Określa nazwę grupy zasobów planu ochrony DDoS.</span><span class="sxs-lookup"><span data-stu-id="d1457-122">Specifies the name of the DDoS protection plan resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="d1457-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1457-123">CommonParameters</span></span>
<span data-ttu-id="d1457-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1457-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1457-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d1457-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1457-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d1457-126">INPUTS</span></span>

### <span data-ttu-id="d1457-127">System.String</span><span class="sxs-lookup"><span data-stu-id="d1457-127">System.String</span></span>

## <span data-ttu-id="d1457-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d1457-128">OUTPUTS</span></span>

### <span data-ttu-id="d1457-129">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="d1457-129">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span></span>

## <span data-ttu-id="d1457-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d1457-130">NOTES</span></span>

## <span data-ttu-id="d1457-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d1457-131">RELATED LINKS</span></span>

[<span data-ttu-id="d1457-132">New-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="d1457-132">New-AzDdosProtectionPlan</span></span>](./New-AzDdosProtectionPlan.md)

[<span data-ttu-id="d1457-133">Remove-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="d1457-133">Remove-AzDdosProtectionPlan</span></span>](./Remove-AzDdosProtectionPlan.md)

[<span data-ttu-id="d1457-134">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d1457-134">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="d1457-135">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d1457-135">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)

[<span data-ttu-id="d1457-136">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d1457-136">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)