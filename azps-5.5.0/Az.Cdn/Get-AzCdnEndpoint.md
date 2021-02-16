---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: F93D9D7C-AC2A-4D83-87EC-4A54CD45272B
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpoint.md
ms.openlocfilehash: 5f137543d694ee9d470a1e24d1ba6d52b22cd2e5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200827"
---
# <span data-ttu-id="b5bc0-101">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b5bc0-101">Get-AzCdnEndpoint</span></span>

## <span data-ttu-id="b5bc0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5bc0-102">SYNOPSIS</span></span>
<span data-ttu-id="b5bc0-103">Pobiera punkt końcowy sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="b5bc0-103">Gets a CDN endpoint.</span></span>

## <span data-ttu-id="b5bc0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b5bc0-104">SYNTAX</span></span>

### <span data-ttu-id="b5bc0-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="b5bc0-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnEndpoint [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5bc0-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5bc0-106">ByObjectParameterSet</span></span>
```
Get-AzCdnEndpoint [-EndpointName <String>] -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b5bc0-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="b5bc0-107">DESCRIPTION</span></span>
<span data-ttu-id="b5bc0-108">Polecenie **cmdlet Get-AzCdnEndpoint** pobiera punkt końcowy usługi Azure Content Delivery Network (CDN) i skojarzone z nim dane konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="b5bc0-108">The **Get-AzCdnEndpoint** cmdlet gets an Azure Content Delivery Network (CDN) endpoint and its associated configuration data.</span></span>

## <span data-ttu-id="b5bc0-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b5bc0-109">EXAMPLES</span></span>

## <span data-ttu-id="b5bc0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b5bc0-110">PARAMETERS</span></span>

### <span data-ttu-id="b5bc0-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="b5bc0-111">-CdnProfile</span></span>
<span data-ttu-id="b5bc0-112">Określa obiekt profilu sieci CDN, do którego należy punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="b5bc0-112">Specifies the CDN profile object to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="b5bc0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5bc0-113">-DefaultProfile</span></span>
<span data-ttu-id="b5bc0-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="b5bc0-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b5bc0-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="b5bc0-115">-EndpointName</span></span>
<span data-ttu-id="b5bc0-116">Określa nazwę punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="b5bc0-116">Specifies the name of the endpoint.</span></span>
<span data-ttu-id="b5bc0-117">Nazwa punktu końcowego nie jest nazwą hosta punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="b5bc0-117">The name of the endpoint is not the host name of the endpoint.</span></span>

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

### <span data-ttu-id="b5bc0-118">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="b5bc0-118">-ProfileName</span></span>
<span data-ttu-id="b5bc0-119">Określa nazwę profilu, do którego należy punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="b5bc0-119">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="b5bc0-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5bc0-120">-ResourceGroupName</span></span>
<span data-ttu-id="b5bc0-121">Określa nazwę grupy zasobów, do której należy punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="b5bc0-121">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="b5bc0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5bc0-122">CommonParameters</span></span>
<span data-ttu-id="b5bc0-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5bc0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5bc0-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b5bc0-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5bc0-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b5bc0-125">INPUTS</span></span>

### <span data-ttu-id="b5bc0-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="b5bc0-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="b5bc0-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b5bc0-127">OUTPUTS</span></span>

### <span data-ttu-id="b5bc0-128">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="b5bc0-128">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="b5bc0-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b5bc0-129">NOTES</span></span>

## <span data-ttu-id="b5bc0-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b5bc0-130">RELATED LINKS</span></span>

[<span data-ttu-id="b5bc0-131">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b5bc0-131">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="b5bc0-132">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b5bc0-132">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="b5bc0-133">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b5bc0-133">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="b5bc0-134">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b5bc0-134">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="b5bc0-135">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b5bc0-135">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


