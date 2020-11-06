---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: F93D9D7C-AC2A-4D83-87EC-4A54CD45272B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpoint.md
ms.openlocfilehash: eb4215a281b83bd533a7502e3ec538ec4e3a570c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549419"
---
# <span data-ttu-id="ca773-101">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="ca773-101">Get-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="ca773-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ca773-102">SYNOPSIS</span></span>
<span data-ttu-id="ca773-103">Pobiera punkt końcowy sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="ca773-103">Gets a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ca773-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ca773-104">SYNTAX</span></span>

### <span data-ttu-id="ca773-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ca773-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzureRmCdnEndpoint [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ca773-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca773-106">ByObjectParameterSet</span></span>
```
Get-AzureRmCdnEndpoint [-EndpointName <String>] -CdnProfile <PSProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ca773-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ca773-107">DESCRIPTION</span></span>
<span data-ttu-id="ca773-108">Polecenie cmdlet **Get-AzureRMCdnEndpoint** umożliwia pobranie punktu końcowego sieci dostarczania zawartości platformy Azure (CDN) i skojarzonych z nim danych konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="ca773-108">The **Get-AzureRMCdnEndpoint** cmdlet gets an Azure Content Delivery Network (CDN) endpoint and its associated configuration data.</span></span>

## <span data-ttu-id="ca773-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ca773-109">EXAMPLES</span></span>

## <span data-ttu-id="ca773-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ca773-110">PARAMETERS</span></span>

### <span data-ttu-id="ca773-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="ca773-111">-CdnProfile</span></span>
<span data-ttu-id="ca773-112">Określa obiekt profilu sieci CDN, do którego należy punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="ca773-112">Specifies the CDN profile object to which the endpoint belongs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ca773-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca773-113">-DefaultProfile</span></span>
<span data-ttu-id="ca773-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="ca773-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ca773-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="ca773-115">-EndpointName</span></span>
<span data-ttu-id="ca773-116">Określa nazwę punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="ca773-116">Specifies the name of the endpoint.</span></span>
<span data-ttu-id="ca773-117">Nazwa punktu końcowego nie jest nazwą hosta punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="ca773-117">The name of the endpoint is not the host name of the endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca773-118">-Refilename</span><span class="sxs-lookup"><span data-stu-id="ca773-118">-ProfileName</span></span>
<span data-ttu-id="ca773-119">Określa nazwę profilu, do którego należy punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="ca773-119">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="ca773-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca773-120">-ResourceGroupName</span></span>
<span data-ttu-id="ca773-121">Określa nazwę grupy zasobów, do której należy punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="ca773-121">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="ca773-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca773-122">CommonParameters</span></span>
<span data-ttu-id="ca773-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca773-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca773-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca773-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca773-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ca773-125">INPUTS</span></span>

### <span data-ttu-id="ca773-126">Microsoft. Azure. Commands. CDN. models. profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="ca773-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>
<span data-ttu-id="ca773-127">Parametry: CdnProfile (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ca773-127">Parameters: CdnProfile (ByValue)</span></span>

## <span data-ttu-id="ca773-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ca773-128">OUTPUTS</span></span>

### <span data-ttu-id="ca773-129">Microsoft. Azure. Commands. CDN. models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="ca773-129">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="ca773-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ca773-130">NOTES</span></span>

## <span data-ttu-id="ca773-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ca773-131">RELATED LINKS</span></span>

[<span data-ttu-id="ca773-132">Nowe — AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="ca773-132">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="ca773-133">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="ca773-133">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="ca773-134">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="ca773-134">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="ca773-135">Start — AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="ca773-135">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)

[<span data-ttu-id="ca773-136">Zatrzymaj — AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="ca773-136">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)


