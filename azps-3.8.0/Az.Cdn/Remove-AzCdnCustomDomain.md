---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 5727E2CA-0A0B-4050-9F4A-7E06758D9B53
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/remove-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnCustomDomain.md
ms.openlocfilehash: 0645b3f5286526ba72db35fd8b9e048c895f4108
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94049298"
---
# <span data-ttu-id="3b731-101">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="3b731-101">Remove-AzCdnCustomDomain</span></span>

## <span data-ttu-id="3b731-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3b731-102">SYNOPSIS</span></span>
<span data-ttu-id="3b731-103">Usuwa domenę niestandardową.</span><span class="sxs-lookup"><span data-stu-id="3b731-103">Removes a custom domain.</span></span>

## <span data-ttu-id="3b731-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3b731-104">SYNTAX</span></span>

### <span data-ttu-id="3b731-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3b731-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3b731-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b731-106">ByObjectParameterSet</span></span>
```
Remove-AzCdnCustomDomain -CdnCustomDomain <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b731-107">Opis</span><span class="sxs-lookup"><span data-stu-id="3b731-107">DESCRIPTION</span></span>
<span data-ttu-id="3b731-108">Polecenie cmdlet **Remove-AzCdnCustomDomain** usuwa domenę niestandardową z punktu końcowego sieci dostarczania zawartości platformy Azure (CDN).</span><span class="sxs-lookup"><span data-stu-id="3b731-108">The **Remove-AzCdnCustomDomain** cmdlet removes the custom domain from an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="3b731-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3b731-109">EXAMPLES</span></span>

## <span data-ttu-id="3b731-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3b731-110">PARAMETERS</span></span>

### <span data-ttu-id="3b731-111">-CdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="3b731-111">-CdnCustomDomain</span></span>
<span data-ttu-id="3b731-112">Określa domenę niestandardową, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b731-112">Specifies the custom domain that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3b731-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="3b731-113">-CustomDomainName</span></span>
<span data-ttu-id="3b731-114">Określa nazwę zasobu niestandardowej domeny, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b731-114">Specifies the resource name of the custom domain that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3b731-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b731-115">-DefaultProfile</span></span>
<span data-ttu-id="3b731-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="3b731-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3b731-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="3b731-117">-EndpointName</span></span>
<span data-ttu-id="3b731-118">Określa nazwę punktu końcowego, z którego to polecenie cmdlet usuwa domenę niestandardową.</span><span class="sxs-lookup"><span data-stu-id="3b731-118">Specifies the name of the endpoint from which this cmdlet removes a custom domain.</span></span>

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

### <span data-ttu-id="3b731-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3b731-119">-PassThru</span></span>
<span data-ttu-id="3b731-120">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="3b731-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3b731-121">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="3b731-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3b731-122">-Refilename</span><span class="sxs-lookup"><span data-stu-id="3b731-122">-ProfileName</span></span>
<span data-ttu-id="3b731-123">Określa nazwę profilu, z którego to polecenie cmdlet usuwa domenę niestandardową.</span><span class="sxs-lookup"><span data-stu-id="3b731-123">Specifies the name of the profile from which this cmdlet removes a custom domain.</span></span>

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

### <span data-ttu-id="3b731-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b731-124">-ResourceGroupName</span></span>
<span data-ttu-id="3b731-125">Określa nazwę grupy zasobów, z której to polecenie cmdlet usuwa domenę niestandardową.</span><span class="sxs-lookup"><span data-stu-id="3b731-125">Specifies the name of the resource group from which this cmdlet removes a custom domain.</span></span>

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

### <span data-ttu-id="3b731-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3b731-126">-Confirm</span></span>
<span data-ttu-id="3b731-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b731-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b731-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b731-128">-WhatIf</span></span>
<span data-ttu-id="3b731-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b731-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b731-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3b731-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b731-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b731-131">CommonParameters</span></span>
<span data-ttu-id="3b731-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b731-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b731-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3b731-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b731-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3b731-134">INPUTS</span></span>

### <span data-ttu-id="3b731-135">Microsoft. Azure. Commands. CDN. models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="3b731-135">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

### <span data-ttu-id="3b731-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3b731-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3b731-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3b731-137">OUTPUTS</span></span>

### <span data-ttu-id="3b731-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3b731-138">System.Boolean</span></span>

## <span data-ttu-id="3b731-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3b731-139">NOTES</span></span>

## <span data-ttu-id="3b731-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3b731-140">RELATED LINKS</span></span>

[<span data-ttu-id="3b731-141">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="3b731-141">Get-AzCdnCustomDomain</span></span>](./Get-AzCdnCustomDomain.md)

[<span data-ttu-id="3b731-142">Nowe — AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="3b731-142">New-AzCdnCustomDomain</span></span>](./New-AzCdnCustomDomain.md)

[<span data-ttu-id="3b731-143">Test — AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="3b731-143">Test-AzCdnCustomDomain</span></span>](./Test-AzCdnCustomDomain.md)


