---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpAllocation.md
ms.openlocfilehash: c08a148d1c58e08daa2fce8cd1e195887a264f19
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956906"
---
# <span data-ttu-id="57526-101">Get-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="57526-101">Get-AzIpAllocation</span></span>

## <span data-ttu-id="57526-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57526-102">SYNOPSIS</span></span>
<span data-ttu-id="57526-103">Pobiera usługę Azure IpAllocation.</span><span class="sxs-lookup"><span data-stu-id="57526-103">Gets a Azure IpAllocation.</span></span>

## <span data-ttu-id="57526-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="57526-104">SYNTAX</span></span>

### <span data-ttu-id="57526-105">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="57526-105">GetByNameParameterSet</span></span>
```
Get-AzIpAllocation [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="57526-106">ListParameterSet</span><span class="sxs-lookup"><span data-stu-id="57526-106">ListParameterSet</span></span>
```
Get-AzIpAllocation [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="57526-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="57526-107">GetByResourceIdParameterSet</span></span>
```
Get-AzIpAllocation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57526-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="57526-108">DESCRIPTION</span></span>
<span data-ttu-id="57526-109">Polecenie **cmdlet Get-AzIpAllocation** otrzymuje adres IpAllocation platformy Azure</span><span class="sxs-lookup"><span data-stu-id="57526-109">The **Get-AzIpAllocation** cmdlet gets an Azure IpAllocation</span></span>

## <span data-ttu-id="57526-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="57526-110">EXAMPLES</span></span>

### <span data-ttu-id="57526-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="57526-111">Example 1</span></span>
```powershell
Get-AzIpAllocation -ResourceGroupName 'TestResourceGroup' -Name 'TestIpAllocation'
```

## <span data-ttu-id="57526-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="57526-112">PARAMETERS</span></span>

### <span data-ttu-id="57526-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57526-113">-DefaultProfile</span></span>
<span data-ttu-id="57526-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="57526-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57526-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="57526-115">-Name</span></span>
<span data-ttu-id="57526-116">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="57526-116">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57526-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57526-117">-ResourceGroupName</span></span>
<span data-ttu-id="57526-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="57526-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57526-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="57526-119">-ResourceId</span></span>
<span data-ttu-id="57526-120">Identyfikator ipAllocation</span><span class="sxs-lookup"><span data-stu-id="57526-120">IpAllocation Id</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57526-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57526-121">CommonParameters</span></span>
<span data-ttu-id="57526-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57526-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57526-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="57526-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57526-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="57526-124">INPUTS</span></span>

### <span data-ttu-id="57526-125">System.String</span><span class="sxs-lookup"><span data-stu-id="57526-125">System.String</span></span>

## <span data-ttu-id="57526-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="57526-126">OUTPUTS</span></span>

### <span data-ttu-id="57526-127">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span><span class="sxs-lookup"><span data-stu-id="57526-127">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="57526-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="57526-128">NOTES</span></span>

## <span data-ttu-id="57526-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="57526-129">RELATED LINKS</span></span>
