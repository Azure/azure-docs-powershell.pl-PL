---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/disable-azcdncustomdomainhttps
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomainHttps.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomainHttps.md
ms.openlocfilehash: 837def99279905e3c647ecd8805ed0284840f5a4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978833"
---
# <span data-ttu-id="2a1a2-101">Disable-AzCdnCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="2a1a2-101">Disable-AzCdnCustomDomainHttps</span></span>

## <span data-ttu-id="2a1a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a1a2-102">SYNOPSIS</span></span>
<span data-ttu-id="2a1a2-103">Wyłącza protokół HTTPS domeny niestandardowej.</span><span class="sxs-lookup"><span data-stu-id="2a1a2-103">Disables Custom Domain HTTPS.</span></span>

## <span data-ttu-id="2a1a2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2a1a2-104">SYNTAX</span></span>

### <span data-ttu-id="2a1a2-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="2a1a2-105">ByFieldsParameterSet (Default)</span></span>
```
Disable-AzCdnCustomDomainHttps -ResourceGroupName <String> -ProfileName <String> -EndpointName <String>
 -CustomDomainName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2a1a2-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2a1a2-106">ByObjectParameterSet</span></span>
```
Disable-AzCdnCustomDomainHttps -InputObject <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a1a2-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2a1a2-107">ByResourceIdParameterSet</span></span>
```
Disable-AzCdnCustomDomainHttps -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a1a2-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="2a1a2-108">DESCRIPTION</span></span>
<span data-ttu-id="2a1a2-109">Polecenie cmdlet **Disable-AzCdnCustomDomainHttps** wyłącza zabezpieczone dostarczanie protokołu HTTPS domeny niestandardowej CDN.</span><span class="sxs-lookup"><span data-stu-id="2a1a2-109">The **Disable-AzCdnCustomDomainHttps** cmdlet disables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="2a1a2-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2a1a2-110">EXAMPLES</span></span>

### <span data-ttu-id="2a1a2-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2a1a2-111">Example 1</span></span>
```powershell
PS C:\> Disable-AzCdnCustomDomainHttps -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -CustomDomainName $customDomainName
```

<span data-ttu-id="2a1a2-112">Wyłącz bezpieczne dostarczanie domeny niestandardowej.</span><span class="sxs-lookup"><span data-stu-id="2a1a2-112">Disable secure delivery of the custom domain.</span></span>

## <span data-ttu-id="2a1a2-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2a1a2-113">PARAMETERS</span></span>

### <span data-ttu-id="2a1a2-114">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="2a1a2-114">-CustomDomainName</span></span>
<span data-ttu-id="2a1a2-115">Nazwa wyświetlana niestandardowej domeny sieci Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="2a1a2-115">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="2a1a2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a1a2-116">-DefaultProfile</span></span>
<span data-ttu-id="2a1a2-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2a1a2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a1a2-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="2a1a2-118">-EndpointName</span></span>
<span data-ttu-id="2a1a2-119">Nazwa punktu końcowego sieci Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="2a1a2-119">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="2a1a2-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2a1a2-120">-InputObject</span></span>
<span data-ttu-id="2a1a2-121">Obiekt domeny niestandardowej.</span><span class="sxs-lookup"><span data-stu-id="2a1a2-121">The custom domain object.</span></span>

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

### <span data-ttu-id="2a1a2-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2a1a2-122">-PassThru</span></span>
<span data-ttu-id="2a1a2-123">Zwracanie obiektu, jeśli jest określony.</span><span class="sxs-lookup"><span data-stu-id="2a1a2-123">Return object if specified.</span></span>

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

### <span data-ttu-id="2a1a2-124">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="2a1a2-124">-ProfileName</span></span>
<span data-ttu-id="2a1a2-125">Nazwa profilu azure CDN.</span><span class="sxs-lookup"><span data-stu-id="2a1a2-125">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="2a1a2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a1a2-126">-ResourceGroupName</span></span>
<span data-ttu-id="2a1a2-127">Grupa zasobów profilu azure CDN</span><span class="sxs-lookup"><span data-stu-id="2a1a2-127">The resource group of the Azure CDN profile</span></span>

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

### <span data-ttu-id="2a1a2-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2a1a2-128">-ResourceId</span></span>
<span data-ttu-id="2a1a2-129">ResourceId domeny niestandardowej</span><span class="sxs-lookup"><span data-stu-id="2a1a2-129">ResourceId of the Custom Domain</span></span>

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

### <span data-ttu-id="2a1a2-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2a1a2-130">-Confirm</span></span>
<span data-ttu-id="2a1a2-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2a1a2-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a1a2-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a1a2-132">-WhatIf</span></span>
<span data-ttu-id="2a1a2-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a1a2-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a1a2-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="2a1a2-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a1a2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a1a2-135">CommonParameters</span></span>
<span data-ttu-id="2a1a2-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a1a2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a1a2-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2a1a2-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a1a2-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2a1a2-138">INPUTS</span></span>

### <span data-ttu-id="2a1a2-139">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="2a1a2-139">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

### <span data-ttu-id="2a1a2-140">System.String</span><span class="sxs-lookup"><span data-stu-id="2a1a2-140">System.String</span></span>

## <span data-ttu-id="2a1a2-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2a1a2-141">OUTPUTS</span></span>

### <span data-ttu-id="2a1a2-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2a1a2-142">System.Boolean</span></span>

## <span data-ttu-id="2a1a2-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2a1a2-143">NOTES</span></span>

## <span data-ttu-id="2a1a2-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2a1a2-144">RELATED LINKS</span></span>
