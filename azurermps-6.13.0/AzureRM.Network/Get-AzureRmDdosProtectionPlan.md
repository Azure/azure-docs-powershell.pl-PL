---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azuredosprotectionplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmDdosProtectionPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmDdosProtectionPlan.md
ms.openlocfilehash: 2d1942dd5c069660d062922a069cc88b505748fa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717913"
---
# <span data-ttu-id="81c4c-101">Get-AzureRmDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="81c4c-101">Get-AzureRmDdosProtectionPlan</span></span>

## <span data-ttu-id="81c4c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="81c4c-102">SYNOPSIS</span></span>
<span data-ttu-id="81c4c-103">Pobiera plan ochrony DDoS.</span><span class="sxs-lookup"><span data-stu-id="81c4c-103">Gets a DDoS protection plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81c4c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="81c4c-104">SYNTAX</span></span>

### <span data-ttu-id="81c4c-105">GetByNameAndGroup</span><span class="sxs-lookup"><span data-stu-id="81c4c-105">GetByNameAndGroup</span></span>
```
Get-AzureRmDdosProtectionPlan -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="81c4c-106">Lista</span><span class="sxs-lookup"><span data-stu-id="81c4c-106">List</span></span>
```
Get-AzureRmDdosProtectionPlan [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="81c4c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="81c4c-107">DESCRIPTION</span></span>
<span data-ttu-id="81c4c-108">Polecenie cmdlet Get-AzureRmDdosProtectionPlan pobiera plan ochrony DDoS.</span><span class="sxs-lookup"><span data-stu-id="81c4c-108">The Get-AzureRmDdosProtectionPlan cmdlet gets a DDoS protection plan.</span></span>

## <span data-ttu-id="81c4c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="81c4c-109">EXAMPLES</span></span>

### <span data-ttu-id="81c4c-110">Przykład 1: uzyskiwanie określonego planu ochrony DDoS</span><span class="sxs-lookup"><span data-stu-id="81c4c-110">Example 1: Get a specific DDoS protection plan</span></span>
```
D:\> Get-AzureRmDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlanName


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

<span data-ttu-id="81c4c-111">W tym przypadku należy określić zarówno atrybuty **ResourceGroupName** , jak i **nazwy** , które odpowiadają grupom zasobów i nazwie planu ochrony DDoS.</span><span class="sxs-lookup"><span data-stu-id="81c4c-111">In this case, we need to specify both **ResourceGroupName** and **Name** attributes, which correspond to the resource group and the name of the DDoS protection plan, respectively.</span></span>

### <span data-ttu-id="81c4c-112">Przykład 2: pobieranie wszystkich planów ochrony DDoS w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="81c4c-112">Example 2: Get all DDoS protection plans in a resource group</span></span>
```
D:\> Get-AzureRmDdosProtectionPlan -ResourceGroupName ResourceGroupName


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

<span data-ttu-id="81c4c-113">W tym scenariuszu należy określić tylko parametr **ResourceGroupName** , aby uzyskać listę planów ochrony DDoS.</span><span class="sxs-lookup"><span data-stu-id="81c4c-113">In this scenario, we only specify the parameter **ResourceGroupName** to get a list of DDoS protection plans.</span></span>

### <span data-ttu-id="81c4c-114">Przykład 2: pobieranie wszystkich planów ochrony DDoS w ramach subskrypcji</span><span class="sxs-lookup"><span data-stu-id="81c4c-114">Example 2: Get all DDoS protection plans in a subscription</span></span>
```
D:\> Get-AzureRmDdosProtectionPlan


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

<span data-ttu-id="81c4c-115">W tym przypadku nie określono żadnych parametrów, aby uzyskać listę wszystkich planów ochrony DDoS w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="81c4c-115">Here, we do not specify any parameters to get a list of all DDoS protection plans in a subscription.</span></span>

## <span data-ttu-id="81c4c-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="81c4c-116">PARAMETERS</span></span>

### <span data-ttu-id="81c4c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81c4c-117">-DefaultProfile</span></span>
<span data-ttu-id="81c4c-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="81c4c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81c4c-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="81c4c-119">-Name</span></span>
<span data-ttu-id="81c4c-120">Określa nazwę planu ochrony DDoS.</span><span class="sxs-lookup"><span data-stu-id="81c4c-120">Specifies the name of the DDoS protection plan.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndGroup
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81c4c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81c4c-121">-ResourceGroupName</span></span>
<span data-ttu-id="81c4c-122">Określa nazwę grupy zasobów planu ochrony DDoS.</span><span class="sxs-lookup"><span data-stu-id="81c4c-122">Specifies the name of the DDoS protection plan resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81c4c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81c4c-123">CommonParameters</span></span>
<span data-ttu-id="81c4c-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81c4c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81c4c-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81c4c-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81c4c-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="81c4c-126">INPUTS</span></span>

### <span data-ttu-id="81c4c-127">System. String</span><span class="sxs-lookup"><span data-stu-id="81c4c-127">System.String</span></span>

## <span data-ttu-id="81c4c-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="81c4c-128">OUTPUTS</span></span>

### <span data-ttu-id="81c4c-129">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="81c4c-129">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span></span>

## <span data-ttu-id="81c4c-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="81c4c-130">NOTES</span></span>

## <span data-ttu-id="81c4c-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="81c4c-131">RELATED LINKS</span></span>

[<span data-ttu-id="81c4c-132">Nowe — AzureRmDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="81c4c-132">New-AzureRmDdosProtectionPlan</span></span>](./New-AzureRmDdosProtectionPlan.md)

[<span data-ttu-id="81c4c-133">Remove-AzureRmDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="81c4c-133">Remove-AzureRmDdosProtectionPlan</span></span>](./Remove-AzureRmDdosProtectionPlan.md)

[<span data-ttu-id="81c4c-134">Nowe — AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="81c4c-134">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="81c4c-135">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="81c4c-135">Set-AzureRmVirtualNetwork</span></span>](./Set-AzureRmVirtualNetwork.md)

[<span data-ttu-id="81c4c-136">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="81c4c-136">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)
