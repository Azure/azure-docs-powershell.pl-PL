---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 7060D3D7-B397-447E-88E3-B6F0D094770D
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnCustomDomain.md
ms.openlocfilehash: 6a0a90657ee76401117971a29dc03a78a7330afc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365752"
---
# <span data-ttu-id="7c272-101">New-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="7c272-101">New-AzCdnCustomDomain</span></span>

## <span data-ttu-id="7c272-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7c272-102">SYNOPSIS</span></span>
<span data-ttu-id="7c272-103">Tworzy domenę niestandardową dla punktu końcowego sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="7c272-103">Creates a custom domain for a CDN endpoint.</span></span>

## <span data-ttu-id="7c272-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7c272-104">SYNTAX</span></span>

### <span data-ttu-id="7c272-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7c272-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnCustomDomain -HostName <String> -CustomDomainName <String> -EndpointName <String>
 -ProfileName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c272-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c272-106">ByObjectParameterSet</span></span>
```
New-AzCdnCustomDomain -HostName <String> -CustomDomainName <String> -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c272-107">Opis</span><span class="sxs-lookup"><span data-stu-id="7c272-107">DESCRIPTION</span></span>
<span data-ttu-id="7c272-108">Polecenie cmdlet **New-AzCdnCustomDomain** tworzy domenę niestandardową dla punktu końcowego sieci dostarczania zawartości Azure (CDN).</span><span class="sxs-lookup"><span data-stu-id="7c272-108">The **New-AzCdnCustomDomain** cmdlet creates a custom domain for the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="7c272-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7c272-109">EXAMPLES</span></span>

## <span data-ttu-id="7c272-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7c272-110">PARAMETERS</span></span>

### <span data-ttu-id="7c272-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="7c272-111">-CdnEndpoint</span></span>
<span data-ttu-id="7c272-112">Określa obiekt punktu końcowego sieci CDN, do którego jest dodawana domena niestandardowa.</span><span class="sxs-lookup"><span data-stu-id="7c272-112">Specifies the CDN endpoint object to which the custom domain is added.</span></span>

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

### <span data-ttu-id="7c272-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="7c272-113">-CustomDomainName</span></span>
<span data-ttu-id="7c272-114">Określa nazwę zasobu domeny niestandardowej.</span><span class="sxs-lookup"><span data-stu-id="7c272-114">Specifies the resource name of the custom domain.</span></span>

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

### <span data-ttu-id="7c272-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c272-115">-DefaultProfile</span></span>
<span data-ttu-id="7c272-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="7c272-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7c272-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="7c272-117">-EndpointName</span></span>
<span data-ttu-id="7c272-118">Określa nazwę punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="7c272-118">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="7c272-119">-HostName</span><span class="sxs-lookup"><span data-stu-id="7c272-119">-HostName</span></span>
<span data-ttu-id="7c272-120">Określa nazwę hosta domeny niestandardowej.</span><span class="sxs-lookup"><span data-stu-id="7c272-120">Specifies the host name of the custom domain.</span></span>

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

### <span data-ttu-id="7c272-121">-Refilename</span><span class="sxs-lookup"><span data-stu-id="7c272-121">-ProfileName</span></span>
<span data-ttu-id="7c272-122">Określa nazwę profilu.</span><span class="sxs-lookup"><span data-stu-id="7c272-122">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="7c272-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c272-123">-ResourceGroupName</span></span>
<span data-ttu-id="7c272-124">Określa nazwę grupy zasobów, do której należy domena niestandardowa.</span><span class="sxs-lookup"><span data-stu-id="7c272-124">Specifies the name of the resource group to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="7c272-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7c272-125">-Confirm</span></span>
<span data-ttu-id="7c272-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c272-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c272-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c272-127">-WhatIf</span></span>
<span data-ttu-id="7c272-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c272-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c272-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7c272-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c272-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c272-130">CommonParameters</span></span>
<span data-ttu-id="7c272-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c272-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c272-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7c272-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c272-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7c272-133">INPUTS</span></span>

### <span data-ttu-id="7c272-134">Microsoft. Azure. Commands. CDN. models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="7c272-134">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="7c272-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7c272-135">OUTPUTS</span></span>

### <span data-ttu-id="7c272-136">Microsoft. Azure. Commands. CDN. models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="7c272-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="7c272-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7c272-137">NOTES</span></span>

## <span data-ttu-id="7c272-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7c272-138">RELATED LINKS</span></span>

[<span data-ttu-id="7c272-139">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="7c272-139">Get-AzCdnCustomDomain</span></span>](./Get-AzCdnCustomDomain.md)

[<span data-ttu-id="7c272-140">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="7c272-140">Remove-AzCdnCustomDomain</span></span>](./Remove-AzCdnCustomDomain.md)

[<span data-ttu-id="7c272-141">Test — AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="7c272-141">Test-AzCdnCustomDomain</span></span>](./Test-AzCdnCustomDomain.md)


