---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 7060D3D7-B397-447E-88E3-B6F0D094770D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnCustomDomain.md
ms.openlocfilehash: ec15b97aa87c5e581069606a425f25b71dd495dd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717873"
---
# <span data-ttu-id="bd039-101">New-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="bd039-101">New-AzureRmCdnCustomDomain</span></span>

## <span data-ttu-id="bd039-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bd039-102">SYNOPSIS</span></span>
<span data-ttu-id="bd039-103">Tworzy domenę niestandardową dla punktu końcowego sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="bd039-103">Creates a custom domain for a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bd039-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bd039-104">SYNTAX</span></span>

### <span data-ttu-id="bd039-105">Parametr ustawiony dla parametrów pól (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="bd039-105">Parameter Set for fields parameters (Default)</span></span>
```
New-AzureRmCdnCustomDomain -HostName <String> -CustomDomainName <String> -EndpointName <String>
 -ProfileName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd039-106">Zestaw parametrów dla parametrów obiektu</span><span class="sxs-lookup"><span data-stu-id="bd039-106">Parameter Set for object parameters</span></span>
```
New-AzureRmCdnCustomDomain -HostName <String> -CustomDomainName <String> -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd039-107">Opis</span><span class="sxs-lookup"><span data-stu-id="bd039-107">DESCRIPTION</span></span>
<span data-ttu-id="bd039-108">Polecenie cmdlet **New-AzureRmCdnCustomDomain** tworzy domenę niestandardową dla punktu końcowego sieci dostarczania zawartości Azure (CDN).</span><span class="sxs-lookup"><span data-stu-id="bd039-108">The **New-AzureRmCdnCustomDomain** cmdlet creates a custom domain for the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="bd039-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bd039-109">EXAMPLES</span></span>

## <span data-ttu-id="bd039-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bd039-110">PARAMETERS</span></span>

### <span data-ttu-id="bd039-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="bd039-111">-CdnEndpoint</span></span>
<span data-ttu-id="bd039-112">Określa obiekt punktu końcowego sieci CDN, do którego jest dodawana domena niestandardowa.</span><span class="sxs-lookup"><span data-stu-id="bd039-112">Specifies the CDN endpoint object to which the custom domain is added.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: Parameter Set for object parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bd039-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="bd039-113">-CustomDomainName</span></span>
<span data-ttu-id="bd039-114">Określa nazwę zasobu domeny niestandardowej.</span><span class="sxs-lookup"><span data-stu-id="bd039-114">Specifies the resource name of the custom domain.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd039-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="bd039-115">-EndpointName</span></span>
<span data-ttu-id="bd039-116">Określa nazwę punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="bd039-116">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="bd039-117">-HostName</span><span class="sxs-lookup"><span data-stu-id="bd039-117">-HostName</span></span>
<span data-ttu-id="bd039-118">Określa nazwę hosta domeny niestandardowej.</span><span class="sxs-lookup"><span data-stu-id="bd039-118">Specifies the host name of the custom domain.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd039-119">-Refilename</span><span class="sxs-lookup"><span data-stu-id="bd039-119">-ProfileName</span></span>
<span data-ttu-id="bd039-120">Określa nazwę profilu.</span><span class="sxs-lookup"><span data-stu-id="bd039-120">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="bd039-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd039-121">-ResourceGroupName</span></span>
<span data-ttu-id="bd039-122">Określa nazwę grupy zasobów, do której należy domena niestandardowa.</span><span class="sxs-lookup"><span data-stu-id="bd039-122">Specifies the name of the resource group to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="bd039-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bd039-123">-Confirm</span></span>
<span data-ttu-id="bd039-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd039-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd039-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd039-125">-WhatIf</span></span>
<span data-ttu-id="bd039-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd039-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd039-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bd039-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd039-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd039-128">-DefaultProfile</span></span>
<span data-ttu-id="bd039-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bd039-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd039-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd039-130">CommonParameters</span></span>
<span data-ttu-id="bd039-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd039-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd039-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd039-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd039-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bd039-133">INPUTS</span></span>

### <span data-ttu-id="bd039-134">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="bd039-134">PSEndpoint</span></span>
<span data-ttu-id="bd039-135">Parametr "CdnEndpoint" akceptuje wartość typu "PSEndpoint" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="bd039-135">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="bd039-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bd039-136">OUTPUTS</span></span>

### <span data-ttu-id="bd039-137">Microsoft. Azure. Commands. CDN. models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="bd039-137">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="bd039-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bd039-138">NOTES</span></span>

## <span data-ttu-id="bd039-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bd039-139">RELATED LINKS</span></span>

[<span data-ttu-id="bd039-140">Get-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="bd039-140">Get-AzureRmCdnCustomDomain</span></span>](./Get-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="bd039-141">Remove-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="bd039-141">Remove-AzureRmCdnCustomDomain</span></span>](./Remove-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="bd039-142">Test — AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="bd039-142">Test-AzureRmCdnCustomDomain</span></span>](./Test-AzureRmCdnCustomDomain.md)


