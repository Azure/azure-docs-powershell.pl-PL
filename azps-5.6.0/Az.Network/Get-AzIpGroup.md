---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpGroup.md
ms.openlocfilehash: 75a7afbb8997492e1b30ead7f745d2f5b6eb8b5d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956897"
---
# <span data-ttu-id="23d8e-101">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="23d8e-101">Get-AzIpGroup</span></span>

## <span data-ttu-id="23d8e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23d8e-102">SYNOPSIS</span></span>
<span data-ttu-id="23d8e-103">Uzyskiwanie usługi Azure IpGroup</span><span class="sxs-lookup"><span data-stu-id="23d8e-103">Get an Azure IpGroup</span></span>

## <span data-ttu-id="23d8e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="23d8e-104">SYNTAX</span></span>

### <span data-ttu-id="23d8e-105">IpGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="23d8e-105">IpGroupNameParameterSet</span></span>
```
Get-AzIpGroup -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="23d8e-106">IpGroupResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="23d8e-106">IpGroupResourceIdParameterSet</span></span>
```
Get-AzIpGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23d8e-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="23d8e-107">DESCRIPTION</span></span>
<span data-ttu-id="23d8e-108">Polecenie **cmdlet Get-AzIpGroup** pobiera grupę IpGroup platformy Azure</span><span class="sxs-lookup"><span data-stu-id="23d8e-108">The **Get-AzIpGroup** cmdlet gets an Azure IpGroup</span></span>

## <span data-ttu-id="23d8e-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="23d8e-109">EXAMPLES</span></span>

### <span data-ttu-id="23d8e-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="23d8e-110">Example 1</span></span>
```powershell
Get-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
```

### <span data-ttu-id="23d8e-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="23d8e-111">Example 2</span></span>
```powershell
$ipGroupId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/ipGroupRG/providers/Microsoft.Network/ipGroups/ipGroup'
Get-AzIpGroup -ResourceId $ipGroupId
```

## <span data-ttu-id="23d8e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="23d8e-112">PARAMETERS</span></span>

### <span data-ttu-id="23d8e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23d8e-113">-DefaultProfile</span></span>
<span data-ttu-id="23d8e-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="23d8e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23d8e-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="23d8e-115">-Name</span></span>
<span data-ttu-id="23d8e-116">Nazwa grupy adresów ip.</span><span class="sxs-lookup"><span data-stu-id="23d8e-116">The name of the ipgroup.</span></span>

```yaml
Type: String
Parameter Sets: IpGroupNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23d8e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23d8e-117">-ResourceGroupName</span></span>
<span data-ttu-id="23d8e-118">Nazwa grupy zasobów grupy ipgroup.</span><span class="sxs-lookup"><span data-stu-id="23d8e-118">The resource group name of the ipgroup.</span></span>

```yaml
Type: String
Parameter Sets: IpGroupNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23d8e-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="23d8e-119">-ResourceId</span></span>
<span data-ttu-id="23d8e-120">ResourceId grupy ip.</span><span class="sxs-lookup"><span data-stu-id="23d8e-120">ResourceId of the ipgroup.</span></span>

```yaml
Type: String
Parameter Sets: IpGroupResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23d8e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23d8e-121">CommonParameters</span></span>
<span data-ttu-id="23d8e-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23d8e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23d8e-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="23d8e-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23d8e-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="23d8e-124">INPUTS</span></span>

### <span data-ttu-id="23d8e-125">System.String</span><span class="sxs-lookup"><span data-stu-id="23d8e-125">System.String</span></span>

## <span data-ttu-id="23d8e-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="23d8e-126">OUTPUTS</span></span>

### <span data-ttu-id="23d8e-127">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="23d8e-127">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="23d8e-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="23d8e-128">NOTES</span></span>

## <span data-ttu-id="23d8e-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="23d8e-129">RELATED LINKS</span></span>
