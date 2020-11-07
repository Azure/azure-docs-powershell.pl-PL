---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azddosprotectionplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzDdosProtectionPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzDdosProtectionPlan.md
ms.openlocfilehash: 729f89742c7dd3249124f2d2404ab85f08db0e86
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709582"
---
# <span data-ttu-id="6cf9f-101">Get-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="6cf9f-101">Get-AzDdosProtectionPlan</span></span>

## <span data-ttu-id="6cf9f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6cf9f-102">SYNOPSIS</span></span>
<span data-ttu-id="6cf9f-103">Pobiera plan ochrony DDoS.</span><span class="sxs-lookup"><span data-stu-id="6cf9f-103">Gets a DDoS protection plan.</span></span>

## <span data-ttu-id="6cf9f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6cf9f-104">SYNTAX</span></span>

```
Get-AzDdosProtectionPlan [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6cf9f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6cf9f-105">DESCRIPTION</span></span>
<span data-ttu-id="6cf9f-106">Polecenie cmdlet Get-AzDdosProtectionPlan pobiera plan ochrony DDoS.</span><span class="sxs-lookup"><span data-stu-id="6cf9f-106">The Get-AzDdosProtectionPlan cmdlet gets a DDoS protection plan.</span></span>

## <span data-ttu-id="6cf9f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6cf9f-107">EXAMPLES</span></span>

### <span data-ttu-id="6cf9f-108">Przykład 1: uzyskiwanie określonego planu ochrony DDoS</span><span class="sxs-lookup"><span data-stu-id="6cf9f-108">Example 1: Get a specific DDoS protection plan</span></span>
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

<span data-ttu-id="6cf9f-109">W tym przypadku należy określić zarówno atrybuty **ResourceGroupName** , jak i **nazwy** , które odpowiadają grupom zasobów i nazwie planu ochrony DDoS.</span><span class="sxs-lookup"><span data-stu-id="6cf9f-109">In this case, we need to specify both **ResourceGroupName** and **Name** attributes, which correspond to the resource group and the name of the DDoS protection plan, respectively.</span></span>

### <span data-ttu-id="6cf9f-110">Przykład 2: pobieranie wszystkich planów ochrony DDoS w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="6cf9f-110">Example 2: Get all DDoS protection plans in a resource group</span></span>
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

<span data-ttu-id="6cf9f-111">W tym scenariuszu należy określić tylko parametr **ResourceGroupName** , aby uzyskać listę planów ochrony DDoS.</span><span class="sxs-lookup"><span data-stu-id="6cf9f-111">In this scenario, we only specify the parameter **ResourceGroupName** to get a list of DDoS protection plans.</span></span>

### <span data-ttu-id="6cf9f-112">Przykład 3: pobieranie wszystkich planów ochrony DDoS w ramach subskrypcji</span><span class="sxs-lookup"><span data-stu-id="6cf9f-112">Example 3: Get all DDoS protection plans in a subscription</span></span>
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

<span data-ttu-id="6cf9f-113">W tym przypadku nie określono żadnych parametrów, aby uzyskać listę wszystkich planów ochrony DDoS w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="6cf9f-113">Here, we do not specify any parameters to get a list of all DDoS protection plans in a subscription.</span></span>

### <span data-ttu-id="6cf9f-114">Przykład 4: pobieranie wszystkich planów ochrony DDoS w ramach subskrypcji</span><span class="sxs-lookup"><span data-stu-id="6cf9f-114">Example 4: Get all DDoS protection plans in a subscription</span></span>
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

<span data-ttu-id="6cf9f-115">To polecenie cmdlet zwraca wszystkie DdosProtectionPlans, które zaczynają się od tekstu "test".</span><span class="sxs-lookup"><span data-stu-id="6cf9f-115">This cmdlet returns all DdosProtectionPlans that start with "test".</span></span>

## <span data-ttu-id="6cf9f-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6cf9f-116">PARAMETERS</span></span>

### <span data-ttu-id="6cf9f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cf9f-117">-DefaultProfile</span></span>
<span data-ttu-id="6cf9f-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6cf9f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6cf9f-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6cf9f-119">-Name</span></span>
<span data-ttu-id="6cf9f-120">Określa nazwę planu ochrony DDoS.</span><span class="sxs-lookup"><span data-stu-id="6cf9f-120">Specifies the name of the DDoS protection plan.</span></span>

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

### <span data-ttu-id="6cf9f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cf9f-121">-ResourceGroupName</span></span>
<span data-ttu-id="6cf9f-122">Określa nazwę grupy zasobów planu ochrony DDoS.</span><span class="sxs-lookup"><span data-stu-id="6cf9f-122">Specifies the name of the DDoS protection plan resource group.</span></span>

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

### <span data-ttu-id="6cf9f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cf9f-123">CommonParameters</span></span>
<span data-ttu-id="6cf9f-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cf9f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cf9f-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6cf9f-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cf9f-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6cf9f-126">INPUTS</span></span>

### <span data-ttu-id="6cf9f-127">System. String</span><span class="sxs-lookup"><span data-stu-id="6cf9f-127">System.String</span></span>

## <span data-ttu-id="6cf9f-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6cf9f-128">OUTPUTS</span></span>

### <span data-ttu-id="6cf9f-129">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="6cf9f-129">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span></span>

## <span data-ttu-id="6cf9f-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6cf9f-130">NOTES</span></span>

## <span data-ttu-id="6cf9f-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6cf9f-131">RELATED LINKS</span></span>

[<span data-ttu-id="6cf9f-132">Nowe — AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="6cf9f-132">New-AzDdosProtectionPlan</span></span>](./New-AzDdosProtectionPlan.md)

[<span data-ttu-id="6cf9f-133">Remove-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="6cf9f-133">Remove-AzDdosProtectionPlan</span></span>](./Remove-AzDdosProtectionPlan.md)

[<span data-ttu-id="6cf9f-134">Nowe — AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6cf9f-134">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="6cf9f-135">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6cf9f-135">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)

[<span data-ttu-id="6cf9f-136">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6cf9f-136">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)