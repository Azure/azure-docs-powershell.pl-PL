---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 8C4E824F-FB4A-4DE7-8FD9-3FDA3848F25C
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/test-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Test-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Test-AzCdnCustomDomain.md
ms.openlocfilehash: 8ceb1fe02ba4a7d5cf4435ac79d404b331b58ea9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195139"
---
# <span data-ttu-id="cd41b-101">Test-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="cd41b-101">Test-AzCdnCustomDomain</span></span>

## <span data-ttu-id="cd41b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd41b-102">SYNOPSIS</span></span>
<span data-ttu-id="cd41b-103">Sprawdza, czy można dodać domenę niestandardową do punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="cd41b-103">Checks whether a custom domain can be added to an endpoint.</span></span>

## <span data-ttu-id="cd41b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="cd41b-104">SYNTAX</span></span>

### <span data-ttu-id="cd41b-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="cd41b-105">ByFieldsParameterSet (Default)</span></span>
```
Test-AzCdnCustomDomain -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -CustomDomainHostName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd41b-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd41b-106">ByObjectParameterSet</span></span>
```
Test-AzCdnCustomDomain -CdnEndpoint <PSEndpoint> -CustomDomainHostName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd41b-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="cd41b-107">DESCRIPTION</span></span>
<span data-ttu-id="cd41b-108">Polecenie **cmdlet Test-AzCdnCustomDomain** sprawdza, czy można dodać domenę niestandardową do punktu końcowego przez sprawdzenie poprawności mapowania CName.</span><span class="sxs-lookup"><span data-stu-id="cd41b-108">The **Test-AzCdnCustomDomain** cmdlet checks whether a custom domain can be added to an endpoint by validating the CName mapping.</span></span>

## <span data-ttu-id="cd41b-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="cd41b-109">EXAMPLES</span></span>

## <span data-ttu-id="cd41b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cd41b-110">PARAMETERS</span></span>

### <span data-ttu-id="cd41b-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="cd41b-111">-CdnEndpoint</span></span>
<span data-ttu-id="cd41b-112">Określa punkt końcowy, do którego chcesz dodać domenę niestandardową.</span><span class="sxs-lookup"><span data-stu-id="cd41b-112">Specifies the endpoint to which you want to add the custom domain.</span></span>

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

### <span data-ttu-id="cd41b-113">-CustomDomainHostName</span><span class="sxs-lookup"><span data-stu-id="cd41b-113">-CustomDomainHostName</span></span>
<span data-ttu-id="cd41b-114">Określa nazwę hosta domeny niestandardowej.</span><span class="sxs-lookup"><span data-stu-id="cd41b-114">Specifies the host name of the custom domain.</span></span>

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

### <span data-ttu-id="cd41b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd41b-115">-DefaultProfile</span></span>
<span data-ttu-id="cd41b-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="cd41b-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cd41b-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="cd41b-117">-EndpointName</span></span>
<span data-ttu-id="cd41b-118">Określa nazwę punktu końcowego, do którego chcesz dodać domenę niestandardową.</span><span class="sxs-lookup"><span data-stu-id="cd41b-118">Specifies the name of the endpoint to which you want to add the custom domain.</span></span>

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

### <span data-ttu-id="cd41b-119">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="cd41b-119">-ProfileName</span></span>
<span data-ttu-id="cd41b-120">Określa nazwę profilu.</span><span class="sxs-lookup"><span data-stu-id="cd41b-120">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="cd41b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd41b-121">-ResourceGroupName</span></span>
<span data-ttu-id="cd41b-122">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cd41b-122">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="cd41b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd41b-123">CommonParameters</span></span>
<span data-ttu-id="cd41b-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd41b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd41b-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cd41b-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd41b-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cd41b-126">INPUTS</span></span>

### <span data-ttu-id="cd41b-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="cd41b-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="cd41b-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cd41b-128">OUTPUTS</span></span>

### <span data-ttu-id="cd41b-129">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateCustomDomainOutput</span><span class="sxs-lookup"><span data-stu-id="cd41b-129">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateCustomDomainOutput</span></span>

## <span data-ttu-id="cd41b-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="cd41b-130">NOTES</span></span>

## <span data-ttu-id="cd41b-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cd41b-131">RELATED LINKS</span></span>

[<span data-ttu-id="cd41b-132">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="cd41b-132">Get-AzCdnCustomDomain</span></span>](./Get-AzCdnCustomDomain.md)

[<span data-ttu-id="cd41b-133">New-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="cd41b-133">New-AzCdnCustomDomain</span></span>](./New-AzCdnCustomDomain.md)

[<span data-ttu-id="cd41b-134">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="cd41b-134">Remove-AzCdnCustomDomain</span></span>](./Remove-AzCdnCustomDomain.md)


