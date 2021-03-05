---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 53246003-D1E9-4863-94E9-8E0BF1272134
online version: https://docs.microsoft.com/powershell/module/az.cdn/get-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnCustomDomain.md
ms.openlocfilehash: e1c436a76a3fc98714798bc938f0de987906e7d3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010817"
---
# <span data-ttu-id="918b0-101">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="918b0-101">Get-AzCdnCustomDomain</span></span>

## <span data-ttu-id="918b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="918b0-102">SYNOPSIS</span></span>
<span data-ttu-id="918b0-103">Pobiera domenę niestandardową CDN.</span><span class="sxs-lookup"><span data-stu-id="918b0-103">Gets a CDN custom domain.</span></span>

## <span data-ttu-id="918b0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="918b0-104">SYNTAX</span></span>

### <span data-ttu-id="918b0-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="918b0-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnCustomDomain [-CustomDomainName <String>] -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="918b0-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="918b0-106">ByObjectParameterSet</span></span>
```
Get-AzCdnCustomDomain [-CustomDomainName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="918b0-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="918b0-107">DESCRIPTION</span></span>
<span data-ttu-id="918b0-108">Polecenie **cmdlet Get-AzCdnCustomDomain** otrzymuje domenę niestandardową Azure Content Delivery Network (CDN) i powiązane z nią ustawienia.</span><span class="sxs-lookup"><span data-stu-id="918b0-108">The **Get-AzCdnCustomDomain** cmdlet gets an Azure Content Delivery Network (CDN) custom domain and its related settings.</span></span>

## <span data-ttu-id="918b0-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="918b0-109">EXAMPLES</span></span>

## <span data-ttu-id="918b0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="918b0-110">PARAMETERS</span></span>

### <span data-ttu-id="918b0-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="918b0-111">-CdnEndpoint</span></span>
<span data-ttu-id="918b0-112">Określa obiekt punktu końcowego sieci CDN, którego członkiem jest domena niestandardowa.</span><span class="sxs-lookup"><span data-stu-id="918b0-112">Specifies the CDN endpoint object of which the custom domain is a member.</span></span>

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

### <span data-ttu-id="918b0-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="918b0-113">-CustomDomainName</span></span>
<span data-ttu-id="918b0-114">Określa nazwę domeny niestandardowej.</span><span class="sxs-lookup"><span data-stu-id="918b0-114">Specifies the name of the custom domain.</span></span>
<span data-ttu-id="918b0-115">Nazwa domeny niestandardowej różni się od nazwy hosta domeny niestandardowej.</span><span class="sxs-lookup"><span data-stu-id="918b0-115">The name of the custom domain differs from the host name of the custom domain.</span></span>

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

### <span data-ttu-id="918b0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="918b0-116">-DefaultProfile</span></span>
<span data-ttu-id="918b0-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="918b0-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="918b0-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="918b0-118">-EndpointName</span></span>
<span data-ttu-id="918b0-119">Określa nazwę punktu końcowego, do którego należy domena niestandardowa.</span><span class="sxs-lookup"><span data-stu-id="918b0-119">Specifies the name of the endpoint to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="918b0-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="918b0-120">-ProfileName</span></span>
<span data-ttu-id="918b0-121">Określa nazwę profilu, do którego należy domena niestandardowa.</span><span class="sxs-lookup"><span data-stu-id="918b0-121">Specifies the name of the Profile to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="918b0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="918b0-122">-ResourceGroupName</span></span>
<span data-ttu-id="918b0-123">Określa nazwę grupy zasobów, do której należy domena niestandardowa.</span><span class="sxs-lookup"><span data-stu-id="918b0-123">Specifies the name of the resource group to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="918b0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="918b0-124">CommonParameters</span></span>
<span data-ttu-id="918b0-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="918b0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="918b0-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="918b0-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="918b0-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="918b0-127">INPUTS</span></span>

### <span data-ttu-id="918b0-128">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="918b0-128">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="918b0-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="918b0-129">OUTPUTS</span></span>

### <span data-ttu-id="918b0-130">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="918b0-130">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="918b0-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="918b0-131">NOTES</span></span>

## <span data-ttu-id="918b0-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="918b0-132">RELATED LINKS</span></span>

[<span data-ttu-id="918b0-133">New-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="918b0-133">New-AzCdnCustomDomain</span></span>](./New-AzCdnCustomDomain.md)

[<span data-ttu-id="918b0-134">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="918b0-134">Remove-AzCdnCustomDomain</span></span>](./Remove-AzCdnCustomDomain.md)


