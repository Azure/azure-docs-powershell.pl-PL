---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/enable-azcdncustomdomainhttps
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Enable-AzCdnCustomDomainHttps.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Enable-AzCdnCustomDomainHttps.md
ms.openlocfilehash: cb11377c4ee18278dee2a3dc97c16bb58a02f5d5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181875"
---
# <span data-ttu-id="3fc2a-101">Enable-AzCdnCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="3fc2a-101">Enable-AzCdnCustomDomainHttps</span></span>

## <span data-ttu-id="3fc2a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3fc2a-102">SYNOPSIS</span></span>
<span data-ttu-id="3fc2a-103">Umożliwia włączenie niestandardowego protokołu HTTPS.</span><span class="sxs-lookup"><span data-stu-id="3fc2a-103">Enables custom HTTPS.</span></span>

## <span data-ttu-id="3fc2a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3fc2a-104">SYNTAX</span></span>

### <span data-ttu-id="3fc2a-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="3fc2a-105">ByFieldsParameterSet (Default)</span></span>
```
Enable-AzCdnCustomDomainHttps -ResourceGroupName <String> -ProfileName <String> -EndpointName <String>
 -CustomDomainName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3fc2a-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3fc2a-106">ByObjectParameterSet</span></span>
```
Enable-AzCdnCustomDomainHttps -InputObject <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3fc2a-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3fc2a-107">ByResourceIdParameterSet</span></span>
```
Enable-AzCdnCustomDomainHttps -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3fc2a-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="3fc2a-108">DESCRIPTION</span></span>
<span data-ttu-id="3fc2a-109">Polecenie **cmdlet Enable-AzCdnCustomDomainHttps** umożliwia dostarczenie zabezpieczonego protokołu HTTPS domeny niestandardowej CDN.</span><span class="sxs-lookup"><span data-stu-id="3fc2a-109">The **Enable-AzCdnCustomDomainHttps** cmdlet enables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="3fc2a-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3fc2a-110">EXAMPLES</span></span>

### <span data-ttu-id="3fc2a-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3fc2a-111">Example 1</span></span>
```powershell
PS C:\> Enable-AzCdnCustomDomainHttps -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -CustomDomainName $customDomainName
```

<span data-ttu-id="3fc2a-112">Włączanie bezpiecznego dostarczania domeny niestandardowej.</span><span class="sxs-lookup"><span data-stu-id="3fc2a-112">Enable secure delivery of the custom domain.</span></span>

## <span data-ttu-id="3fc2a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3fc2a-113">PARAMETERS</span></span>

### <span data-ttu-id="3fc2a-114">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="3fc2a-114">-CustomDomainName</span></span>
<span data-ttu-id="3fc2a-115">Nazwa wyświetlana niestandardowej domeny sieci Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="3fc2a-115">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="3fc2a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fc2a-116">-DefaultProfile</span></span>
<span data-ttu-id="3fc2a-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3fc2a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3fc2a-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="3fc2a-118">-EndpointName</span></span>
<span data-ttu-id="3fc2a-119">Nazwa punktu końcowego sieci Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="3fc2a-119">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="3fc2a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3fc2a-120">-InputObject</span></span>
<span data-ttu-id="3fc2a-121">Obiekt domeny niestandardowej.</span><span class="sxs-lookup"><span data-stu-id="3fc2a-121">The custom domain object.</span></span>

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

### <span data-ttu-id="3fc2a-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3fc2a-122">-PassThru</span></span>
<span data-ttu-id="3fc2a-123">Zwracanie obiektu, jeśli jest określony.</span><span class="sxs-lookup"><span data-stu-id="3fc2a-123">Return object if specified.</span></span>

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

### <span data-ttu-id="3fc2a-124">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="3fc2a-124">-ProfileName</span></span>
<span data-ttu-id="3fc2a-125">Nazwa profilu azure CDN.</span><span class="sxs-lookup"><span data-stu-id="3fc2a-125">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="3fc2a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fc2a-126">-ResourceGroupName</span></span>
<span data-ttu-id="3fc2a-127">Grupa zasobów profilu azure CDN</span><span class="sxs-lookup"><span data-stu-id="3fc2a-127">The resource group of the Azure CDN profile</span></span>

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

### <span data-ttu-id="3fc2a-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3fc2a-128">-ResourceId</span></span>
<span data-ttu-id="3fc2a-129">ResourceId domeny niestandardowej</span><span class="sxs-lookup"><span data-stu-id="3fc2a-129">ResourceId of the Custom Domain</span></span>

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

### <span data-ttu-id="3fc2a-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3fc2a-130">-Confirm</span></span>
<span data-ttu-id="3fc2a-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3fc2a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3fc2a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3fc2a-132">-WhatIf</span></span>
<span data-ttu-id="3fc2a-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3fc2a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3fc2a-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="3fc2a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3fc2a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fc2a-135">CommonParameters</span></span>
<span data-ttu-id="3fc2a-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3fc2a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fc2a-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3fc2a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fc2a-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3fc2a-138">INPUTS</span></span>

### <span data-ttu-id="3fc2a-139">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="3fc2a-139">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

### <span data-ttu-id="3fc2a-140">System.String</span><span class="sxs-lookup"><span data-stu-id="3fc2a-140">System.String</span></span>

## <span data-ttu-id="3fc2a-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3fc2a-141">OUTPUTS</span></span>

### <span data-ttu-id="3fc2a-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3fc2a-142">System.Boolean</span></span>

## <span data-ttu-id="3fc2a-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3fc2a-143">NOTES</span></span>

## <span data-ttu-id="3fc2a-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3fc2a-144">RELATED LINKS</span></span>
