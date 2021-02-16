---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpGroup.md
ms.openlocfilehash: 11c5e3ff2d8ee548917de7a94b1a592ae4cce52b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189763"
---
# <span data-ttu-id="a2c31-101">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="a2c31-101">Get-AzIpGroup</span></span>

## <span data-ttu-id="a2c31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2c31-102">SYNOPSIS</span></span>
<span data-ttu-id="a2c31-103">Uzyskiwanie usługi Azure IpGroup</span><span class="sxs-lookup"><span data-stu-id="a2c31-103">Get an Azure IpGroup</span></span>

## <span data-ttu-id="a2c31-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a2c31-104">SYNTAX</span></span>

### <span data-ttu-id="a2c31-105">IpGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2c31-105">IpGroupNameParameterSet</span></span>
```
Get-AzIpGroup -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a2c31-106">IpGroupResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2c31-106">IpGroupResourceIdParameterSet</span></span>
```
Get-AzIpGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2c31-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="a2c31-107">DESCRIPTION</span></span>
<span data-ttu-id="a2c31-108">Polecenie **cmdlet Get-AzIpGroup** pobiera grupę IpGroup platformy Azure</span><span class="sxs-lookup"><span data-stu-id="a2c31-108">The **Get-AzIpGroup** cmdlet gets an Azure IpGroup</span></span>

## <span data-ttu-id="a2c31-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a2c31-109">EXAMPLES</span></span>

### <span data-ttu-id="a2c31-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a2c31-110">Example 1</span></span>
```powershell
Get-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
```

### <span data-ttu-id="a2c31-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="a2c31-111">Example 2</span></span>
```powershell
$ipGroupId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/ipGroupRG/providers/Microsoft.Network/ipGroups/ipGroup'
Get-AzIpGroup -ResourceId $ipGroupId
```

## <span data-ttu-id="a2c31-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a2c31-112">PARAMETERS</span></span>

### <span data-ttu-id="a2c31-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2c31-113">-DefaultProfile</span></span>
<span data-ttu-id="a2c31-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a2c31-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2c31-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a2c31-115">-Name</span></span>
<span data-ttu-id="a2c31-116">Nazwa grupy adresów ip.</span><span class="sxs-lookup"><span data-stu-id="a2c31-116">The name of the ipgroup.</span></span>

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

### <span data-ttu-id="a2c31-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2c31-117">-ResourceGroupName</span></span>
<span data-ttu-id="a2c31-118">Nazwa grupy zasobów grupy ipgroup.</span><span class="sxs-lookup"><span data-stu-id="a2c31-118">The resource group name of the ipgroup.</span></span>

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

### <span data-ttu-id="a2c31-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a2c31-119">-ResourceId</span></span>
<span data-ttu-id="a2c31-120">ResourceId grupy ip.</span><span class="sxs-lookup"><span data-stu-id="a2c31-120">ResourceId of the ipgroup.</span></span>

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

### <span data-ttu-id="a2c31-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2c31-121">CommonParameters</span></span>
<span data-ttu-id="a2c31-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2c31-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2c31-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a2c31-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2c31-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a2c31-124">INPUTS</span></span>

### <span data-ttu-id="a2c31-125">System.String</span><span class="sxs-lookup"><span data-stu-id="a2c31-125">System.String</span></span>

## <span data-ttu-id="a2c31-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a2c31-126">OUTPUTS</span></span>

### <span data-ttu-id="a2c31-127">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="a2c31-127">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="a2c31-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a2c31-128">NOTES</span></span>

## <span data-ttu-id="a2c31-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a2c31-129">RELATED LINKS</span></span>
