---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnendpointresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointResourceUsage.md
ms.openlocfilehash: 7b8773f4e8e0f63404d81c56703181124f6f8ad0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94220171"
---
# <span data-ttu-id="15064-101">Get-AzCdnEndpointResourceUsage</span><span class="sxs-lookup"><span data-stu-id="15064-101">Get-AzCdnEndpointResourceUsage</span></span>

## <span data-ttu-id="15064-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="15064-102">SYNOPSIS</span></span>
<span data-ttu-id="15064-103">Pobiera użycie zasobów punktu końcowego sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="15064-103">Gets the resource usage of a CDN endpoint.</span></span>

## <span data-ttu-id="15064-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="15064-104">SYNTAX</span></span>

### <span data-ttu-id="15064-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="15064-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnEndpointResourceUsage [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15064-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="15064-106">ByObjectParameterSet</span></span>
```
Get-AzCdnEndpointResourceUsage [-EndpointName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15064-107">Opis</span><span class="sxs-lookup"><span data-stu-id="15064-107">DESCRIPTION</span></span>
<span data-ttu-id="15064-108">{{Wpisz opis}}</span><span class="sxs-lookup"><span data-stu-id="15064-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="15064-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="15064-109">EXAMPLES</span></span>

### <span data-ttu-id="15064-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="15064-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="15064-111">{{Dodaj opis przykładu}}</span><span class="sxs-lookup"><span data-stu-id="15064-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="15064-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="15064-112">PARAMETERS</span></span>

### <span data-ttu-id="15064-113">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="15064-113">-CdnEndpoint</span></span>
<span data-ttu-id="15064-114">Obiekt punktu końcowego sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="15064-114">The CDN endpoint object.</span></span>

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

### <span data-ttu-id="15064-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15064-115">-DefaultProfile</span></span>
<span data-ttu-id="15064-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="15064-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="15064-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="15064-117">-EndpointName</span></span>
<span data-ttu-id="15064-118">Nazwa punktu końcowego usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="15064-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="15064-119">-Refilename</span><span class="sxs-lookup"><span data-stu-id="15064-119">-ProfileName</span></span>
<span data-ttu-id="15064-120">Nazwa profilu usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="15064-120">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="15064-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15064-121">-ResourceGroupName</span></span>
<span data-ttu-id="15064-122">Grupa zasobów profilu usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="15064-122">The resource group of the Azure CDN Profile.</span></span>

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

### <span data-ttu-id="15064-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15064-123">CommonParameters</span></span>
<span data-ttu-id="15064-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15064-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15064-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="15064-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15064-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="15064-126">INPUTS</span></span>

### <span data-ttu-id="15064-127">Microsoft. Azure. Commands. CDN. models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="15064-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="15064-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="15064-128">OUTPUTS</span></span>

### <span data-ttu-id="15064-129">Microsoft. Azure. Commands. CDN. modele. PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="15064-129">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="15064-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="15064-130">NOTES</span></span>

## <span data-ttu-id="15064-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="15064-131">RELATED LINKS</span></span>
