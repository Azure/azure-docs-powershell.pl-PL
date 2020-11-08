---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/disable-azcdncustomdomainhttps
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomainHttps.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomainHttps.md
ms.openlocfilehash: be3e4d0437e24a282c1933cf82e1818dd9f88221
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222660"
---
# <span data-ttu-id="ca50c-101">Disable-AzCdnCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="ca50c-101">Disable-AzCdnCustomDomainHttps</span></span>

## <span data-ttu-id="ca50c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ca50c-102">SYNOPSIS</span></span>
<span data-ttu-id="ca50c-103">Wyłącza niestandardową HTTPS domeny.</span><span class="sxs-lookup"><span data-stu-id="ca50c-103">Disables Custom Domain HTTPS.</span></span>

## <span data-ttu-id="ca50c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ca50c-104">SYNTAX</span></span>

### <span data-ttu-id="ca50c-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ca50c-105">ByFieldsParameterSet (Default)</span></span>
```
Disable-AzCdnCustomDomainHttps -ResourceGroupName <String> -ProfileName <String> -EndpointName <String>
 -CustomDomainName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ca50c-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca50c-106">ByObjectParameterSet</span></span>
```
Disable-AzCdnCustomDomainHttps -InputObject <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca50c-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca50c-107">ByResourceIdParameterSet</span></span>
```
Disable-AzCdnCustomDomainHttps -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca50c-108">Opis</span><span class="sxs-lookup"><span data-stu-id="ca50c-108">DESCRIPTION</span></span>
<span data-ttu-id="ca50c-109">Polecenie cmdlet **disable-AzCdnCustomDomainHttps** wyłącza zabezpieczoną dostawę https domeny NIESTANDARDOWEJ usługi CDN.</span><span class="sxs-lookup"><span data-stu-id="ca50c-109">The **Disable-AzCdnCustomDomainHttps** cmdlet disables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="ca50c-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ca50c-110">EXAMPLES</span></span>

### <span data-ttu-id="ca50c-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ca50c-111">Example 1</span></span>
```powershell
PS C:\> Disable-AzCdnCustomDomainHttps -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -CustomDomainName $customDomainName
```

<span data-ttu-id="ca50c-112">Wyłącz bezpieczną dostarczenie domeny niestandardowej.</span><span class="sxs-lookup"><span data-stu-id="ca50c-112">Disable secure delivery of the custom domain.</span></span>

## <span data-ttu-id="ca50c-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ca50c-113">PARAMETERS</span></span>

### <span data-ttu-id="ca50c-114">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="ca50c-114">-CustomDomainName</span></span>
<span data-ttu-id="ca50c-115">Nazwa wyświetlana domeny niestandardowej usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="ca50c-115">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="ca50c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca50c-116">-DefaultProfile</span></span>
<span data-ttu-id="ca50c-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ca50c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca50c-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="ca50c-118">-EndpointName</span></span>
<span data-ttu-id="ca50c-119">Nazwa punktu końcowego usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="ca50c-119">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="ca50c-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ca50c-120">-InputObject</span></span>
<span data-ttu-id="ca50c-121">Niestandardowy obiekt domeny.</span><span class="sxs-lookup"><span data-stu-id="ca50c-121">The custom domain object.</span></span>

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

### <span data-ttu-id="ca50c-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ca50c-122">-PassThru</span></span>
<span data-ttu-id="ca50c-123">Zwraca obiekt, jeśli jest określony.</span><span class="sxs-lookup"><span data-stu-id="ca50c-123">Return object if specified.</span></span>

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

### <span data-ttu-id="ca50c-124">-Refilename</span><span class="sxs-lookup"><span data-stu-id="ca50c-124">-ProfileName</span></span>
<span data-ttu-id="ca50c-125">Nazwa profilu usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="ca50c-125">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="ca50c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca50c-126">-ResourceGroupName</span></span>
<span data-ttu-id="ca50c-127">Grupa zasobów profilu usługi Azure CDN</span><span class="sxs-lookup"><span data-stu-id="ca50c-127">The resource group of the Azure CDN profile</span></span>

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

### <span data-ttu-id="ca50c-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ca50c-128">-ResourceId</span></span>
<span data-ttu-id="ca50c-129">Identyfikator zasobu domeny niestandardowej</span><span class="sxs-lookup"><span data-stu-id="ca50c-129">ResourceId of the Custom Domain</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca50c-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ca50c-130">-Confirm</span></span>
<span data-ttu-id="ca50c-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca50c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca50c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca50c-132">-WhatIf</span></span>
<span data-ttu-id="ca50c-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca50c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca50c-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ca50c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca50c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca50c-135">CommonParameters</span></span>
<span data-ttu-id="ca50c-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca50c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca50c-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ca50c-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca50c-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ca50c-138">INPUTS</span></span>

### <span data-ttu-id="ca50c-139">Microsoft. Azure. Commands. CDN. models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="ca50c-139">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

### <span data-ttu-id="ca50c-140">System. String</span><span class="sxs-lookup"><span data-stu-id="ca50c-140">System.String</span></span>

## <span data-ttu-id="ca50c-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ca50c-141">OUTPUTS</span></span>

### <span data-ttu-id="ca50c-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ca50c-142">System.Boolean</span></span>

## <span data-ttu-id="ca50c-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ca50c-143">NOTES</span></span>

## <span data-ttu-id="ca50c-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ca50c-144">RELATED LINKS</span></span>
