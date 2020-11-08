---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/enable-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Enable-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Enable-AzCdnCustomDomain.md
ms.openlocfilehash: 9cf4633f464316d41034a0cb2d79384e229bcf4c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94049776"
---
# <span data-ttu-id="53dd1-101">Enable-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="53dd1-101">Enable-AzCdnCustomDomain</span></span>

## <span data-ttu-id="53dd1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="53dd1-102">SYNOPSIS</span></span>
<span data-ttu-id="53dd1-103">Umożliwia włączenie niestandardowego HTTPS domeny (przestarzałe).</span><span class="sxs-lookup"><span data-stu-id="53dd1-103">Enables Custom Domain HTTPS (Deprecated).</span></span>

## <span data-ttu-id="53dd1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="53dd1-104">SYNTAX</span></span>

### <span data-ttu-id="53dd1-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="53dd1-105">ByFieldsParameterSet (Default)</span></span>
```
Enable-AzCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="53dd1-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="53dd1-106">ByObjectParameterSet</span></span>
```
Enable-AzCdnCustomDomain -InputObject <PSCustomDomain> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53dd1-107">Opis</span><span class="sxs-lookup"><span data-stu-id="53dd1-107">DESCRIPTION</span></span>
<span data-ttu-id="53dd1-108">Polecenie cmdlet **enable-AzCdnCustomDomain** włącza zabezpieczoną dostawę https domeny NIESTANDARDOWEJ usługi CDN.</span><span class="sxs-lookup"><span data-stu-id="53dd1-108">The **Enable-AzCdnCustomDomain** cmdlet enables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="53dd1-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="53dd1-109">EXAMPLES</span></span>

### <span data-ttu-id="53dd1-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="53dd1-110">Example 1</span></span>
```powershell
Enable-AzCdnCustomDomain -CustomDomainName $customDomainName -EndpointName $endpointName -ProfileName $profileName -ResourceGroupName $resourceGroupName
true
```

<span data-ttu-id="53dd1-111">Włącz dostarczanie za pomocą protokołu HTTPS domeny niestandardowej.</span><span class="sxs-lookup"><span data-stu-id="53dd1-111">Enable https delivery of the custom domain.</span></span>

## <span data-ttu-id="53dd1-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="53dd1-112">PARAMETERS</span></span>

### <span data-ttu-id="53dd1-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="53dd1-113">-CustomDomainName</span></span>
<span data-ttu-id="53dd1-114">Nazwa wyświetlana domeny niestandardowej usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="53dd1-114">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="53dd1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53dd1-115">-DefaultProfile</span></span>
<span data-ttu-id="53dd1-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="53dd1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53dd1-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="53dd1-117">-EndpointName</span></span>
<span data-ttu-id="53dd1-118">Nazwa punktu końcowego usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="53dd1-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="53dd1-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="53dd1-119">-InputObject</span></span>
<span data-ttu-id="53dd1-120">Niestandardowy obiekt domeny.</span><span class="sxs-lookup"><span data-stu-id="53dd1-120">The custom domain object.</span></span>

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

### <span data-ttu-id="53dd1-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="53dd1-121">-PassThru</span></span>
<span data-ttu-id="53dd1-122">Zwraca obiekt (jeśli jest określony).</span><span class="sxs-lookup"><span data-stu-id="53dd1-122">Return object (if specified).</span></span>

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

### <span data-ttu-id="53dd1-123">-Refilename</span><span class="sxs-lookup"><span data-stu-id="53dd1-123">-ProfileName</span></span>
<span data-ttu-id="53dd1-124">Nazwa profilu usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="53dd1-124">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="53dd1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53dd1-125">-ResourceGroupName</span></span>
<span data-ttu-id="53dd1-126">Grupa zasobów profilu usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="53dd1-126">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="53dd1-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="53dd1-127">-Confirm</span></span>
<span data-ttu-id="53dd1-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53dd1-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53dd1-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53dd1-129">-WhatIf</span></span>
<span data-ttu-id="53dd1-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53dd1-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="53dd1-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="53dd1-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53dd1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53dd1-132">CommonParameters</span></span>
<span data-ttu-id="53dd1-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53dd1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53dd1-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="53dd1-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53dd1-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="53dd1-135">INPUTS</span></span>

### <span data-ttu-id="53dd1-136">Microsoft. Azure. Commands. CDN. models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="53dd1-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="53dd1-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="53dd1-137">OUTPUTS</span></span>

### <span data-ttu-id="53dd1-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="53dd1-138">System.Boolean</span></span>

## <span data-ttu-id="53dd1-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="53dd1-139">NOTES</span></span>

## <span data-ttu-id="53dd1-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="53dd1-140">RELATED LINKS</span></span>