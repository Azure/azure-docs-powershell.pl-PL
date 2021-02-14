---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 53246003-D1E9-4863-94E9-8E0BF1272134
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnCustomDomain.md
ms.openlocfilehash: c98ec2ebee71188ddbc5760dbbd3d1528da3c770
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195171"
---
# <span data-ttu-id="d6dc7-101">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="d6dc7-101">Get-AzCdnCustomDomain</span></span>

## <span data-ttu-id="d6dc7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6dc7-102">SYNOPSIS</span></span>
<span data-ttu-id="d6dc7-103">Pobiera domenę niestandardową CDN.</span><span class="sxs-lookup"><span data-stu-id="d6dc7-103">Gets a CDN custom domain.</span></span>

## <span data-ttu-id="d6dc7-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d6dc7-104">SYNTAX</span></span>

### <span data-ttu-id="d6dc7-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="d6dc7-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnCustomDomain [-CustomDomainName <String>] -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6dc7-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6dc7-106">ByObjectParameterSet</span></span>
```
Get-AzCdnCustomDomain [-CustomDomainName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6dc7-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="d6dc7-107">DESCRIPTION</span></span>
<span data-ttu-id="d6dc7-108">Polecenie **cmdlet Get-AzCdnCustomDomain** otrzymuje domenę niestandardową Azure Content Delivery Network (CDN) i powiązane z nią ustawienia.</span><span class="sxs-lookup"><span data-stu-id="d6dc7-108">The **Get-AzCdnCustomDomain** cmdlet gets an Azure Content Delivery Network (CDN) custom domain and its related settings.</span></span>

## <span data-ttu-id="d6dc7-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d6dc7-109">EXAMPLES</span></span>

## <span data-ttu-id="d6dc7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d6dc7-110">PARAMETERS</span></span>

### <span data-ttu-id="d6dc7-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="d6dc7-111">-CdnEndpoint</span></span>
<span data-ttu-id="d6dc7-112">Określa obiekt punktu końcowego sieci CDN, którego członkiem jest domena niestandardowa.</span><span class="sxs-lookup"><span data-stu-id="d6dc7-112">Specifies the CDN endpoint object of which the custom domain is a member.</span></span>

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

### <span data-ttu-id="d6dc7-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="d6dc7-113">-CustomDomainName</span></span>
<span data-ttu-id="d6dc7-114">Określa nazwę domeny niestandardowej.</span><span class="sxs-lookup"><span data-stu-id="d6dc7-114">Specifies the name of the custom domain.</span></span>
<span data-ttu-id="d6dc7-115">Nazwa domeny niestandardowej różni się od nazwy hosta domeny niestandardowej.</span><span class="sxs-lookup"><span data-stu-id="d6dc7-115">The name of the custom domain differs from the host name of the custom domain.</span></span>

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

### <span data-ttu-id="d6dc7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6dc7-116">-DefaultProfile</span></span>
<span data-ttu-id="d6dc7-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="d6dc7-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d6dc7-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="d6dc7-118">-EndpointName</span></span>
<span data-ttu-id="d6dc7-119">Określa nazwę punktu końcowego, do którego należy domena niestandardowa.</span><span class="sxs-lookup"><span data-stu-id="d6dc7-119">Specifies the name of the endpoint to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="d6dc7-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="d6dc7-120">-ProfileName</span></span>
<span data-ttu-id="d6dc7-121">Określa nazwę profilu, do którego należy domena niestandardowa.</span><span class="sxs-lookup"><span data-stu-id="d6dc7-121">Specifies the name of the Profile to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="d6dc7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6dc7-122">-ResourceGroupName</span></span>
<span data-ttu-id="d6dc7-123">Określa nazwę grupy zasobów, do której należy domena niestandardowa.</span><span class="sxs-lookup"><span data-stu-id="d6dc7-123">Specifies the name of the resource group to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="d6dc7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6dc7-124">CommonParameters</span></span>
<span data-ttu-id="d6dc7-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6dc7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6dc7-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d6dc7-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6dc7-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d6dc7-127">INPUTS</span></span>

### <span data-ttu-id="d6dc7-128">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="d6dc7-128">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="d6dc7-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d6dc7-129">OUTPUTS</span></span>

### <span data-ttu-id="d6dc7-130">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="d6dc7-130">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="d6dc7-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d6dc7-131">NOTES</span></span>

## <span data-ttu-id="d6dc7-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d6dc7-132">RELATED LINKS</span></span>

[<span data-ttu-id="d6dc7-133">New-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="d6dc7-133">New-AzCdnCustomDomain</span></span>](./New-AzCdnCustomDomain.md)

[<span data-ttu-id="d6dc7-134">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="d6dc7-134">Remove-AzCdnCustomDomain</span></span>](./Remove-AzCdnCustomDomain.md)


