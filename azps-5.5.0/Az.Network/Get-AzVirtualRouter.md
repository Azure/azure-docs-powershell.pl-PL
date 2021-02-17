---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouter.md
ms.openlocfilehash: e99df2f29781281ee0293f4cf52715153ff0d0cc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184611"
---
# <span data-ttu-id="485bf-101">Get-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="485bf-101">Get-AzVirtualRouter</span></span>

## <span data-ttu-id="485bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="485bf-102">SYNOPSIS</span></span>
<span data-ttu-id="485bf-103">Uzyskiwanie wirtualnego przekierowania na platformę Azure</span><span class="sxs-lookup"><span data-stu-id="485bf-103">Get an Azure VirtualRouter</span></span>

## <span data-ttu-id="485bf-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="485bf-104">SYNTAX</span></span>

### <span data-ttu-id="485bf-105">VirtualRouterSubscriptionIdParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="485bf-105">VirtualRouterSubscriptionIdParameterSet (Default)</span></span>
```
Get-AzVirtualRouter [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="485bf-106">VirtualRouterNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="485bf-106">VirtualRouterNameParameterSet</span></span>
```
Get-AzVirtualRouter -ResourceGroupName <String> [-RouterName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="485bf-107">VirtualRouterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="485bf-107">VirtualRouterResourceIdParameterSet</span></span>
```
Get-AzVirtualRouter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="485bf-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="485bf-108">DESCRIPTION</span></span>
<span data-ttu-id="485bf-109">Polecenie **cmdlet Get-AzVirtualRouter** otrzymuje narzędzie Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="485bf-109">The **Get-AzVirtualRouter** cmdlet gets an Azure VirtualRouter</span></span>

## <span data-ttu-id="485bf-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="485bf-110">EXAMPLES</span></span>

### <span data-ttu-id="485bf-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="485bf-111">Example 1</span></span>
```powershell
Get-AzVirtualRouter -ResourceGroupName virtualRouterRG -RouterName virtualRouter
```

### <span data-ttu-id="485bf-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="485bf-112">Example 2</span></span>
```powershell
$virtualRouterId = '/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter'
Get-AzVirtualRouter -ResourceId $virtualRouterId
```

## <span data-ttu-id="485bf-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="485bf-113">PARAMETERS</span></span>

### <span data-ttu-id="485bf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="485bf-114">-DefaultProfile</span></span>
<span data-ttu-id="485bf-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="485bf-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="485bf-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="485bf-116">-ResourceGroupName</span></span>
<span data-ttu-id="485bf-117">Nazwa grupy zasobów routera wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="485bf-117">The resource group name of the virtual router.</span></span>

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

### <span data-ttu-id="485bf-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="485bf-118">-ResourceId</span></span>
<span data-ttu-id="485bf-119">ResourceId routera wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="485bf-119">ResourceId of the virtual router.</span></span>

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

### <span data-ttu-id="485bf-120">-RouterName</span><span class="sxs-lookup"><span data-stu-id="485bf-120">-RouterName</span></span>
<span data-ttu-id="485bf-121">Nazwa routera wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="485bf-121">The name of the virtual router.</span></span>

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

### <span data-ttu-id="485bf-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="485bf-122">CommonParameters</span></span>
<span data-ttu-id="485bf-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="485bf-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="485bf-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="485bf-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="485bf-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="485bf-125">INPUTS</span></span>

### <span data-ttu-id="485bf-126">System.String</span><span class="sxs-lookup"><span data-stu-id="485bf-126">System.String</span></span>

## <span data-ttu-id="485bf-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="485bf-127">OUTPUTS</span></span>

### <span data-ttu-id="485bf-128">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="485bf-128">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="485bf-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="485bf-129">NOTES</span></span>

## <span data-ttu-id="485bf-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="485bf-130">RELATED LINKS</span></span>
