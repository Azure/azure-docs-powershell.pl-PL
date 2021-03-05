---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/get-azcdnendpointresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointResourceUsage.md
ms.openlocfilehash: d39bd2d3a10f1ff8512b54cdf45902fb10f6810d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015409"
---
# <span data-ttu-id="a5509-101">Get-AzCdnEndpointResourceUsage</span><span class="sxs-lookup"><span data-stu-id="a5509-101">Get-AzCdnEndpointResourceUsage</span></span>

## <span data-ttu-id="a5509-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5509-102">SYNOPSIS</span></span>
<span data-ttu-id="a5509-103">Pobiera użycie zasobu punktu końcowego sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="a5509-103">Gets the resource usage of a CDN endpoint.</span></span>

## <span data-ttu-id="a5509-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a5509-104">SYNTAX</span></span>

### <span data-ttu-id="a5509-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="a5509-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnEndpointResourceUsage [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5509-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5509-106">ByObjectParameterSet</span></span>
```
Get-AzCdnEndpointResourceUsage [-EndpointName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5509-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="a5509-107">DESCRIPTION</span></span>
<span data-ttu-id="a5509-108">{{Wypełnij opis}}</span><span class="sxs-lookup"><span data-stu-id="a5509-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="a5509-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a5509-109">EXAMPLES</span></span>

### <span data-ttu-id="a5509-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a5509-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="a5509-111">{{ Dodaj przykładowy opis tutaj }}</span><span class="sxs-lookup"><span data-stu-id="a5509-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="a5509-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a5509-112">PARAMETERS</span></span>

### <span data-ttu-id="a5509-113">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="a5509-113">-CdnEndpoint</span></span>
<span data-ttu-id="a5509-114">Obiekt punktu końcowego sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="a5509-114">The CDN endpoint object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a5509-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5509-115">-DefaultProfile</span></span>
<span data-ttu-id="a5509-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="a5509-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a5509-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="a5509-117">-EndpointName</span></span>
<span data-ttu-id="a5509-118">Nazwa punktu końcowego sieci Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="a5509-118">Azure CDN endpoint name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5509-119">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="a5509-119">-ProfileName</span></span>
<span data-ttu-id="a5509-120">Nazwa profilu azure CDN.</span><span class="sxs-lookup"><span data-stu-id="a5509-120">Azure CDN profile name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5509-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5509-121">-ResourceGroupName</span></span>
<span data-ttu-id="a5509-122">Grupa zasobów profilu azure CDN.</span><span class="sxs-lookup"><span data-stu-id="a5509-122">The resource group of the Azure CDN Profile.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5509-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5509-123">CommonParameters</span></span>
<span data-ttu-id="a5509-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5509-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5509-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a5509-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5509-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a5509-126">INPUTS</span></span>

### <span data-ttu-id="a5509-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="a5509-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="a5509-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a5509-128">OUTPUTS</span></span>

### <span data-ttu-id="a5509-129">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="a5509-129">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="a5509-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a5509-130">NOTES</span></span>

## <span data-ttu-id="a5509-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a5509-131">RELATED LINKS</span></span>
