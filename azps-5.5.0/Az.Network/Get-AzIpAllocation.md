---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpAllocation.md
ms.openlocfilehash: 89a0276a94ffa2729c5803a017e297ff05e84534
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189771"
---
# <span data-ttu-id="a8f90-101">Get-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="a8f90-101">Get-AzIpAllocation</span></span>

## <span data-ttu-id="a8f90-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8f90-102">SYNOPSIS</span></span>
<span data-ttu-id="a8f90-103">Otrzymuje usługę Azure IpAllocation.</span><span class="sxs-lookup"><span data-stu-id="a8f90-103">Gets a Azure IpAllocation.</span></span>

## <span data-ttu-id="a8f90-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a8f90-104">SYNTAX</span></span>

### <span data-ttu-id="a8f90-105">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8f90-105">GetByNameParameterSet</span></span>
```
Get-AzIpAllocation [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a8f90-106">ListParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8f90-106">ListParameterSet</span></span>
```
Get-AzIpAllocation [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a8f90-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8f90-107">GetByResourceIdParameterSet</span></span>
```
Get-AzIpAllocation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a8f90-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="a8f90-108">DESCRIPTION</span></span>
<span data-ttu-id="a8f90-109">Polecenie **cmdlet Get-AzIpAllocation** otrzymuje adres IpAllocation platformy Azure</span><span class="sxs-lookup"><span data-stu-id="a8f90-109">The **Get-AzIpAllocation** cmdlet gets an Azure IpAllocation</span></span>

## <span data-ttu-id="a8f90-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a8f90-110">EXAMPLES</span></span>

### <span data-ttu-id="a8f90-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a8f90-111">Example 1</span></span>
```powershell
Get-AzIpAllocation -ResourceGroupName 'TestResourceGroup' -Name 'TestIpAllocation'
```

## <span data-ttu-id="a8f90-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a8f90-112">PARAMETERS</span></span>

### <span data-ttu-id="a8f90-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8f90-113">-DefaultProfile</span></span>
<span data-ttu-id="a8f90-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a8f90-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8f90-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a8f90-115">-Name</span></span>
<span data-ttu-id="a8f90-116">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="a8f90-116">The resource name.</span></span>

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

### <span data-ttu-id="a8f90-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8f90-117">-ResourceGroupName</span></span>
<span data-ttu-id="a8f90-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a8f90-118">The resource group name.</span></span>

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

### <span data-ttu-id="a8f90-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a8f90-119">-ResourceId</span></span>
<span data-ttu-id="a8f90-120">Identyfikator ipAllocation</span><span class="sxs-lookup"><span data-stu-id="a8f90-120">IpAllocation Id</span></span>

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

### <span data-ttu-id="a8f90-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8f90-121">CommonParameters</span></span>
<span data-ttu-id="a8f90-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8f90-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8f90-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a8f90-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8f90-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a8f90-124">INPUTS</span></span>

### <span data-ttu-id="a8f90-125">System.String</span><span class="sxs-lookup"><span data-stu-id="a8f90-125">System.String</span></span>

## <span data-ttu-id="a8f90-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a8f90-126">OUTPUTS</span></span>

### <span data-ttu-id="a8f90-127">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span><span class="sxs-lookup"><span data-stu-id="a8f90-127">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="a8f90-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a8f90-128">NOTES</span></span>

## <span data-ttu-id="a8f90-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a8f90-129">RELATED LINKS</span></span>
