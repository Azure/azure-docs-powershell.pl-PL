---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 21E9F441-A00B-4F79-8FF1-968D92982471
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/unpublish-azcdnendpointcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Unpublish-AzCdnEndpointContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Unpublish-AzCdnEndpointContent.md
ms.openlocfilehash: 6a5a0925967895514de8b7e5294c81571b1cbaba
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706523"
---
# <span data-ttu-id="48984-101">Unpublish-AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="48984-101">Unpublish-AzCdnEndpointContent</span></span>

## <span data-ttu-id="48984-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="48984-102">SYNOPSIS</span></span>
<span data-ttu-id="48984-103">Przeczyszcza punkt końcowy sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="48984-103">Purges a CDN endpoint.</span></span>

## <span data-ttu-id="48984-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="48984-104">SYNTAX</span></span>

### <span data-ttu-id="48984-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="48984-105">ByFieldsParameterSet (Default)</span></span>
```
Unpublish-AzCdnEndpointContent -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -PurgeContent <String[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="48984-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="48984-106">ByObjectParameterSet</span></span>
```
Unpublish-AzCdnEndpointContent -CdnEndpoint <PSEndpoint> -PurgeContent <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48984-107">Opis</span><span class="sxs-lookup"><span data-stu-id="48984-107">DESCRIPTION</span></span>
<span data-ttu-id="48984-108">Polecenie cmdlet **cofnięcia publikowania — AzCdnEndpointContent** Przeczyszcza zawartość z punktu końcowego sieci dostarczania zawartości Azure (CDN).</span><span class="sxs-lookup"><span data-stu-id="48984-108">The **Unpublish-AzCdnEndpointContent** cmdlet purges the content from an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="48984-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="48984-109">EXAMPLES</span></span>

## <span data-ttu-id="48984-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="48984-110">PARAMETERS</span></span>

### <span data-ttu-id="48984-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="48984-111">-CdnEndpoint</span></span>
<span data-ttu-id="48984-112">Określa punkt końcowy, który to polecenie cmdlet Przeczyszcza.</span><span class="sxs-lookup"><span data-stu-id="48984-112">Specifies the endpoint that this cmdlet purges.</span></span>

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

### <span data-ttu-id="48984-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48984-113">-DefaultProfile</span></span>
<span data-ttu-id="48984-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="48984-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="48984-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="48984-115">-EndpointName</span></span>
<span data-ttu-id="48984-116">Określa nazwę punktu końcowego, który jest czyszczony przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48984-116">Specifies name of the endpoint that this cmdlet purges.</span></span>

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

### <span data-ttu-id="48984-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="48984-117">-PassThru</span></span>
<span data-ttu-id="48984-118">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="48984-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="48984-119">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="48984-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="48984-120">-Refilename</span><span class="sxs-lookup"><span data-stu-id="48984-120">-ProfileName</span></span>
<span data-ttu-id="48984-121">Określa nazwę profilu, do którego należy punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="48984-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="48984-122">-PurgeContent</span><span class="sxs-lookup"><span data-stu-id="48984-122">-PurgeContent</span></span>
<span data-ttu-id="48984-123">Określa tablicę względnych ścieżek dla zawartości na serwerze pochodzenia, którą to polecenie cmdlet Przeczyszcza.</span><span class="sxs-lookup"><span data-stu-id="48984-123">Specifies an array of relative paths for the content on the origin server that this cmdlet purges.</span></span>

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

### <span data-ttu-id="48984-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48984-124">-ResourceGroupName</span></span>
<span data-ttu-id="48984-125">Określa nazwę grupy zasobów, do której należy punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="48984-125">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="48984-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="48984-126">-Confirm</span></span>
<span data-ttu-id="48984-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48984-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48984-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48984-128">-WhatIf</span></span>
<span data-ttu-id="48984-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48984-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48984-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="48984-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48984-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48984-131">CommonParameters</span></span>
<span data-ttu-id="48984-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48984-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48984-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="48984-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48984-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="48984-134">INPUTS</span></span>

### <span data-ttu-id="48984-135">Microsoft. Azure. Commands. CDN. models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="48984-135">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="48984-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="48984-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="48984-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="48984-137">OUTPUTS</span></span>

### <span data-ttu-id="48984-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="48984-138">System.Boolean</span></span>

## <span data-ttu-id="48984-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="48984-139">NOTES</span></span>

## <span data-ttu-id="48984-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="48984-140">RELATED LINKS</span></span>

[<span data-ttu-id="48984-141">Publikowanie — AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="48984-141">Publish-AzCdnEndpointContent</span></span>](./Publish-AzCdnEndpointContent.md)


