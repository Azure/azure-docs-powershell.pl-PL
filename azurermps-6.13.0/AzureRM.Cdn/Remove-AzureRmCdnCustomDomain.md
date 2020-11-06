---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 5727E2CA-0A0B-4050-9F4A-7E06758D9B53
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/remove-azurermcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnCustomDomain.md
ms.openlocfilehash: fa0e3682d62f01d7d305d190c6765aab709bed15
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547528"
---
# <span data-ttu-id="97444-101">Remove-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="97444-101">Remove-AzureRmCdnCustomDomain</span></span>

## <span data-ttu-id="97444-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="97444-102">SYNOPSIS</span></span>
<span data-ttu-id="97444-103">Usuwa domenę niestandardową.</span><span class="sxs-lookup"><span data-stu-id="97444-103">Removes a custom domain.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97444-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="97444-104">SYNTAX</span></span>

### <span data-ttu-id="97444-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="97444-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzureRmCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="97444-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="97444-106">ByObjectParameterSet</span></span>
```
Remove-AzureRmCdnCustomDomain -CdnCustomDomain <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97444-107">Opis</span><span class="sxs-lookup"><span data-stu-id="97444-107">DESCRIPTION</span></span>
<span data-ttu-id="97444-108">Polecenie cmdlet **Remove-AzureRmCdnCustomDomain** usuwa domenę niestandardową z punktu końcowego sieci dostarczania zawartości platformy Azure (CDN).</span><span class="sxs-lookup"><span data-stu-id="97444-108">The **Remove-AzureRmCdnCustomDomain** cmdlet removes the custom domain from an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="97444-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="97444-109">EXAMPLES</span></span>

## <span data-ttu-id="97444-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="97444-110">PARAMETERS</span></span>

### <span data-ttu-id="97444-111">-CdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="97444-111">-CdnCustomDomain</span></span>
<span data-ttu-id="97444-112">Określa domenę niestandardową, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97444-112">Specifies the custom domain that this cmdlet removes.</span></span>

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

### <span data-ttu-id="97444-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="97444-113">-CustomDomainName</span></span>
<span data-ttu-id="97444-114">Określa nazwę zasobu niestandardowej domeny, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97444-114">Specifies the resource name of the custom domain that this cmdlet removes.</span></span>

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

### <span data-ttu-id="97444-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97444-115">-DefaultProfile</span></span>
<span data-ttu-id="97444-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="97444-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97444-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="97444-117">-EndpointName</span></span>
<span data-ttu-id="97444-118">Określa nazwę punktu końcowego, z którego to polecenie cmdlet usuwa domenę niestandardową.</span><span class="sxs-lookup"><span data-stu-id="97444-118">Specifies the name of the endpoint from which this cmdlet removes a custom domain.</span></span>

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

### <span data-ttu-id="97444-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="97444-119">-PassThru</span></span>
<span data-ttu-id="97444-120">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="97444-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="97444-121">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="97444-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="97444-122">-Refilename</span><span class="sxs-lookup"><span data-stu-id="97444-122">-ProfileName</span></span>
<span data-ttu-id="97444-123">Określa nazwę profilu, z którego to polecenie cmdlet usuwa domenę niestandardową.</span><span class="sxs-lookup"><span data-stu-id="97444-123">Specifies the name of the profile from which this cmdlet removes a custom domain.</span></span>

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

### <span data-ttu-id="97444-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97444-124">-ResourceGroupName</span></span>
<span data-ttu-id="97444-125">Określa nazwę grupy zasobów, z której to polecenie cmdlet usuwa domenę niestandardową.</span><span class="sxs-lookup"><span data-stu-id="97444-125">Specifies the name of the resource group from which this cmdlet removes a custom domain.</span></span>

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

### <span data-ttu-id="97444-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="97444-126">-Confirm</span></span>
<span data-ttu-id="97444-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97444-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97444-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97444-128">-WhatIf</span></span>
<span data-ttu-id="97444-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97444-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97444-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="97444-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97444-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97444-131">CommonParameters</span></span>
<span data-ttu-id="97444-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97444-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97444-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97444-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97444-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="97444-134">INPUTS</span></span>

### <span data-ttu-id="97444-135">Microsoft. Azure. Commands. CDN. models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="97444-135">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>
<span data-ttu-id="97444-136">Parametry: CdnCustomDomain (ByValue)</span><span class="sxs-lookup"><span data-stu-id="97444-136">Parameters: CdnCustomDomain (ByValue)</span></span>

### <span data-ttu-id="97444-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="97444-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="97444-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="97444-138">OUTPUTS</span></span>

### <span data-ttu-id="97444-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="97444-139">System.Boolean</span></span>

## <span data-ttu-id="97444-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="97444-140">NOTES</span></span>

## <span data-ttu-id="97444-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="97444-141">RELATED LINKS</span></span>

[<span data-ttu-id="97444-142">Get-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="97444-142">Get-AzureRmCdnCustomDomain</span></span>](./Get-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="97444-143">Nowe — AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="97444-143">New-AzureRmCdnCustomDomain</span></span>](./New-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="97444-144">Test — AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="97444-144">Test-AzureRmCdnCustomDomain</span></span>](./Test-AzureRmCdnCustomDomain.md)


