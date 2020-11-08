---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpAllocation.md
ms.openlocfilehash: 89a0276a94ffa2729c5803a017e297ff05e84534
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223107"
---
# <span data-ttu-id="4ab01-101">Get-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="4ab01-101">Get-AzIpAllocation</span></span>

## <span data-ttu-id="4ab01-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4ab01-102">SYNOPSIS</span></span>
<span data-ttu-id="4ab01-103">Pobiera usługę Azure IpAllocation.</span><span class="sxs-lookup"><span data-stu-id="4ab01-103">Gets a Azure IpAllocation.</span></span>

## <span data-ttu-id="4ab01-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4ab01-104">SYNTAX</span></span>

### <span data-ttu-id="4ab01-105">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4ab01-105">GetByNameParameterSet</span></span>
```
Get-AzIpAllocation [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4ab01-106">ListParameterSet</span><span class="sxs-lookup"><span data-stu-id="4ab01-106">ListParameterSet</span></span>
```
Get-AzIpAllocation [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4ab01-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4ab01-107">GetByResourceIdParameterSet</span></span>
```
Get-AzIpAllocation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ab01-108">Opis</span><span class="sxs-lookup"><span data-stu-id="4ab01-108">DESCRIPTION</span></span>
<span data-ttu-id="4ab01-109">Polecenie cmdlet **Get-AzIpAllocation** pobiera platformę Azure IpAllocation</span><span class="sxs-lookup"><span data-stu-id="4ab01-109">The **Get-AzIpAllocation** cmdlet gets an Azure IpAllocation</span></span>

## <span data-ttu-id="4ab01-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4ab01-110">EXAMPLES</span></span>

### <span data-ttu-id="4ab01-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4ab01-111">Example 1</span></span>
```powershell
Get-AzIpAllocation -ResourceGroupName 'TestResourceGroup' -Name 'TestIpAllocation'
```

## <span data-ttu-id="4ab01-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4ab01-112">PARAMETERS</span></span>

### <span data-ttu-id="4ab01-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ab01-113">-DefaultProfile</span></span>
<span data-ttu-id="4ab01-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4ab01-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ab01-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4ab01-115">-Name</span></span>
<span data-ttu-id="4ab01-116">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="4ab01-116">The resource name.</span></span>

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

### <span data-ttu-id="4ab01-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ab01-117">-ResourceGroupName</span></span>
<span data-ttu-id="4ab01-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4ab01-118">The resource group name.</span></span>

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

### <span data-ttu-id="4ab01-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4ab01-119">-ResourceId</span></span>
<span data-ttu-id="4ab01-120">Identyfikator IpAllocation</span><span class="sxs-lookup"><span data-stu-id="4ab01-120">IpAllocation Id</span></span>

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

### <span data-ttu-id="4ab01-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ab01-121">CommonParameters</span></span>
<span data-ttu-id="4ab01-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ab01-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ab01-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4ab01-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ab01-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4ab01-124">INPUTS</span></span>

### <span data-ttu-id="4ab01-125">System. String</span><span class="sxs-lookup"><span data-stu-id="4ab01-125">System.String</span></span>

## <span data-ttu-id="4ab01-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4ab01-126">OUTPUTS</span></span>

### <span data-ttu-id="4ab01-127">Microsoft. Azure. Commands. Network. models. PSIpAllocation</span><span class="sxs-lookup"><span data-stu-id="4ab01-127">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="4ab01-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4ab01-128">NOTES</span></span>

## <span data-ttu-id="4ab01-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4ab01-129">RELATED LINKS</span></span>
