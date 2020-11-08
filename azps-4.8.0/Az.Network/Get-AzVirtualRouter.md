---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouter.md
ms.openlocfilehash: 26e919935a65a486252cac234450adf214992b36
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223096"
---
# <span data-ttu-id="008b6-101">Get-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="008b6-101">Get-AzVirtualRouter</span></span>

## <span data-ttu-id="008b6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="008b6-102">SYNOPSIS</span></span>
<span data-ttu-id="008b6-103">Pobierz usługę Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="008b6-103">Get an Azure VirtualRouter</span></span>

## <span data-ttu-id="008b6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="008b6-104">SYNTAX</span></span>

### <span data-ttu-id="008b6-105">VirtualRouterSubscriptionIdParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="008b6-105">VirtualRouterSubscriptionIdParameterSet (Default)</span></span>
```
Get-AzVirtualRouter [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="008b6-106">VirtualRouterNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="008b6-106">VirtualRouterNameParameterSet</span></span>
```
Get-AzVirtualRouter -ResourceGroupName <String> [-RouterName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="008b6-107">VirtualRouterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="008b6-107">VirtualRouterResourceIdParameterSet</span></span>
```
Get-AzVirtualRouter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="008b6-108">Opis</span><span class="sxs-lookup"><span data-stu-id="008b6-108">DESCRIPTION</span></span>
<span data-ttu-id="008b6-109">Polecenie cmdlet **Get-AzVirtualRouter** pobiera platformę Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="008b6-109">The **Get-AzVirtualRouter** cmdlet gets an Azure VirtualRouter</span></span>

## <span data-ttu-id="008b6-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="008b6-110">EXAMPLES</span></span>

### <span data-ttu-id="008b6-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="008b6-111">Example 1</span></span>
```powershell
Get-AzVirtualRouter -ResourceGroupName virtualRouterRG -RouterName virtualRouter
```

### <span data-ttu-id="008b6-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="008b6-112">Example 2</span></span>
```powershell
$virtualRouterId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter'
Get-AzVirtualRouter -ResourceId $virtualRouterId
```

## <span data-ttu-id="008b6-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="008b6-113">PARAMETERS</span></span>

### <span data-ttu-id="008b6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="008b6-114">-DefaultProfile</span></span>
<span data-ttu-id="008b6-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="008b6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="008b6-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="008b6-116">-ResourceGroupName</span></span>
<span data-ttu-id="008b6-117">Nazwa grupy zasobów routera wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="008b6-117">The resource group name of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="008b6-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="008b6-118">-ResourceId</span></span>
<span data-ttu-id="008b6-119">Identyfikator zasobu routera wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="008b6-119">ResourceId of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="008b6-120">-Routername</span><span class="sxs-lookup"><span data-stu-id="008b6-120">-RouterName</span></span>
<span data-ttu-id="008b6-121">Nazwa routera wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="008b6-121">The name of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="008b6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="008b6-122">CommonParameters</span></span>
<span data-ttu-id="008b6-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="008b6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="008b6-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="008b6-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="008b6-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="008b6-125">INPUTS</span></span>

### <span data-ttu-id="008b6-126">System. String</span><span class="sxs-lookup"><span data-stu-id="008b6-126">System.String</span></span>

## <span data-ttu-id="008b6-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="008b6-127">OUTPUTS</span></span>

### <span data-ttu-id="008b6-128">Microsoft. Azure. Commands. Network. models. PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="008b6-128">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="008b6-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="008b6-129">NOTES</span></span>

## <span data-ttu-id="008b6-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="008b6-130">RELATED LINKS</span></span>
