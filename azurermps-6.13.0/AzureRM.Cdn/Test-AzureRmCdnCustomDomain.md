---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 8C4E824F-FB4A-4DE7-8FD9-3FDA3848F25C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/test-azurermcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Test-AzureRmCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Test-AzureRmCdnCustomDomain.md
ms.openlocfilehash: e249331f70e0ef0b7e1397f514363787e9dcf0dd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550336"
---
# <span data-ttu-id="bec5a-101">Test-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="bec5a-101">Test-AzureRmCdnCustomDomain</span></span>

## <span data-ttu-id="bec5a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bec5a-102">SYNOPSIS</span></span>
<span data-ttu-id="bec5a-103">Sprawdza, czy do punktu końcowego można dodać domenę niestandardową.</span><span class="sxs-lookup"><span data-stu-id="bec5a-103">Checks whether a custom domain can be added to an endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bec5a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bec5a-104">SYNTAX</span></span>

### <span data-ttu-id="bec5a-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="bec5a-105">ByFieldsParameterSet (Default)</span></span>
```
Test-AzureRmCdnCustomDomain -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -CustomDomainHostName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bec5a-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bec5a-106">ByObjectParameterSet</span></span>
```
Test-AzureRmCdnCustomDomain -CdnEndpoint <PSEndpoint> -CustomDomainHostName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bec5a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="bec5a-107">DESCRIPTION</span></span>
<span data-ttu-id="bec5a-108">Polecenie cmdlet **test-AzureRmCdnCustomDomain** sprawdza, czy można dodać domenę niestandardową do punktu końcowego, sprawdzając poprawność mapowania CNAME.</span><span class="sxs-lookup"><span data-stu-id="bec5a-108">The **Test-AzureRmCdnCustomDomain** cmdlet checks whether a custom domain can be added to an endpoint by validating the CName mapping.</span></span>

## <span data-ttu-id="bec5a-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bec5a-109">EXAMPLES</span></span>

## <span data-ttu-id="bec5a-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bec5a-110">PARAMETERS</span></span>

### <span data-ttu-id="bec5a-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="bec5a-111">-CdnEndpoint</span></span>
<span data-ttu-id="bec5a-112">Określa punkt końcowy, do którego ma zostać dodana domena niestandardowa.</span><span class="sxs-lookup"><span data-stu-id="bec5a-112">Specifies the endpoint to which you want to add the custom domain.</span></span>

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

### <span data-ttu-id="bec5a-113">-CustomDomainHostName</span><span class="sxs-lookup"><span data-stu-id="bec5a-113">-CustomDomainHostName</span></span>
<span data-ttu-id="bec5a-114">Określa nazwę hosta domeny niestandardowej.</span><span class="sxs-lookup"><span data-stu-id="bec5a-114">Specifies the host name of the custom domain.</span></span>

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

### <span data-ttu-id="bec5a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bec5a-115">-DefaultProfile</span></span>
<span data-ttu-id="bec5a-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="bec5a-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bec5a-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="bec5a-117">-EndpointName</span></span>
<span data-ttu-id="bec5a-118">Określa nazwę punktu końcowego, do którego chcesz dodać domenę niestandardową.</span><span class="sxs-lookup"><span data-stu-id="bec5a-118">Specifies the name of the endpoint to which you want to add the custom domain.</span></span>

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

### <span data-ttu-id="bec5a-119">-Refilename</span><span class="sxs-lookup"><span data-stu-id="bec5a-119">-ProfileName</span></span>
<span data-ttu-id="bec5a-120">Określa nazwę profilu.</span><span class="sxs-lookup"><span data-stu-id="bec5a-120">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="bec5a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bec5a-121">-ResourceGroupName</span></span>
<span data-ttu-id="bec5a-122">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="bec5a-122">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="bec5a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bec5a-123">CommonParameters</span></span>
<span data-ttu-id="bec5a-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bec5a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bec5a-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bec5a-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bec5a-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bec5a-126">INPUTS</span></span>

### <span data-ttu-id="bec5a-127">Microsoft. Azure. Commands. CDN. models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="bec5a-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>
<span data-ttu-id="bec5a-128">Parametry: CdnEndpoint (ByValue)</span><span class="sxs-lookup"><span data-stu-id="bec5a-128">Parameters: CdnEndpoint (ByValue)</span></span>

## <span data-ttu-id="bec5a-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bec5a-129">OUTPUTS</span></span>

### <span data-ttu-id="bec5a-130">Microsoft. Azure. Commands. CDN. models. Endpoint. PSValidateCustomDomainOutput</span><span class="sxs-lookup"><span data-stu-id="bec5a-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateCustomDomainOutput</span></span>

## <span data-ttu-id="bec5a-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bec5a-131">NOTES</span></span>

## <span data-ttu-id="bec5a-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bec5a-132">RELATED LINKS</span></span>

[<span data-ttu-id="bec5a-133">Get-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="bec5a-133">Get-AzureRmCdnCustomDomain</span></span>](./Get-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="bec5a-134">Nowe — AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="bec5a-134">New-AzureRmCdnCustomDomain</span></span>](./New-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="bec5a-135">Remove-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="bec5a-135">Remove-AzureRmCdnCustomDomain</span></span>](./Remove-AzureRmCdnCustomDomain.md)


