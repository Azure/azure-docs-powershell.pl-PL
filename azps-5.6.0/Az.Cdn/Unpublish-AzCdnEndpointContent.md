---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 21E9F441-A00B-4F79-8FF1-968D92982471
online version: https://docs.microsoft.com/powershell/module/az.cdn/unpublish-azcdnendpointcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Unpublish-AzCdnEndpointContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Unpublish-AzCdnEndpointContent.md
ms.openlocfilehash: 403c91802c70d7d5e6cfb844909dee1ca6956847
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969633"
---
# <span data-ttu-id="e1690-101">Unpublish-AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="e1690-101">Unpublish-AzCdnEndpointContent</span></span>

## <span data-ttu-id="e1690-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1690-102">SYNOPSIS</span></span>
<span data-ttu-id="e1690-103">Przeczyszcza punkt końcowy sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="e1690-103">Purges a CDN endpoint.</span></span>

## <span data-ttu-id="e1690-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e1690-104">SYNTAX</span></span>

### <span data-ttu-id="e1690-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="e1690-105">ByFieldsParameterSet (Default)</span></span>
```
Unpublish-AzCdnEndpointContent -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -PurgeContent <String[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e1690-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1690-106">ByObjectParameterSet</span></span>
```
Unpublish-AzCdnEndpointContent -CdnEndpoint <PSEndpoint> -PurgeContent <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1690-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="e1690-107">DESCRIPTION</span></span>
<span data-ttu-id="e1690-108">Polecenie **cmdlet Unpublish-AzCdnEndpointContent** czyści zawartość z punktu końcowego usługi Azure Content Delivery Network (CDN).</span><span class="sxs-lookup"><span data-stu-id="e1690-108">The **Unpublish-AzCdnEndpointContent** cmdlet purges the content from an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="e1690-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e1690-109">EXAMPLES</span></span>

## <span data-ttu-id="e1690-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e1690-110">PARAMETERS</span></span>

### <span data-ttu-id="e1690-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e1690-111">-CdnEndpoint</span></span>
<span data-ttu-id="e1690-112">Określa punkt końcowy, który będzie czyszczony przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1690-112">Specifies the endpoint that this cmdlet purges.</span></span>

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

### <span data-ttu-id="e1690-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1690-113">-DefaultProfile</span></span>
<span data-ttu-id="e1690-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="e1690-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e1690-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="e1690-115">-EndpointName</span></span>
<span data-ttu-id="e1690-116">Określa nazwę punktu końcowego, który czyści to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1690-116">Specifies name of the endpoint that this cmdlet purges.</span></span>

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

### <span data-ttu-id="e1690-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e1690-117">-PassThru</span></span>
<span data-ttu-id="e1690-118">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="e1690-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e1690-119">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="e1690-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1690-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="e1690-120">-ProfileName</span></span>
<span data-ttu-id="e1690-121">Określa nazwę profilu, do którego należy punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="e1690-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="e1690-122">- PurgeContent</span><span class="sxs-lookup"><span data-stu-id="e1690-122">-PurgeContent</span></span>
<span data-ttu-id="e1690-123">Określa tablicę ścieżek względnych dla zawartości na serwerze pochodzenia, która jest czyszczona przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1690-123">Specifies an array of relative paths for the content on the origin server that this cmdlet purges.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1690-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1690-124">-ResourceGroupName</span></span>
<span data-ttu-id="e1690-125">Określa nazwę grupy zasobów, do której należy punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="e1690-125">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="e1690-126">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e1690-126">-Confirm</span></span>
<span data-ttu-id="e1690-127">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e1690-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1690-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1690-128">-WhatIf</span></span>
<span data-ttu-id="e1690-129">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1690-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1690-130">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e1690-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1690-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1690-131">CommonParameters</span></span>
<span data-ttu-id="e1690-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1690-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1690-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e1690-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1690-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e1690-134">INPUTS</span></span>

### <span data-ttu-id="e1690-135">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="e1690-135">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="e1690-136">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="e1690-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e1690-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e1690-137">OUTPUTS</span></span>

### <span data-ttu-id="e1690-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e1690-138">System.Boolean</span></span>

## <span data-ttu-id="e1690-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e1690-139">NOTES</span></span>

## <span data-ttu-id="e1690-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e1690-140">RELATED LINKS</span></span>

[<span data-ttu-id="e1690-141">Publish-azCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="e1690-141">Publish-AzCdnEndpointContent</span></span>](./Publish-AzCdnEndpointContent.md)


