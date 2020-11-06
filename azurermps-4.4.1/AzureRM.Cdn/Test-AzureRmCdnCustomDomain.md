---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 8C4E824F-FB4A-4DE7-8FD9-3FDA3848F25C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Test-AzureRmCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Test-AzureRmCdnCustomDomain.md
ms.openlocfilehash: df871dff0f59bc9c1e319e1470bbaa37750542e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547004"
---
# <span data-ttu-id="69441-101">Test-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="69441-101">Test-AzureRmCdnCustomDomain</span></span>

## <span data-ttu-id="69441-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="69441-102">SYNOPSIS</span></span>
<span data-ttu-id="69441-103">Sprawdza, czy do punktu końcowego można dodać domenę niestandardową.</span><span class="sxs-lookup"><span data-stu-id="69441-103">Checks whether a custom domain can be added to an endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="69441-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="69441-104">SYNTAX</span></span>

### <span data-ttu-id="69441-105">Parametr ustawiony dla parametrów pól (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="69441-105">Parameter Set for fields parameters (Default)</span></span>
```
Test-AzureRmCdnCustomDomain -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -CustomDomainHostName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="69441-106">Zestaw parametrów dla parametrów obiektu</span><span class="sxs-lookup"><span data-stu-id="69441-106">Parameter Set for object parameters</span></span>
```
Test-AzureRmCdnCustomDomain -CdnEndpoint <PSEndpoint> -CustomDomainHostName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69441-107">Opis</span><span class="sxs-lookup"><span data-stu-id="69441-107">DESCRIPTION</span></span>
<span data-ttu-id="69441-108">Polecenie cmdlet **test-AzureRmCdnCustomDomain** sprawdza, czy można dodać domenę niestandardową do punktu końcowego, sprawdzając poprawność mapowania CNAME.</span><span class="sxs-lookup"><span data-stu-id="69441-108">The **Test-AzureRmCdnCustomDomain** cmdlet checks whether a custom domain can be added to an endpoint by validating the CName mapping.</span></span>

## <span data-ttu-id="69441-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="69441-109">EXAMPLES</span></span>

## <span data-ttu-id="69441-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="69441-110">PARAMETERS</span></span>

### <span data-ttu-id="69441-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="69441-111">-CdnEndpoint</span></span>
<span data-ttu-id="69441-112">Określa punkt końcowy, do którego ma zostać dodana domena niestandardowa.</span><span class="sxs-lookup"><span data-stu-id="69441-112">Specifies the endpoint to which you want to add the custom domain.</span></span>

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

### <span data-ttu-id="69441-113">-CustomDomainHostName</span><span class="sxs-lookup"><span data-stu-id="69441-113">-CustomDomainHostName</span></span>
<span data-ttu-id="69441-114">Określa nazwę hosta domeny niestandardowej.</span><span class="sxs-lookup"><span data-stu-id="69441-114">Specifies the host name of the custom domain.</span></span>

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

### <span data-ttu-id="69441-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="69441-115">-EndpointName</span></span>
<span data-ttu-id="69441-116">Określa nazwę punktu końcowego, do którego chcesz dodać domenę niestandardową.</span><span class="sxs-lookup"><span data-stu-id="69441-116">Specifies the name of the endpoint to which you want to add the custom domain.</span></span>

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

### <span data-ttu-id="69441-117">-Refilename</span><span class="sxs-lookup"><span data-stu-id="69441-117">-ProfileName</span></span>
<span data-ttu-id="69441-118">Określa nazwę profilu.</span><span class="sxs-lookup"><span data-stu-id="69441-118">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="69441-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69441-119">-ResourceGroupName</span></span>
<span data-ttu-id="69441-120">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="69441-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="69441-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69441-121">-DefaultProfile</span></span>
<span data-ttu-id="69441-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="69441-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69441-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69441-123">CommonParameters</span></span>
<span data-ttu-id="69441-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69441-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69441-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69441-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69441-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="69441-126">INPUTS</span></span>

### <span data-ttu-id="69441-127">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="69441-127">PSEndpoint</span></span>
<span data-ttu-id="69441-128">Parametr "CdnEndpoint" akceptuje wartość typu "PSEndpoint" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="69441-128">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="69441-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="69441-129">OUTPUTS</span></span>

### <span data-ttu-id="69441-130">Microsoft. Azure. Commands. CDN. models. Endpoint. PSValidateCustomDomainOutput</span><span class="sxs-lookup"><span data-stu-id="69441-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateCustomDomainOutput</span></span>

## <span data-ttu-id="69441-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="69441-131">NOTES</span></span>

## <span data-ttu-id="69441-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="69441-132">RELATED LINKS</span></span>

[<span data-ttu-id="69441-133">Get-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="69441-133">Get-AzureRmCdnCustomDomain</span></span>](./Get-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="69441-134">Nowe — AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="69441-134">New-AzureRmCdnCustomDomain</span></span>](./New-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="69441-135">Remove-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="69441-135">Remove-AzureRmCdnCustomDomain</span></span>](./Remove-AzureRmCdnCustomDomain.md)


