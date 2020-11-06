---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 5727E2CA-0A0B-4050-9F4A-7E06758D9B53
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnCustomDomain.md
ms.openlocfilehash: 2aa6b3932424f7a8375cca2584a7fc7916124c54
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550056"
---
# <span data-ttu-id="25ee6-101">Remove-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="25ee6-101">Remove-AzureRmCdnCustomDomain</span></span>

## <span data-ttu-id="25ee6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="25ee6-102">SYNOPSIS</span></span>
<span data-ttu-id="25ee6-103">Usuwa domenę niestandardową.</span><span class="sxs-lookup"><span data-stu-id="25ee6-103">Removes a custom domain.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25ee6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="25ee6-104">SYNTAX</span></span>

### <span data-ttu-id="25ee6-105">Parametr ustawiony dla parametrów pól (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="25ee6-105">Parameter Set for fields parameters (Default)</span></span>
```
Remove-AzureRmCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="25ee6-106">Zestaw parametrów dla parametrów obiektu</span><span class="sxs-lookup"><span data-stu-id="25ee6-106">Parameter Set for object parameters</span></span>
```
Remove-AzureRmCdnCustomDomain -CdnCustomDomain <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25ee6-107">Opis</span><span class="sxs-lookup"><span data-stu-id="25ee6-107">DESCRIPTION</span></span>
<span data-ttu-id="25ee6-108">Polecenie cmdlet **Remove-AzureRmCdnCustomDomain** usuwa domenę niestandardową z punktu końcowego sieci dostarczania zawartości platformy Azure (CDN).</span><span class="sxs-lookup"><span data-stu-id="25ee6-108">The **Remove-AzureRmCdnCustomDomain** cmdlet removes the custom domain from an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="25ee6-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="25ee6-109">EXAMPLES</span></span>

## <span data-ttu-id="25ee6-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="25ee6-110">PARAMETERS</span></span>

### <span data-ttu-id="25ee6-111">-CdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="25ee6-111">-CdnCustomDomain</span></span>
<span data-ttu-id="25ee6-112">Określa domenę niestandardową, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25ee6-112">Specifies the custom domain that this cmdlet removes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain
Parameter Sets: Parameter Set for object parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="25ee6-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="25ee6-113">-CustomDomainName</span></span>
<span data-ttu-id="25ee6-114">Określa nazwę zasobu niestandardowej domeny, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25ee6-114">Specifies the resource name of the custom domain that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25ee6-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="25ee6-115">-EndpointName</span></span>
<span data-ttu-id="25ee6-116">Określa nazwę punktu końcowego, z którego to polecenie cmdlet usuwa domenę niestandardową.</span><span class="sxs-lookup"><span data-stu-id="25ee6-116">Specifies the name of the endpoint from which this cmdlet removes a custom domain.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25ee6-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="25ee6-117">-PassThru</span></span>
<span data-ttu-id="25ee6-118">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="25ee6-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="25ee6-119">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="25ee6-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="25ee6-120">-Refilename</span><span class="sxs-lookup"><span data-stu-id="25ee6-120">-ProfileName</span></span>
<span data-ttu-id="25ee6-121">Określa nazwę profilu, z którego to polecenie cmdlet usuwa domenę niestandardową.</span><span class="sxs-lookup"><span data-stu-id="25ee6-121">Specifies the name of the profile from which this cmdlet removes a custom domain.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25ee6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25ee6-122">-ResourceGroupName</span></span>
<span data-ttu-id="25ee6-123">Określa nazwę grupy zasobów, z której to polecenie cmdlet usuwa domenę niestandardową.</span><span class="sxs-lookup"><span data-stu-id="25ee6-123">Specifies the name of the resource group from which this cmdlet removes a custom domain.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25ee6-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="25ee6-124">-Confirm</span></span>
<span data-ttu-id="25ee6-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25ee6-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25ee6-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25ee6-126">-WhatIf</span></span>
<span data-ttu-id="25ee6-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25ee6-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25ee6-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="25ee6-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25ee6-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25ee6-129">-DefaultProfile</span></span>
<span data-ttu-id="25ee6-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="25ee6-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25ee6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25ee6-131">CommonParameters</span></span>
<span data-ttu-id="25ee6-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25ee6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25ee6-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25ee6-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25ee6-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="25ee6-134">INPUTS</span></span>

### <span data-ttu-id="25ee6-135">PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="25ee6-135">PSCustomDomain</span></span>
<span data-ttu-id="25ee6-136">Parametr "CdnCustomDomain" akceptuje wartość typu "PSCustomDomain" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="25ee6-136">Parameter 'CdnCustomDomain' accepts value of type 'PSCustomDomain' from the pipeline</span></span>

## <span data-ttu-id="25ee6-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="25ee6-137">OUTPUTS</span></span>

### <span data-ttu-id="25ee6-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="25ee6-138">System.Boolean</span></span>

## <span data-ttu-id="25ee6-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="25ee6-139">NOTES</span></span>

## <span data-ttu-id="25ee6-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="25ee6-140">RELATED LINKS</span></span>

[<span data-ttu-id="25ee6-141">Get-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="25ee6-141">Get-AzureRmCdnCustomDomain</span></span>](./Get-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="25ee6-142">Nowe — AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="25ee6-142">New-AzureRmCdnCustomDomain</span></span>](./New-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="25ee6-143">Test — AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="25ee6-143">Test-AzureRmCdnCustomDomain</span></span>](./Test-AzureRmCdnCustomDomain.md)


