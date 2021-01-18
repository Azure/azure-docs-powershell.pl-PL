---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/disable-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomain.md
ms.openlocfilehash: 3352991d73bcef2e4f5b6475c9c71d5f48eaa526
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502032"
---
# <span data-ttu-id="2dd09-101">Disable-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="2dd09-101">Disable-AzCdnCustomDomain</span></span>

## <span data-ttu-id="2dd09-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2dd09-102">SYNOPSIS</span></span>
<span data-ttu-id="2dd09-103">Wyłącza niestandardową HTTPS domeny (przestarzałe).</span><span class="sxs-lookup"><span data-stu-id="2dd09-103">Disables Custom Domain HTTPS (Deprecated).</span></span>

## <span data-ttu-id="2dd09-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2dd09-104">SYNTAX</span></span>

### <span data-ttu-id="2dd09-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2dd09-105">ByFieldsParameterSet (Default)</span></span>
```
Disable-AzCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2dd09-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2dd09-106">ByObjectParameterSet</span></span>
```
Disable-AzCdnCustomDomain -InputObject <PSCustomDomain> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2dd09-107">Opis</span><span class="sxs-lookup"><span data-stu-id="2dd09-107">DESCRIPTION</span></span>
<span data-ttu-id="2dd09-108">Polecenie cmdlet **disable-AzCdnCustomDomain** wyłącza zabezpieczoną dostawę https domeny NIESTANDARDOWEJ usługi CDN.</span><span class="sxs-lookup"><span data-stu-id="2dd09-108">The **Disable-AzCdnCustomDomain** cmdlet disables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="2dd09-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2dd09-109">EXAMPLES</span></span>

### <span data-ttu-id="2dd09-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2dd09-110">Example 1</span></span>
```powershell
Disable-AzCdnCustomDomain -CustomDomainName $customDomainName -EndpointName $endpointName -ProfileName $profileName -ResourceGroupName $resourceGroupName
true
```

<span data-ttu-id="2dd09-111">Wyłącz dostarczanie https domeny niestandardowej.</span><span class="sxs-lookup"><span data-stu-id="2dd09-111">Disable https delivery of the custom domain.</span></span>

## <span data-ttu-id="2dd09-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2dd09-112">PARAMETERS</span></span>

### <span data-ttu-id="2dd09-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="2dd09-113">-CustomDomainName</span></span>
<span data-ttu-id="2dd09-114">Nazwa wyświetlana domeny niestandardowej usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="2dd09-114">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="2dd09-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dd09-115">-DefaultProfile</span></span>
<span data-ttu-id="2dd09-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2dd09-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2dd09-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="2dd09-117">-EndpointName</span></span>
<span data-ttu-id="2dd09-118">Nazwa punktu końcowego usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="2dd09-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="2dd09-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2dd09-119">-InputObject</span></span>
<span data-ttu-id="2dd09-120">Niestandardowy obiekt domeny.</span><span class="sxs-lookup"><span data-stu-id="2dd09-120">The custom domain object.</span></span>

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

### <span data-ttu-id="2dd09-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2dd09-121">-PassThru</span></span>
<span data-ttu-id="2dd09-122">Zwraca obiekt (jeśli jest określony).</span><span class="sxs-lookup"><span data-stu-id="2dd09-122">Return object (if specified).</span></span>

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

### <span data-ttu-id="2dd09-123">-Refilename</span><span class="sxs-lookup"><span data-stu-id="2dd09-123">-ProfileName</span></span>
<span data-ttu-id="2dd09-124">Nazwa profilu usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="2dd09-124">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="2dd09-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2dd09-125">-ResourceGroupName</span></span>
<span data-ttu-id="2dd09-126">Grupa zasobów profilu usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="2dd09-126">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="2dd09-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2dd09-127">-Confirm</span></span>
<span data-ttu-id="2dd09-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2dd09-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2dd09-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2dd09-129">-WhatIf</span></span>
<span data-ttu-id="2dd09-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2dd09-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2dd09-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2dd09-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2dd09-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dd09-132">CommonParameters</span></span>
<span data-ttu-id="2dd09-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2dd09-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dd09-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2dd09-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dd09-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2dd09-135">INPUTS</span></span>

### <span data-ttu-id="2dd09-136">Microsoft. Azure. Commands. CDN. models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="2dd09-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="2dd09-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2dd09-137">OUTPUTS</span></span>

### <span data-ttu-id="2dd09-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2dd09-138">System.Boolean</span></span>

## <span data-ttu-id="2dd09-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2dd09-139">NOTES</span></span>

## <span data-ttu-id="2dd09-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2dd09-140">RELATED LINKS</span></span>
