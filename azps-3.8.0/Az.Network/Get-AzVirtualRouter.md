---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouter.md
ms.openlocfilehash: dc568657feb5f86cf7cfaa21042e03f8470a9caa
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050330"
---
# <span data-ttu-id="05d37-101">Get-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="05d37-101">Get-AzVirtualRouter</span></span>

## <span data-ttu-id="05d37-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="05d37-102">SYNOPSIS</span></span>
<span data-ttu-id="05d37-103">Pobierz usługę Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="05d37-103">Get an Azure VirtualRouter</span></span>

## <span data-ttu-id="05d37-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="05d37-104">SYNTAX</span></span>

### <span data-ttu-id="05d37-105">VirtualRouterNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="05d37-105">VirtualRouterNameParameterSet (Default)</span></span>
```
Get-AzVirtualRouter -ResourceGroupName <String> [-RouterName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="05d37-106">VirtualRouterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="05d37-106">VirtualRouterResourceIdParameterSet</span></span>
```
Get-AzVirtualRouter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="05d37-107">Opis</span><span class="sxs-lookup"><span data-stu-id="05d37-107">DESCRIPTION</span></span>
<span data-ttu-id="05d37-108">Polecenie cmdlet **Get-AzVirtualRouter** pobiera platformę Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="05d37-108">The **Get-AzVirtualRouter** cmdlet gets an Azure VirtualRouter</span></span>

## <span data-ttu-id="05d37-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="05d37-109">EXAMPLES</span></span>

### <span data-ttu-id="05d37-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="05d37-110">Example 1</span></span>
```powershell
Get-AzVirtualRouter -ResourceGroupName virtualRouterRG -RouterName virtualRouter 
```

### <span data-ttu-id="05d37-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="05d37-111">Example 2</span></span>
```powershell
$virtualRouterId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter'
Get-AzVirtualRouter -ResourceId $virtualRouterId
```

## <span data-ttu-id="05d37-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="05d37-112">PARAMETERS</span></span>

### <span data-ttu-id="05d37-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05d37-113">-DefaultProfile</span></span>
<span data-ttu-id="05d37-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="05d37-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05d37-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05d37-115">-ResourceGroupName</span></span>
<span data-ttu-id="05d37-116">Nazwa grupy zasobów routera wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="05d37-116">The resource group name of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05d37-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="05d37-117">-ResourceId</span></span>
<span data-ttu-id="05d37-118">Identyfikator zasobu routera wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="05d37-118">ResourceId of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05d37-119">-Routername</span><span class="sxs-lookup"><span data-stu-id="05d37-119">-RouterName</span></span>
<span data-ttu-id="05d37-120">Nazwa routera wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="05d37-120">The name of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05d37-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05d37-121">CommonParameters</span></span>
<span data-ttu-id="05d37-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05d37-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05d37-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05d37-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05d37-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="05d37-124">INPUTS</span></span>

### <span data-ttu-id="05d37-125">System. String</span><span class="sxs-lookup"><span data-stu-id="05d37-125">System.String</span></span>

## <span data-ttu-id="05d37-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="05d37-126">OUTPUTS</span></span>

### <span data-ttu-id="05d37-127">Microsoft. Azure. Commands. Network. models. PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="05d37-127">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="05d37-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="05d37-128">NOTES</span></span>

## <span data-ttu-id="05d37-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="05d37-129">RELATED LINKS</span></span>
