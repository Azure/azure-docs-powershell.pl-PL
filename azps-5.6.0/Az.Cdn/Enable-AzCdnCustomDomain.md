---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/enable-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Enable-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Enable-AzCdnCustomDomain.md
ms.openlocfilehash: 82d980768147bb82332dae2dfa8965d962cc882e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956017"
---
# <span data-ttu-id="58495-101">Enable-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="58495-101">Enable-AzCdnCustomDomain</span></span>

## <span data-ttu-id="58495-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58495-102">SYNOPSIS</span></span>
<span data-ttu-id="58495-103">Włącza domenę niestandardową HTTPS (przestarzałe).</span><span class="sxs-lookup"><span data-stu-id="58495-103">Enables Custom Domain HTTPS (Deprecated).</span></span>

## <span data-ttu-id="58495-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="58495-104">SYNTAX</span></span>

### <span data-ttu-id="58495-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="58495-105">ByFieldsParameterSet (Default)</span></span>
```
Enable-AzCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="58495-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="58495-106">ByObjectParameterSet</span></span>
```
Enable-AzCdnCustomDomain -InputObject <PSCustomDomain> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58495-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="58495-107">DESCRIPTION</span></span>
<span data-ttu-id="58495-108">Polecenie **cmdlet Enable-AzCdnCustomDomain** umożliwia dostarczenie zabezpieczonego protokołu HTTPS domeny niestandardowej CDN.</span><span class="sxs-lookup"><span data-stu-id="58495-108">The **Enable-AzCdnCustomDomain** cmdlet enables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="58495-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="58495-109">EXAMPLES</span></span>

### <span data-ttu-id="58495-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="58495-110">Example 1</span></span>
```powershell
Enable-AzCdnCustomDomain -CustomDomainName $customDomainName -EndpointName $endpointName -ProfileName $profileName -ResourceGroupName $resourceGroupName
true
```

<span data-ttu-id="58495-111">Włącz dostarczanie https domeny niestandardowej.</span><span class="sxs-lookup"><span data-stu-id="58495-111">Enable https delivery of the custom domain.</span></span>

## <span data-ttu-id="58495-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="58495-112">PARAMETERS</span></span>

### <span data-ttu-id="58495-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="58495-113">-CustomDomainName</span></span>
<span data-ttu-id="58495-114">Nazwa wyświetlana niestandardowej domeny sieci Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="58495-114">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="58495-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58495-115">-DefaultProfile</span></span>
<span data-ttu-id="58495-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="58495-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58495-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="58495-117">-EndpointName</span></span>
<span data-ttu-id="58495-118">Nazwa punktu końcowego sieci Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="58495-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="58495-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="58495-119">-InputObject</span></span>
<span data-ttu-id="58495-120">Obiekt domeny niestandardowej.</span><span class="sxs-lookup"><span data-stu-id="58495-120">The custom domain object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="58495-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="58495-121">-PassThru</span></span>
<span data-ttu-id="58495-122">Zwracany obiekt (jeśli jest określony).</span><span class="sxs-lookup"><span data-stu-id="58495-122">Return object (if specified).</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58495-123">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="58495-123">-ProfileName</span></span>
<span data-ttu-id="58495-124">Nazwa profilu azure CDN.</span><span class="sxs-lookup"><span data-stu-id="58495-124">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="58495-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58495-125">-ResourceGroupName</span></span>
<span data-ttu-id="58495-126">Grupa zasobów profilu azure CDN.</span><span class="sxs-lookup"><span data-stu-id="58495-126">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="58495-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="58495-127">-Confirm</span></span>
<span data-ttu-id="58495-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="58495-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58495-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58495-129">-WhatIf</span></span>
<span data-ttu-id="58495-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58495-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="58495-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="58495-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58495-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58495-132">CommonParameters</span></span>
<span data-ttu-id="58495-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58495-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58495-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="58495-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58495-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="58495-135">INPUTS</span></span>

### <span data-ttu-id="58495-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="58495-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="58495-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="58495-137">OUTPUTS</span></span>

### <span data-ttu-id="58495-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="58495-138">System.Boolean</span></span>

## <span data-ttu-id="58495-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="58495-139">NOTES</span></span>

## <span data-ttu-id="58495-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="58495-140">RELATED LINKS</span></span>
