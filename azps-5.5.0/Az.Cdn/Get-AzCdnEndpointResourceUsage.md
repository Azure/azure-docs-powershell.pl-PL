---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnendpointresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointResourceUsage.md
ms.openlocfilehash: 7b8773f4e8e0f63404d81c56703181124f6f8ad0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239140"
---
# <span data-ttu-id="515c4-101">Get-AzCdnEndpointResourceUsage</span><span class="sxs-lookup"><span data-stu-id="515c4-101">Get-AzCdnEndpointResourceUsage</span></span>

## <span data-ttu-id="515c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="515c4-102">SYNOPSIS</span></span>
<span data-ttu-id="515c4-103">Pobiera użycie zasobu punktu końcowego sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="515c4-103">Gets the resource usage of a CDN endpoint.</span></span>

## <span data-ttu-id="515c4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="515c4-104">SYNTAX</span></span>

### <span data-ttu-id="515c4-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="515c4-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnEndpointResourceUsage [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="515c4-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="515c4-106">ByObjectParameterSet</span></span>
```
Get-AzCdnEndpointResourceUsage [-EndpointName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="515c4-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="515c4-107">DESCRIPTION</span></span>
<span data-ttu-id="515c4-108">{{Wypełnij opis}}</span><span class="sxs-lookup"><span data-stu-id="515c4-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="515c4-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="515c4-109">EXAMPLES</span></span>

### <span data-ttu-id="515c4-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="515c4-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="515c4-111">{{ Dodaj przykładowy opis tutaj }}</span><span class="sxs-lookup"><span data-stu-id="515c4-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="515c4-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="515c4-112">PARAMETERS</span></span>

### <span data-ttu-id="515c4-113">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="515c4-113">-CdnEndpoint</span></span>
<span data-ttu-id="515c4-114">Obiekt punktu końcowego sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="515c4-114">The CDN endpoint object.</span></span>

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

### <span data-ttu-id="515c4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="515c4-115">-DefaultProfile</span></span>
<span data-ttu-id="515c4-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="515c4-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="515c4-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="515c4-117">-EndpointName</span></span>
<span data-ttu-id="515c4-118">Nazwa punktu końcowego sieci Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="515c4-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="515c4-119">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="515c4-119">-ProfileName</span></span>
<span data-ttu-id="515c4-120">Nazwa profilu azure CDN.</span><span class="sxs-lookup"><span data-stu-id="515c4-120">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="515c4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="515c4-121">-ResourceGroupName</span></span>
<span data-ttu-id="515c4-122">Grupa zasobów profilu azure CDN.</span><span class="sxs-lookup"><span data-stu-id="515c4-122">The resource group of the Azure CDN Profile.</span></span>

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

### <span data-ttu-id="515c4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="515c4-123">CommonParameters</span></span>
<span data-ttu-id="515c4-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="515c4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="515c4-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="515c4-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="515c4-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="515c4-126">INPUTS</span></span>

### <span data-ttu-id="515c4-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="515c4-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="515c4-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="515c4-128">OUTPUTS</span></span>

### <span data-ttu-id="515c4-129">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="515c4-129">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="515c4-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="515c4-130">NOTES</span></span>

## <span data-ttu-id="515c4-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="515c4-131">RELATED LINKS</span></span>
