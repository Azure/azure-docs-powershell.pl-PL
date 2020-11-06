---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnendpointresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpointResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpointResourceUsage.md
ms.openlocfilehash: 3fe740fc8643ab6ef4f010feeee57b3339426c21
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546680"
---
# <span data-ttu-id="f7c9a-101">Get-AzureRmCdnEndpointResourceUsage</span><span class="sxs-lookup"><span data-stu-id="f7c9a-101">Get-AzureRmCdnEndpointResourceUsage</span></span>

## <span data-ttu-id="f7c9a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f7c9a-102">SYNOPSIS</span></span>
<span data-ttu-id="f7c9a-103">Pobiera użycie zasobów punktu końcowego sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="f7c9a-103">Gets the resource usage of a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f7c9a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f7c9a-104">SYNTAX</span></span>

### <span data-ttu-id="f7c9a-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f7c9a-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzureRmCdnEndpointResourceUsage [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7c9a-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7c9a-106">ByObjectParameterSet</span></span>
```
Get-AzureRmCdnEndpointResourceUsage [-EndpointName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7c9a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f7c9a-107">DESCRIPTION</span></span>
<span data-ttu-id="f7c9a-108">{{Wpisz opis}}</span><span class="sxs-lookup"><span data-stu-id="f7c9a-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="f7c9a-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f7c9a-109">EXAMPLES</span></span>

### <span data-ttu-id="f7c9a-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f7c9a-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="f7c9a-111">{{Dodaj opis przykładu}}</span><span class="sxs-lookup"><span data-stu-id="f7c9a-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="f7c9a-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f7c9a-112">PARAMETERS</span></span>

### <span data-ttu-id="f7c9a-113">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="f7c9a-113">-CdnEndpoint</span></span>
<span data-ttu-id="f7c9a-114">Obiekt punktu końcowego sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="f7c9a-114">The CDN endpoint object.</span></span>

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

### <span data-ttu-id="f7c9a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7c9a-115">-DefaultProfile</span></span>
<span data-ttu-id="f7c9a-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="f7c9a-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7c9a-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="f7c9a-117">-EndpointName</span></span>
<span data-ttu-id="f7c9a-118">Nazwa punktu końcowego usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="f7c9a-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="f7c9a-119">-Refilename</span><span class="sxs-lookup"><span data-stu-id="f7c9a-119">-ProfileName</span></span>
<span data-ttu-id="f7c9a-120">Nazwa profilu usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="f7c9a-120">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="f7c9a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7c9a-121">-ResourceGroupName</span></span>
<span data-ttu-id="f7c9a-122">Grupa zasobów profilu usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="f7c9a-122">The resource group of the Azure CDN Profile.</span></span>

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

### <span data-ttu-id="f7c9a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7c9a-123">CommonParameters</span></span>
<span data-ttu-id="f7c9a-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7c9a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7c9a-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7c9a-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7c9a-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f7c9a-126">INPUTS</span></span>

### <span data-ttu-id="f7c9a-127">Microsoft. Azure. Commands. CDN. models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="f7c9a-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>
<span data-ttu-id="f7c9a-128">Parametry: CdnEndpoint (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f7c9a-128">Parameters: CdnEndpoint (ByValue)</span></span>

## <span data-ttu-id="f7c9a-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f7c9a-129">OUTPUTS</span></span>

### <span data-ttu-id="f7c9a-130">Microsoft. Azure. Commands. CDN. modele. PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="f7c9a-130">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="f7c9a-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f7c9a-131">NOTES</span></span>

## <span data-ttu-id="f7c9a-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f7c9a-132">RELATED LINKS</span></span>
