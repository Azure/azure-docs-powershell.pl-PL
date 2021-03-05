---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 7060D3D7-B397-447E-88E3-B6F0D094770D
online version: https://docs.microsoft.com/powershell/module/az.cdn/new-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnCustomDomain.md
ms.openlocfilehash: 58e4d922d74f36f6f472cf3bfef8e0d0d45155d2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010794"
---
# <span data-ttu-id="1158b-101">New-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="1158b-101">New-AzCdnCustomDomain</span></span>

## <span data-ttu-id="1158b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1158b-102">SYNOPSIS</span></span>
<span data-ttu-id="1158b-103">Tworzy domenę niestandardową dla punktu końcowego sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="1158b-103">Creates a custom domain for a CDN endpoint.</span></span>

## <span data-ttu-id="1158b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1158b-104">SYNTAX</span></span>

### <span data-ttu-id="1158b-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="1158b-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnCustomDomain -HostName <String> -CustomDomainName <String> -EndpointName <String>
 -ProfileName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1158b-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1158b-106">ByObjectParameterSet</span></span>
```
New-AzCdnCustomDomain -HostName <String> -CustomDomainName <String> -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1158b-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="1158b-107">DESCRIPTION</span></span>
<span data-ttu-id="1158b-108">Polecenie **cmdlet New-AzCdnCustomDomain** tworzy domenę niestandardową dla punktu końcowego usługi Azure Content Delivery Network (CDN).</span><span class="sxs-lookup"><span data-stu-id="1158b-108">The **New-AzCdnCustomDomain** cmdlet creates a custom domain for the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="1158b-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1158b-109">EXAMPLES</span></span>

## <span data-ttu-id="1158b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1158b-110">PARAMETERS</span></span>

### <span data-ttu-id="1158b-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="1158b-111">-CdnEndpoint</span></span>
<span data-ttu-id="1158b-112">Określa obiekt punktu końcowego sieci CDN, do którego dodano domenę niestandardową.</span><span class="sxs-lookup"><span data-stu-id="1158b-112">Specifies the CDN endpoint object to which the custom domain is added.</span></span>

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

### <span data-ttu-id="1158b-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="1158b-113">-CustomDomainName</span></span>
<span data-ttu-id="1158b-114">Określa nazwę zasobu domeny niestandardowej.</span><span class="sxs-lookup"><span data-stu-id="1158b-114">Specifies the resource name of the custom domain.</span></span>

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

### <span data-ttu-id="1158b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1158b-115">-DefaultProfile</span></span>
<span data-ttu-id="1158b-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="1158b-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1158b-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="1158b-117">-EndpointName</span></span>
<span data-ttu-id="1158b-118">Określa nazwę punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="1158b-118">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="1158b-119">-HostName</span><span class="sxs-lookup"><span data-stu-id="1158b-119">-HostName</span></span>
<span data-ttu-id="1158b-120">Określa nazwę hosta domeny niestandardowej.</span><span class="sxs-lookup"><span data-stu-id="1158b-120">Specifies the host name of the custom domain.</span></span>

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

### <span data-ttu-id="1158b-121">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="1158b-121">-ProfileName</span></span>
<span data-ttu-id="1158b-122">Określa nazwę profilu.</span><span class="sxs-lookup"><span data-stu-id="1158b-122">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="1158b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1158b-123">-ResourceGroupName</span></span>
<span data-ttu-id="1158b-124">Określa nazwę grupy zasobów, do której należy domena niestandardowa.</span><span class="sxs-lookup"><span data-stu-id="1158b-124">Specifies the name of the resource group to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="1158b-125">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1158b-125">-Confirm</span></span>
<span data-ttu-id="1158b-126">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1158b-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1158b-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1158b-127">-WhatIf</span></span>
<span data-ttu-id="1158b-128">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1158b-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1158b-129">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="1158b-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1158b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1158b-130">CommonParameters</span></span>
<span data-ttu-id="1158b-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1158b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1158b-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1158b-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1158b-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1158b-133">INPUTS</span></span>

### <span data-ttu-id="1158b-134">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="1158b-134">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="1158b-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1158b-135">OUTPUTS</span></span>

### <span data-ttu-id="1158b-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="1158b-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="1158b-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1158b-137">NOTES</span></span>

## <span data-ttu-id="1158b-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1158b-138">RELATED LINKS</span></span>

[<span data-ttu-id="1158b-139">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="1158b-139">Get-AzCdnCustomDomain</span></span>](./Get-AzCdnCustomDomain.md)

[<span data-ttu-id="1158b-140">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="1158b-140">Remove-AzCdnCustomDomain</span></span>](./Remove-AzCdnCustomDomain.md)

[<span data-ttu-id="1158b-141">Test-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="1158b-141">Test-AzCdnCustomDomain</span></span>](./Test-AzCdnCustomDomain.md)


