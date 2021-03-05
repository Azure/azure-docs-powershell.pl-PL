---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 8C4E824F-FB4A-4DE7-8FD9-3FDA3848F25C
online version: https://docs.microsoft.com/powershell/module/az.cdn/test-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Test-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Test-AzCdnCustomDomain.md
ms.openlocfilehash: b2c061f7755c7891946bcf8ea8f3fa5cdb15439d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986959"
---
# <span data-ttu-id="7027f-101">Test-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="7027f-101">Test-AzCdnCustomDomain</span></span>

## <span data-ttu-id="7027f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7027f-102">SYNOPSIS</span></span>
<span data-ttu-id="7027f-103">Sprawdza, czy można dodać domenę niestandardową do punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="7027f-103">Checks whether a custom domain can be added to an endpoint.</span></span>

## <span data-ttu-id="7027f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7027f-104">SYNTAX</span></span>

### <span data-ttu-id="7027f-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="7027f-105">ByFieldsParameterSet (Default)</span></span>
```
Test-AzCdnCustomDomain -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -CustomDomainHostName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7027f-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7027f-106">ByObjectParameterSet</span></span>
```
Test-AzCdnCustomDomain -CdnEndpoint <PSEndpoint> -CustomDomainHostName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7027f-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="7027f-107">DESCRIPTION</span></span>
<span data-ttu-id="7027f-108">Polecenie **cmdlet Test-AzCdnCustomDomain** sprawdza, czy można dodać domenę niestandardową do punktu końcowego przez sprawdzenie poprawności mapowania CName.</span><span class="sxs-lookup"><span data-stu-id="7027f-108">The **Test-AzCdnCustomDomain** cmdlet checks whether a custom domain can be added to an endpoint by validating the CName mapping.</span></span>

## <span data-ttu-id="7027f-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7027f-109">EXAMPLES</span></span>

## <span data-ttu-id="7027f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7027f-110">PARAMETERS</span></span>

### <span data-ttu-id="7027f-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="7027f-111">-CdnEndpoint</span></span>
<span data-ttu-id="7027f-112">Określa punkt końcowy, do którego chcesz dodać domenę niestandardową.</span><span class="sxs-lookup"><span data-stu-id="7027f-112">Specifies the endpoint to which you want to add the custom domain.</span></span>

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

### <span data-ttu-id="7027f-113">-CustomDomainHostName</span><span class="sxs-lookup"><span data-stu-id="7027f-113">-CustomDomainHostName</span></span>
<span data-ttu-id="7027f-114">Określa nazwę hosta domeny niestandardowej.</span><span class="sxs-lookup"><span data-stu-id="7027f-114">Specifies the host name of the custom domain.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7027f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7027f-115">-DefaultProfile</span></span>
<span data-ttu-id="7027f-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="7027f-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7027f-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="7027f-117">-EndpointName</span></span>
<span data-ttu-id="7027f-118">Określa nazwę punktu końcowego, do którego chcesz dodać domenę niestandardową.</span><span class="sxs-lookup"><span data-stu-id="7027f-118">Specifies the name of the endpoint to which you want to add the custom domain.</span></span>

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

### <span data-ttu-id="7027f-119">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="7027f-119">-ProfileName</span></span>
<span data-ttu-id="7027f-120">Określa nazwę profilu.</span><span class="sxs-lookup"><span data-stu-id="7027f-120">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="7027f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7027f-121">-ResourceGroupName</span></span>
<span data-ttu-id="7027f-122">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7027f-122">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="7027f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7027f-123">CommonParameters</span></span>
<span data-ttu-id="7027f-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7027f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7027f-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7027f-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7027f-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7027f-126">INPUTS</span></span>

### <span data-ttu-id="7027f-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="7027f-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="7027f-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7027f-128">OUTPUTS</span></span>

### <span data-ttu-id="7027f-129">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateCustomDomainOutput</span><span class="sxs-lookup"><span data-stu-id="7027f-129">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateCustomDomainOutput</span></span>

## <span data-ttu-id="7027f-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7027f-130">NOTES</span></span>

## <span data-ttu-id="7027f-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7027f-131">RELATED LINKS</span></span>

[<span data-ttu-id="7027f-132">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="7027f-132">Get-AzCdnCustomDomain</span></span>](./Get-AzCdnCustomDomain.md)

[<span data-ttu-id="7027f-133">New-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="7027f-133">New-AzCdnCustomDomain</span></span>](./New-AzCdnCustomDomain.md)

[<span data-ttu-id="7027f-134">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="7027f-134">Remove-AzCdnCustomDomain</span></span>](./Remove-AzCdnCustomDomain.md)


