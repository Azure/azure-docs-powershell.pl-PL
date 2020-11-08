---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/disable-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomain.md
ms.openlocfilehash: 3352991d73bcef2e4f5b6475c9c71d5f48eaa526
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94049943"
---
# <span data-ttu-id="26dec-101">Disable-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="26dec-101">Disable-AzCdnCustomDomain</span></span>

## <span data-ttu-id="26dec-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="26dec-102">SYNOPSIS</span></span>
<span data-ttu-id="26dec-103">Wyłącza niestandardową HTTPS domeny (przestarzałe).</span><span class="sxs-lookup"><span data-stu-id="26dec-103">Disables Custom Domain HTTPS (Deprecated).</span></span>

## <span data-ttu-id="26dec-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="26dec-104">SYNTAX</span></span>

### <span data-ttu-id="26dec-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="26dec-105">ByFieldsParameterSet (Default)</span></span>
```
Disable-AzCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="26dec-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="26dec-106">ByObjectParameterSet</span></span>
```
Disable-AzCdnCustomDomain -InputObject <PSCustomDomain> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26dec-107">Opis</span><span class="sxs-lookup"><span data-stu-id="26dec-107">DESCRIPTION</span></span>
<span data-ttu-id="26dec-108">Polecenie cmdlet **disable-AzCdnCustomDomain** wyłącza zabezpieczoną dostawę https domeny NIESTANDARDOWEJ usługi CDN.</span><span class="sxs-lookup"><span data-stu-id="26dec-108">The **Disable-AzCdnCustomDomain** cmdlet disables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="26dec-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="26dec-109">EXAMPLES</span></span>

### <span data-ttu-id="26dec-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="26dec-110">Example 1</span></span>
```powershell
Disable-AzCdnCustomDomain -CustomDomainName $customDomainName -EndpointName $endpointName -ProfileName $profileName -ResourceGroupName $resourceGroupName
true
```

<span data-ttu-id="26dec-111">Wyłącz dostarczanie https domeny niestandardowej.</span><span class="sxs-lookup"><span data-stu-id="26dec-111">Disable https delivery of the custom domain.</span></span>

## <span data-ttu-id="26dec-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="26dec-112">PARAMETERS</span></span>

### <span data-ttu-id="26dec-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="26dec-113">-CustomDomainName</span></span>
<span data-ttu-id="26dec-114">Nazwa wyświetlana domeny niestandardowej usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="26dec-114">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="26dec-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26dec-115">-DefaultProfile</span></span>
<span data-ttu-id="26dec-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="26dec-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26dec-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="26dec-117">-EndpointName</span></span>
<span data-ttu-id="26dec-118">Nazwa punktu końcowego usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="26dec-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="26dec-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="26dec-119">-InputObject</span></span>
<span data-ttu-id="26dec-120">Niestandardowy obiekt domeny.</span><span class="sxs-lookup"><span data-stu-id="26dec-120">The custom domain object.</span></span>

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

### <span data-ttu-id="26dec-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="26dec-121">-PassThru</span></span>
<span data-ttu-id="26dec-122">Zwraca obiekt (jeśli jest określony).</span><span class="sxs-lookup"><span data-stu-id="26dec-122">Return object (if specified).</span></span>

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

### <span data-ttu-id="26dec-123">-Refilename</span><span class="sxs-lookup"><span data-stu-id="26dec-123">-ProfileName</span></span>
<span data-ttu-id="26dec-124">Nazwa profilu usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="26dec-124">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="26dec-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26dec-125">-ResourceGroupName</span></span>
<span data-ttu-id="26dec-126">Grupa zasobów profilu usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="26dec-126">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="26dec-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="26dec-127">-Confirm</span></span>
<span data-ttu-id="26dec-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26dec-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26dec-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26dec-129">-WhatIf</span></span>
<span data-ttu-id="26dec-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26dec-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="26dec-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="26dec-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26dec-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26dec-132">CommonParameters</span></span>
<span data-ttu-id="26dec-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26dec-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26dec-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="26dec-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26dec-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="26dec-135">INPUTS</span></span>

### <span data-ttu-id="26dec-136">Microsoft. Azure. Commands. CDN. models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="26dec-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="26dec-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="26dec-137">OUTPUTS</span></span>

### <span data-ttu-id="26dec-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="26dec-138">System.Boolean</span></span>

## <span data-ttu-id="26dec-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="26dec-139">NOTES</span></span>

## <span data-ttu-id="26dec-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="26dec-140">RELATED LINKS</span></span>
