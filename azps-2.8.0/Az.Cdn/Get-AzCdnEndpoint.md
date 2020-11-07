---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: F93D9D7C-AC2A-4D83-87EC-4A54CD45272B
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpoint.md
ms.openlocfilehash: 09439fd202d01d6cf5ffc8be614940cdf39ad1ac
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706578"
---
# <span data-ttu-id="e3cee-101">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e3cee-101">Get-AzCdnEndpoint</span></span>

## <span data-ttu-id="e3cee-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e3cee-102">SYNOPSIS</span></span>
<span data-ttu-id="e3cee-103">Pobiera punkt końcowy sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="e3cee-103">Gets a CDN endpoint.</span></span>

## <span data-ttu-id="e3cee-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e3cee-104">SYNTAX</span></span>

### <span data-ttu-id="e3cee-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e3cee-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnEndpoint [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e3cee-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3cee-106">ByObjectParameterSet</span></span>
```
Get-AzCdnEndpoint [-EndpointName <String>] -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e3cee-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e3cee-107">DESCRIPTION</span></span>
<span data-ttu-id="e3cee-108">Polecenie cmdlet **Get-AzCdnEndpoint** umożliwia pobranie punktu końcowego sieci dostarczania zawartości platformy Azure (CDN) i skojarzonych z nim danych konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="e3cee-108">The **Get-AzCdnEndpoint** cmdlet gets an Azure Content Delivery Network (CDN) endpoint and its associated configuration data.</span></span>

## <span data-ttu-id="e3cee-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e3cee-109">EXAMPLES</span></span>

## <span data-ttu-id="e3cee-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e3cee-110">PARAMETERS</span></span>

### <span data-ttu-id="e3cee-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="e3cee-111">-CdnProfile</span></span>
<span data-ttu-id="e3cee-112">Określa obiekt profilu sieci CDN, do którego należy punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="e3cee-112">Specifies the CDN profile object to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="e3cee-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3cee-113">-DefaultProfile</span></span>
<span data-ttu-id="e3cee-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="e3cee-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e3cee-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="e3cee-115">-EndpointName</span></span>
<span data-ttu-id="e3cee-116">Określa nazwę punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="e3cee-116">Specifies the name of the endpoint.</span></span>
<span data-ttu-id="e3cee-117">Nazwa punktu końcowego nie jest nazwą hosta punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="e3cee-117">The name of the endpoint is not the host name of the endpoint.</span></span>

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

### <span data-ttu-id="e3cee-118">-Refilename</span><span class="sxs-lookup"><span data-stu-id="e3cee-118">-ProfileName</span></span>
<span data-ttu-id="e3cee-119">Określa nazwę profilu, do którego należy punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="e3cee-119">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="e3cee-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3cee-120">-ResourceGroupName</span></span>
<span data-ttu-id="e3cee-121">Określa nazwę grupy zasobów, do której należy punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="e3cee-121">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="e3cee-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3cee-122">CommonParameters</span></span>
<span data-ttu-id="e3cee-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3cee-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3cee-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e3cee-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3cee-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e3cee-125">INPUTS</span></span>

### <span data-ttu-id="e3cee-126">Microsoft. Azure. Commands. CDN. models. profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="e3cee-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="e3cee-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e3cee-127">OUTPUTS</span></span>

### <span data-ttu-id="e3cee-128">Microsoft. Azure. Commands. CDN. models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="e3cee-128">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="e3cee-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e3cee-129">NOTES</span></span>

## <span data-ttu-id="e3cee-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e3cee-130">RELATED LINKS</span></span>

[<span data-ttu-id="e3cee-131">Nowe — AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e3cee-131">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="e3cee-132">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e3cee-132">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="e3cee-133">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e3cee-133">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="e3cee-134">Start — AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e3cee-134">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="e3cee-135">Zatrzymaj — AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e3cee-135">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)

