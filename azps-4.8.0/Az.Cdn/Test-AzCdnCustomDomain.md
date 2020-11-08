---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 8C4E824F-FB4A-4DE7-8FD9-3FDA3848F25C
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/test-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Test-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Test-AzCdnCustomDomain.md
ms.openlocfilehash: 8ceb1fe02ba4a7d5cf4435ac79d404b331b58ea9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94221857"
---
# <span data-ttu-id="3751b-101">Test-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="3751b-101">Test-AzCdnCustomDomain</span></span>

## <span data-ttu-id="3751b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3751b-102">SYNOPSIS</span></span>
<span data-ttu-id="3751b-103">Sprawdza, czy do punktu końcowego można dodać domenę niestandardową.</span><span class="sxs-lookup"><span data-stu-id="3751b-103">Checks whether a custom domain can be added to an endpoint.</span></span>

## <span data-ttu-id="3751b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3751b-104">SYNTAX</span></span>

### <span data-ttu-id="3751b-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3751b-105">ByFieldsParameterSet (Default)</span></span>
```
Test-AzCdnCustomDomain -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -CustomDomainHostName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3751b-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3751b-106">ByObjectParameterSet</span></span>
```
Test-AzCdnCustomDomain -CdnEndpoint <PSEndpoint> -CustomDomainHostName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3751b-107">Opis</span><span class="sxs-lookup"><span data-stu-id="3751b-107">DESCRIPTION</span></span>
<span data-ttu-id="3751b-108">Polecenie cmdlet **test-AzCdnCustomDomain** sprawdza, czy można dodać domenę niestandardową do punktu końcowego, sprawdzając poprawność mapowania CNAME.</span><span class="sxs-lookup"><span data-stu-id="3751b-108">The **Test-AzCdnCustomDomain** cmdlet checks whether a custom domain can be added to an endpoint by validating the CName mapping.</span></span>

## <span data-ttu-id="3751b-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3751b-109">EXAMPLES</span></span>

## <span data-ttu-id="3751b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3751b-110">PARAMETERS</span></span>

### <span data-ttu-id="3751b-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="3751b-111">-CdnEndpoint</span></span>
<span data-ttu-id="3751b-112">Określa punkt końcowy, do którego ma zostać dodana domena niestandardowa.</span><span class="sxs-lookup"><span data-stu-id="3751b-112">Specifies the endpoint to which you want to add the custom domain.</span></span>

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

### <span data-ttu-id="3751b-113">-CustomDomainHostName</span><span class="sxs-lookup"><span data-stu-id="3751b-113">-CustomDomainHostName</span></span>
<span data-ttu-id="3751b-114">Określa nazwę hosta domeny niestandardowej.</span><span class="sxs-lookup"><span data-stu-id="3751b-114">Specifies the host name of the custom domain.</span></span>

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

### <span data-ttu-id="3751b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3751b-115">-DefaultProfile</span></span>
<span data-ttu-id="3751b-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="3751b-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3751b-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="3751b-117">-EndpointName</span></span>
<span data-ttu-id="3751b-118">Określa nazwę punktu końcowego, do którego chcesz dodać domenę niestandardową.</span><span class="sxs-lookup"><span data-stu-id="3751b-118">Specifies the name of the endpoint to which you want to add the custom domain.</span></span>

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

### <span data-ttu-id="3751b-119">-Refilename</span><span class="sxs-lookup"><span data-stu-id="3751b-119">-ProfileName</span></span>
<span data-ttu-id="3751b-120">Określa nazwę profilu.</span><span class="sxs-lookup"><span data-stu-id="3751b-120">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="3751b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3751b-121">-ResourceGroupName</span></span>
<span data-ttu-id="3751b-122">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3751b-122">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="3751b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3751b-123">CommonParameters</span></span>
<span data-ttu-id="3751b-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3751b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3751b-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3751b-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3751b-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3751b-126">INPUTS</span></span>

### <span data-ttu-id="3751b-127">Microsoft. Azure. Commands. CDN. models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="3751b-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="3751b-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3751b-128">OUTPUTS</span></span>

### <span data-ttu-id="3751b-129">Microsoft. Azure. Commands. CDN. models. Endpoint. PSValidateCustomDomainOutput</span><span class="sxs-lookup"><span data-stu-id="3751b-129">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateCustomDomainOutput</span></span>

## <span data-ttu-id="3751b-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3751b-130">NOTES</span></span>

## <span data-ttu-id="3751b-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3751b-131">RELATED LINKS</span></span>

[<span data-ttu-id="3751b-132">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="3751b-132">Get-AzCdnCustomDomain</span></span>](./Get-AzCdnCustomDomain.md)

[<span data-ttu-id="3751b-133">Nowe — AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="3751b-133">New-AzCdnCustomDomain</span></span>](./New-AzCdnCustomDomain.md)

[<span data-ttu-id="3751b-134">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="3751b-134">Remove-AzCdnCustomDomain</span></span>](./Remove-AzCdnCustomDomain.md)


