---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpGroup.md
ms.openlocfilehash: 11c5e3ff2d8ee548917de7a94b1a592ae4cce52b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052309"
---
# <span data-ttu-id="17b37-101">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="17b37-101">Get-AzIpGroup</span></span>

## <span data-ttu-id="17b37-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="17b37-102">SYNOPSIS</span></span>
<span data-ttu-id="17b37-103">Pobierz usługę Azure IpGroup</span><span class="sxs-lookup"><span data-stu-id="17b37-103">Get an Azure IpGroup</span></span>

## <span data-ttu-id="17b37-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="17b37-104">SYNTAX</span></span>

### <span data-ttu-id="17b37-105">IpGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="17b37-105">IpGroupNameParameterSet</span></span>
```
Get-AzIpGroup -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="17b37-106">IpGroupResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="17b37-106">IpGroupResourceIdParameterSet</span></span>
```
Get-AzIpGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17b37-107">Opis</span><span class="sxs-lookup"><span data-stu-id="17b37-107">DESCRIPTION</span></span>
<span data-ttu-id="17b37-108">Polecenie cmdlet **Get-AzIpGroup** pobiera platformę Azure IpGroup</span><span class="sxs-lookup"><span data-stu-id="17b37-108">The **Get-AzIpGroup** cmdlet gets an Azure IpGroup</span></span>

## <span data-ttu-id="17b37-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="17b37-109">EXAMPLES</span></span>

### <span data-ttu-id="17b37-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="17b37-110">Example 1</span></span>
```powershell
Get-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
```

### <span data-ttu-id="17b37-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="17b37-111">Example 2</span></span>
```powershell
$ipGroupId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/ipGroupRG/providers/Microsoft.Network/ipGroups/ipGroup'
Get-AzIpGroup -ResourceId $ipGroupId
```

## <span data-ttu-id="17b37-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="17b37-112">PARAMETERS</span></span>

### <span data-ttu-id="17b37-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17b37-113">-DefaultProfile</span></span>
<span data-ttu-id="17b37-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="17b37-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17b37-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="17b37-115">-Name</span></span>
<span data-ttu-id="17b37-116">Nazwa ipgroup.</span><span class="sxs-lookup"><span data-stu-id="17b37-116">The name of the ipgroup.</span></span>

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

### <span data-ttu-id="17b37-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17b37-117">-ResourceGroupName</span></span>
<span data-ttu-id="17b37-118">Nazwa grupy zasobów ipgroup.</span><span class="sxs-lookup"><span data-stu-id="17b37-118">The resource group name of the ipgroup.</span></span>

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

### <span data-ttu-id="17b37-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="17b37-119">-ResourceId</span></span>
<span data-ttu-id="17b37-120">Identyfikator zasobu ipgroup.</span><span class="sxs-lookup"><span data-stu-id="17b37-120">ResourceId of the ipgroup.</span></span>

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

### <span data-ttu-id="17b37-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17b37-121">CommonParameters</span></span>
<span data-ttu-id="17b37-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17b37-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17b37-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="17b37-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17b37-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="17b37-124">INPUTS</span></span>

### <span data-ttu-id="17b37-125">System. String</span><span class="sxs-lookup"><span data-stu-id="17b37-125">System.String</span></span>

## <span data-ttu-id="17b37-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="17b37-126">OUTPUTS</span></span>

### <span data-ttu-id="17b37-127">Microsoft. Azure. Commands. Network. models. PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="17b37-127">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="17b37-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="17b37-128">NOTES</span></span>

## <span data-ttu-id="17b37-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="17b37-129">RELATED LINKS</span></span>
