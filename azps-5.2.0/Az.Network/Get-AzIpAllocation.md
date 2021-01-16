---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpAllocation.md
ms.openlocfilehash: 89a0276a94ffa2729c5803a017e297ff05e84534
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98353761"
---
# <span data-ttu-id="0563f-101">Get-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="0563f-101">Get-AzIpAllocation</span></span>

## <span data-ttu-id="0563f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0563f-102">SYNOPSIS</span></span>
<span data-ttu-id="0563f-103">Pobiera usługę Azure IpAllocation.</span><span class="sxs-lookup"><span data-stu-id="0563f-103">Gets a Azure IpAllocation.</span></span>

## <span data-ttu-id="0563f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0563f-104">SYNTAX</span></span>

### <span data-ttu-id="0563f-105">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0563f-105">GetByNameParameterSet</span></span>
```
Get-AzIpAllocation [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0563f-106">ListParameterSet</span><span class="sxs-lookup"><span data-stu-id="0563f-106">ListParameterSet</span></span>
```
Get-AzIpAllocation [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0563f-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0563f-107">GetByResourceIdParameterSet</span></span>
```
Get-AzIpAllocation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0563f-108">Opis</span><span class="sxs-lookup"><span data-stu-id="0563f-108">DESCRIPTION</span></span>
<span data-ttu-id="0563f-109">Polecenie cmdlet **Get-AzIpAllocation** pobiera platformę Azure IpAllocation</span><span class="sxs-lookup"><span data-stu-id="0563f-109">The **Get-AzIpAllocation** cmdlet gets an Azure IpAllocation</span></span>

## <span data-ttu-id="0563f-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0563f-110">EXAMPLES</span></span>

### <span data-ttu-id="0563f-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0563f-111">Example 1</span></span>
```powershell
Get-AzIpAllocation -ResourceGroupName 'TestResourceGroup' -Name 'TestIpAllocation'
```

## <span data-ttu-id="0563f-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0563f-112">PARAMETERS</span></span>

### <span data-ttu-id="0563f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0563f-113">-DefaultProfile</span></span>
<span data-ttu-id="0563f-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0563f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0563f-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0563f-115">-Name</span></span>
<span data-ttu-id="0563f-116">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="0563f-116">The resource name.</span></span>

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

### <span data-ttu-id="0563f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0563f-117">-ResourceGroupName</span></span>
<span data-ttu-id="0563f-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0563f-118">The resource group name.</span></span>

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

### <span data-ttu-id="0563f-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0563f-119">-ResourceId</span></span>
<span data-ttu-id="0563f-120">Identyfikator IpAllocation</span><span class="sxs-lookup"><span data-stu-id="0563f-120">IpAllocation Id</span></span>

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

### <span data-ttu-id="0563f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0563f-121">CommonParameters</span></span>
<span data-ttu-id="0563f-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0563f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0563f-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0563f-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0563f-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0563f-124">INPUTS</span></span>

### <span data-ttu-id="0563f-125">System. String</span><span class="sxs-lookup"><span data-stu-id="0563f-125">System.String</span></span>

## <span data-ttu-id="0563f-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0563f-126">OUTPUTS</span></span>

### <span data-ttu-id="0563f-127">Microsoft. Azure. Commands. Network. models. PSIpAllocation</span><span class="sxs-lookup"><span data-stu-id="0563f-127">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="0563f-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0563f-128">NOTES</span></span>

## <span data-ttu-id="0563f-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0563f-129">RELATED LINKS</span></span>
