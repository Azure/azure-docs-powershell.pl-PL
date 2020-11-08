---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 8C4E824F-FB4A-4DE7-8FD9-3FDA3848F25C
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/test-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Test-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Test-AzCdnCustomDomain.md
ms.openlocfilehash: 8ceb1fe02ba4a7d5cf4435ac79d404b331b58ea9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94233680"
---
# <span data-ttu-id="822fb-101">Test-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="822fb-101">Test-AzCdnCustomDomain</span></span>

## <span data-ttu-id="822fb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="822fb-102">SYNOPSIS</span></span>
<span data-ttu-id="822fb-103">Sprawdza, czy do punktu końcowego można dodać domenę niestandardową.</span><span class="sxs-lookup"><span data-stu-id="822fb-103">Checks whether a custom domain can be added to an endpoint.</span></span>

## <span data-ttu-id="822fb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="822fb-104">SYNTAX</span></span>

### <span data-ttu-id="822fb-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="822fb-105">ByFieldsParameterSet (Default)</span></span>
```
Test-AzCdnCustomDomain -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -CustomDomainHostName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="822fb-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="822fb-106">ByObjectParameterSet</span></span>
```
Test-AzCdnCustomDomain -CdnEndpoint <PSEndpoint> -CustomDomainHostName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="822fb-107">Opis</span><span class="sxs-lookup"><span data-stu-id="822fb-107">DESCRIPTION</span></span>
<span data-ttu-id="822fb-108">Polecenie cmdlet **test-AzCdnCustomDomain** sprawdza, czy można dodać domenę niestandardową do punktu końcowego, sprawdzając poprawność mapowania CNAME.</span><span class="sxs-lookup"><span data-stu-id="822fb-108">The **Test-AzCdnCustomDomain** cmdlet checks whether a custom domain can be added to an endpoint by validating the CName mapping.</span></span>

## <span data-ttu-id="822fb-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="822fb-109">EXAMPLES</span></span>

## <span data-ttu-id="822fb-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="822fb-110">PARAMETERS</span></span>

### <span data-ttu-id="822fb-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="822fb-111">-CdnEndpoint</span></span>
<span data-ttu-id="822fb-112">Określa punkt końcowy, do którego ma zostać dodana domena niestandardowa.</span><span class="sxs-lookup"><span data-stu-id="822fb-112">Specifies the endpoint to which you want to add the custom domain.</span></span>

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

### <span data-ttu-id="822fb-113">-CustomDomainHostName</span><span class="sxs-lookup"><span data-stu-id="822fb-113">-CustomDomainHostName</span></span>
<span data-ttu-id="822fb-114">Określa nazwę hosta domeny niestandardowej.</span><span class="sxs-lookup"><span data-stu-id="822fb-114">Specifies the host name of the custom domain.</span></span>

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

### <span data-ttu-id="822fb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="822fb-115">-DefaultProfile</span></span>
<span data-ttu-id="822fb-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="822fb-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="822fb-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="822fb-117">-EndpointName</span></span>
<span data-ttu-id="822fb-118">Określa nazwę punktu końcowego, do którego chcesz dodać domenę niestandardową.</span><span class="sxs-lookup"><span data-stu-id="822fb-118">Specifies the name of the endpoint to which you want to add the custom domain.</span></span>

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

### <span data-ttu-id="822fb-119">-Refilename</span><span class="sxs-lookup"><span data-stu-id="822fb-119">-ProfileName</span></span>
<span data-ttu-id="822fb-120">Określa nazwę profilu.</span><span class="sxs-lookup"><span data-stu-id="822fb-120">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="822fb-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="822fb-121">-ResourceGroupName</span></span>
<span data-ttu-id="822fb-122">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="822fb-122">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="822fb-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="822fb-123">CommonParameters</span></span>
<span data-ttu-id="822fb-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="822fb-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="822fb-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="822fb-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="822fb-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="822fb-126">INPUTS</span></span>

### <span data-ttu-id="822fb-127">Microsoft. Azure. Commands. CDN. models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="822fb-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="822fb-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="822fb-128">OUTPUTS</span></span>

### <span data-ttu-id="822fb-129">Microsoft. Azure. Commands. CDN. models. Endpoint. PSValidateCustomDomainOutput</span><span class="sxs-lookup"><span data-stu-id="822fb-129">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateCustomDomainOutput</span></span>

## <span data-ttu-id="822fb-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="822fb-130">NOTES</span></span>

## <span data-ttu-id="822fb-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="822fb-131">RELATED LINKS</span></span>

[<span data-ttu-id="822fb-132">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="822fb-132">Get-AzCdnCustomDomain</span></span>](./Get-AzCdnCustomDomain.md)

[<span data-ttu-id="822fb-133">Nowe — AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="822fb-133">New-AzCdnCustomDomain</span></span>](./New-AzCdnCustomDomain.md)

[<span data-ttu-id="822fb-134">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="822fb-134">Remove-AzCdnCustomDomain</span></span>](./Remove-AzCdnCustomDomain.md)


