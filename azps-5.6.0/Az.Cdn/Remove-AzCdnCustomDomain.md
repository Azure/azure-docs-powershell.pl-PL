---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 5727E2CA-0A0B-4050-9F4A-7E06758D9B53
online version: https://docs.microsoft.com/powershell/module/az.cdn/remove-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnCustomDomain.md
ms.openlocfilehash: c76e8d9da78fed592f506ba9aca39b68d4d119c6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975562"
---
# <span data-ttu-id="0f163-101">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="0f163-101">Remove-AzCdnCustomDomain</span></span>

## <span data-ttu-id="0f163-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f163-102">SYNOPSIS</span></span>
<span data-ttu-id="0f163-103">Usuwa domenę niestandardową.</span><span class="sxs-lookup"><span data-stu-id="0f163-103">Removes a custom domain.</span></span>

## <span data-ttu-id="0f163-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0f163-104">SYNTAX</span></span>

### <span data-ttu-id="0f163-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="0f163-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0f163-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f163-106">ByObjectParameterSet</span></span>
```
Remove-AzCdnCustomDomain -CdnCustomDomain <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f163-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="0f163-107">DESCRIPTION</span></span>
<span data-ttu-id="0f163-108">Polecenie **cmdlet Remove-AzCdnCustomDomain** usuwa domenę niestandardową z punktu końcowego usługi Azure Content Delivery Network (CDN).</span><span class="sxs-lookup"><span data-stu-id="0f163-108">The **Remove-AzCdnCustomDomain** cmdlet removes the custom domain from an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="0f163-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0f163-109">EXAMPLES</span></span>

## <span data-ttu-id="0f163-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0f163-110">PARAMETERS</span></span>

### <span data-ttu-id="0f163-111">-CdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="0f163-111">-CdnCustomDomain</span></span>
<span data-ttu-id="0f163-112">Określa domenę niestandardową usuwaną przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f163-112">Specifies the custom domain that this cmdlet removes.</span></span>

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

### <span data-ttu-id="0f163-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="0f163-113">-CustomDomainName</span></span>
<span data-ttu-id="0f163-114">Określa nazwę zasobu domeny niestandardowej, która jest usuwana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f163-114">Specifies the resource name of the custom domain that this cmdlet removes.</span></span>

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

### <span data-ttu-id="0f163-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f163-115">-DefaultProfile</span></span>
<span data-ttu-id="0f163-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="0f163-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0f163-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="0f163-117">-EndpointName</span></span>
<span data-ttu-id="0f163-118">Określa nazwę punktu końcowego, z którego to polecenie cmdlet usuwa domenę niestandardową.</span><span class="sxs-lookup"><span data-stu-id="0f163-118">Specifies the name of the endpoint from which this cmdlet removes a custom domain.</span></span>

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

### <span data-ttu-id="0f163-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0f163-119">-PassThru</span></span>
<span data-ttu-id="0f163-120">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="0f163-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0f163-121">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="0f163-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0f163-122">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="0f163-122">-ProfileName</span></span>
<span data-ttu-id="0f163-123">Określa nazwę profilu, z którego to polecenie cmdlet usuwa domenę niestandardową.</span><span class="sxs-lookup"><span data-stu-id="0f163-123">Specifies the name of the profile from which this cmdlet removes a custom domain.</span></span>

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

### <span data-ttu-id="0f163-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f163-124">-ResourceGroupName</span></span>
<span data-ttu-id="0f163-125">Określa nazwę grupy zasobów, z której to polecenie cmdlet usuwa domenę niestandardową.</span><span class="sxs-lookup"><span data-stu-id="0f163-125">Specifies the name of the resource group from which this cmdlet removes a custom domain.</span></span>

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

### <span data-ttu-id="0f163-126">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0f163-126">-Confirm</span></span>
<span data-ttu-id="0f163-127">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0f163-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f163-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f163-128">-WhatIf</span></span>
<span data-ttu-id="0f163-129">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f163-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f163-130">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="0f163-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f163-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f163-131">CommonParameters</span></span>
<span data-ttu-id="0f163-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f163-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f163-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0f163-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f163-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0f163-134">INPUTS</span></span>

### <span data-ttu-id="0f163-135">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="0f163-135">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

### <span data-ttu-id="0f163-136">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="0f163-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0f163-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0f163-137">OUTPUTS</span></span>

### <span data-ttu-id="0f163-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0f163-138">System.Boolean</span></span>

## <span data-ttu-id="0f163-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0f163-139">NOTES</span></span>

## <span data-ttu-id="0f163-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0f163-140">RELATED LINKS</span></span>

[<span data-ttu-id="0f163-141">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="0f163-141">Get-AzCdnCustomDomain</span></span>](./Get-AzCdnCustomDomain.md)

[<span data-ttu-id="0f163-142">New-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="0f163-142">New-AzCdnCustomDomain</span></span>](./New-AzCdnCustomDomain.md)

[<span data-ttu-id="0f163-143">Test-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="0f163-143">Test-AzCdnCustomDomain</span></span>](./Test-AzCdnCustomDomain.md)


