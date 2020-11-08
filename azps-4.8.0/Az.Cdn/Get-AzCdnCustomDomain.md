---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 53246003-D1E9-4863-94E9-8E0BF1272134
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnCustomDomain.md
ms.openlocfilehash: c98ec2ebee71188ddbc5760dbbd3d1528da3c770
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94220181"
---
# <span data-ttu-id="4999f-101">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="4999f-101">Get-AzCdnCustomDomain</span></span>

## <span data-ttu-id="4999f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4999f-102">SYNOPSIS</span></span>
<span data-ttu-id="4999f-103">Pobiera niestandardową domenę sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="4999f-103">Gets a CDN custom domain.</span></span>

## <span data-ttu-id="4999f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4999f-104">SYNTAX</span></span>

### <span data-ttu-id="4999f-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4999f-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnCustomDomain [-CustomDomainName <String>] -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4999f-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4999f-106">ByObjectParameterSet</span></span>
```
Get-AzCdnCustomDomain [-CustomDomainName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4999f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="4999f-107">DESCRIPTION</span></span>
<span data-ttu-id="4999f-108">Polecenie cmdlet **Get-AzCdnCustomDomain** pobiera domenę niestandardową sieci dostarczania zawartości (CDN) platformy Azure oraz jej ustawienia pokrewne.</span><span class="sxs-lookup"><span data-stu-id="4999f-108">The **Get-AzCdnCustomDomain** cmdlet gets an Azure Content Delivery Network (CDN) custom domain and its related settings.</span></span>

## <span data-ttu-id="4999f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4999f-109">EXAMPLES</span></span>

## <span data-ttu-id="4999f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4999f-110">PARAMETERS</span></span>

### <span data-ttu-id="4999f-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="4999f-111">-CdnEndpoint</span></span>
<span data-ttu-id="4999f-112">Określa obiekt punktu końcowego sieci CDN, do którego należy Twoja domena niestandardowa.</span><span class="sxs-lookup"><span data-stu-id="4999f-112">Specifies the CDN endpoint object of which the custom domain is a member.</span></span>

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

### <span data-ttu-id="4999f-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="4999f-113">-CustomDomainName</span></span>
<span data-ttu-id="4999f-114">Określa nazwę domeny niestandardowej.</span><span class="sxs-lookup"><span data-stu-id="4999f-114">Specifies the name of the custom domain.</span></span>
<span data-ttu-id="4999f-115">Nazwa domeny niestandardowej różni się od nazwy hosta domeny niestandardowej.</span><span class="sxs-lookup"><span data-stu-id="4999f-115">The name of the custom domain differs from the host name of the custom domain.</span></span>

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

### <span data-ttu-id="4999f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4999f-116">-DefaultProfile</span></span>
<span data-ttu-id="4999f-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="4999f-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4999f-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="4999f-118">-EndpointName</span></span>
<span data-ttu-id="4999f-119">Określa nazwę punktu końcowego, do którego należy domena niestandardowa.</span><span class="sxs-lookup"><span data-stu-id="4999f-119">Specifies the name of the endpoint to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="4999f-120">-Refilename</span><span class="sxs-lookup"><span data-stu-id="4999f-120">-ProfileName</span></span>
<span data-ttu-id="4999f-121">Określa nazwę profilu, do którego należy domena niestandardowa.</span><span class="sxs-lookup"><span data-stu-id="4999f-121">Specifies the name of the Profile to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="4999f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4999f-122">-ResourceGroupName</span></span>
<span data-ttu-id="4999f-123">Określa nazwę grupy zasobów, do której należy domena niestandardowa.</span><span class="sxs-lookup"><span data-stu-id="4999f-123">Specifies the name of the resource group to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="4999f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4999f-124">CommonParameters</span></span>
<span data-ttu-id="4999f-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4999f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4999f-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4999f-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4999f-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4999f-127">INPUTS</span></span>

### <span data-ttu-id="4999f-128">Microsoft. Azure. Commands. CDN. models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="4999f-128">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="4999f-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4999f-129">OUTPUTS</span></span>

### <span data-ttu-id="4999f-130">Microsoft. Azure. Commands. CDN. models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="4999f-130">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="4999f-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4999f-131">NOTES</span></span>

## <span data-ttu-id="4999f-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4999f-132">RELATED LINKS</span></span>

[<span data-ttu-id="4999f-133">Nowe — AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="4999f-133">New-AzCdnCustomDomain</span></span>](./New-AzCdnCustomDomain.md)

[<span data-ttu-id="4999f-134">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="4999f-134">Remove-AzCdnCustomDomain</span></span>](./Remove-AzCdnCustomDomain.md)


