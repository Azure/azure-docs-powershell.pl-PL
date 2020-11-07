---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 53246003-D1E9-4863-94E9-8E0BF1272134
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnCustomDomain.md
ms.openlocfilehash: b87963b45010299dcb80c4b1859af8614f845526
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527041"
---
# <span data-ttu-id="82431-101">Get-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="82431-101">Get-AzureRmCdnCustomDomain</span></span>

## <span data-ttu-id="82431-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="82431-102">SYNOPSIS</span></span>
<span data-ttu-id="82431-103">Pobiera niestandardową domenę sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="82431-103">Gets a CDN custom domain.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="82431-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="82431-104">SYNTAX</span></span>

### <span data-ttu-id="82431-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="82431-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzureRmCdnCustomDomain [-CustomDomainName <String>] -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="82431-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="82431-106">ByObjectParameterSet</span></span>
```
Get-AzureRmCdnCustomDomain [-CustomDomainName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82431-107">Opis</span><span class="sxs-lookup"><span data-stu-id="82431-107">DESCRIPTION</span></span>
<span data-ttu-id="82431-108">Polecenie cmdlet **Get-AzureRmCdnCustomDomain** pobiera domenę niestandardową sieci dostarczania zawartości (CDN) platformy Azure oraz jej ustawienia pokrewne.</span><span class="sxs-lookup"><span data-stu-id="82431-108">The **Get-AzureRmCdnCustomDomain** cmdlet gets an Azure Content Delivery Network (CDN) custom domain and its related settings.</span></span>

## <span data-ttu-id="82431-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="82431-109">EXAMPLES</span></span>

## <span data-ttu-id="82431-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="82431-110">PARAMETERS</span></span>

### <span data-ttu-id="82431-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="82431-111">-CdnEndpoint</span></span>
<span data-ttu-id="82431-112">Określa obiekt punktu końcowego sieci CDN, do którego należy Twoja domena niestandardowa.</span><span class="sxs-lookup"><span data-stu-id="82431-112">Specifies the CDN endpoint object of which the custom domain is a member.</span></span>

```yaml
Type: PSEndpoint
Parameter Sets: ByObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="82431-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="82431-113">-CustomDomainName</span></span>
<span data-ttu-id="82431-114">Określa nazwę domeny niestandardowej.</span><span class="sxs-lookup"><span data-stu-id="82431-114">Specifies the name of the custom domain.</span></span>
<span data-ttu-id="82431-115">Nazwa domeny niestandardowej różni się od nazwy hosta domeny niestandardowej.</span><span class="sxs-lookup"><span data-stu-id="82431-115">The name of the custom domain differs from the host name of the custom domain.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82431-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82431-116">-DefaultProfile</span></span>
<span data-ttu-id="82431-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="82431-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82431-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="82431-118">-EndpointName</span></span>
<span data-ttu-id="82431-119">Określa nazwę punktu końcowego, do którego należy domena niestandardowa.</span><span class="sxs-lookup"><span data-stu-id="82431-119">Specifies the name of the endpoint to which the custom domain belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82431-120">-Refilename</span><span class="sxs-lookup"><span data-stu-id="82431-120">-ProfileName</span></span>
<span data-ttu-id="82431-121">Określa nazwę profilu, do którego należy domena niestandardowa.</span><span class="sxs-lookup"><span data-stu-id="82431-121">Specifies the name of the Profile to which the custom domain belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82431-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82431-122">-ResourceGroupName</span></span>
<span data-ttu-id="82431-123">Określa nazwę grupy zasobów, do której należy domena niestandardowa.</span><span class="sxs-lookup"><span data-stu-id="82431-123">Specifies the name of the resource group to which the custom domain belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82431-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82431-124">CommonParameters</span></span>
<span data-ttu-id="82431-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82431-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82431-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82431-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82431-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="82431-127">INPUTS</span></span>

### <span data-ttu-id="82431-128">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="82431-128">PSEndpoint</span></span>
<span data-ttu-id="82431-129">Parametr "CdnEndpoint" akceptuje wartość typu "PSEndpoint" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="82431-129">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="82431-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="82431-130">OUTPUTS</span></span>

###  
<span data-ttu-id="82431-131">To polecenie cmdlet zwraca obiekt domeny niestandardowej.</span><span class="sxs-lookup"><span data-stu-id="82431-131">This cmdlet returns a custom domain object.</span></span>

## <span data-ttu-id="82431-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="82431-132">NOTES</span></span>

## <span data-ttu-id="82431-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="82431-133">RELATED LINKS</span></span>

[<span data-ttu-id="82431-134">Nowe — AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="82431-134">New-AzureRmCdnCustomDomain</span></span>](./New-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="82431-135">Remove-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="82431-135">Remove-AzureRmCdnCustomDomain</span></span>](./Remove-AzureRmCdnCustomDomain.md)

