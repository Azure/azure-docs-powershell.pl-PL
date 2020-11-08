---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 91919242-59ED-4938-A3A3-23A66F85FBC1
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOrigin.md
ms.openlocfilehash: f648d347e45b6394776a25735efbb06157cc5611
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94221401"
---
# <span data-ttu-id="e39e0-101">Get-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="e39e0-101">Get-AzCdnOrigin</span></span>

## <span data-ttu-id="e39e0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e39e0-102">SYNOPSIS</span></span>
<span data-ttu-id="e39e0-103">Pobiera serwer pochodzenia sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="e39e0-103">Gets a CDN origin server.</span></span>

## <span data-ttu-id="e39e0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e39e0-104">SYNTAX</span></span>

### <span data-ttu-id="e39e0-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e39e0-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnOrigin [-OriginName <String>] -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e39e0-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e39e0-106">ByObjectParameterSet</span></span>
```
Get-AzCdnOrigin [-OriginName <String>] -CdnEndpoint <PSEndpoint> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e39e0-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e39e0-107">DESCRIPTION</span></span>
<span data-ttu-id="e39e0-108">Polecenie cmdlet **Get-AzCdnOrigin** pobiera serwer pochodzenia sieci dostarczania zawartości platformy Azure (CDN) i jego dane konfiguracyjne.</span><span class="sxs-lookup"><span data-stu-id="e39e0-108">The **Get-AzCdnOrigin** cmdlet gets an Azure Content Delivery Network (CDN) origin server and its configuration data.</span></span>

## <span data-ttu-id="e39e0-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e39e0-109">EXAMPLES</span></span>

## <span data-ttu-id="e39e0-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e39e0-110">PARAMETERS</span></span>

### <span data-ttu-id="e39e0-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e39e0-111">-CdnEndpoint</span></span>
<span data-ttu-id="e39e0-112">Określa obiekt punktu końcowego sieci CDN, do którego należy pochodzenie.</span><span class="sxs-lookup"><span data-stu-id="e39e0-112">Specifies the CDN endpoint object to which the origin belongs.</span></span>

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

### <span data-ttu-id="e39e0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e39e0-113">-DefaultProfile</span></span>
<span data-ttu-id="e39e0-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="e39e0-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e39e0-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="e39e0-115">-EndpointName</span></span>
<span data-ttu-id="e39e0-116">Określa nazwę punktu końcowego, do którego należy serwer pochodzenia.</span><span class="sxs-lookup"><span data-stu-id="e39e0-116">Specifies the name of the endpoint to which the origin server belongs.</span></span>

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

### <span data-ttu-id="e39e0-117">-Originname</span><span class="sxs-lookup"><span data-stu-id="e39e0-117">-OriginName</span></span>
<span data-ttu-id="e39e0-118">Określa nazwę serwera pochodzenia.</span><span class="sxs-lookup"><span data-stu-id="e39e0-118">Specifies the name of the origin server.</span></span>

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

### <span data-ttu-id="e39e0-119">-Refilename</span><span class="sxs-lookup"><span data-stu-id="e39e0-119">-ProfileName</span></span>
<span data-ttu-id="e39e0-120">Określa nazwę profilu, do którego należy serwer pochodzenia.</span><span class="sxs-lookup"><span data-stu-id="e39e0-120">Specifies the name of the profile to which the origin server belongs.</span></span>

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

### <span data-ttu-id="e39e0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e39e0-121">-ResourceGroupName</span></span>
<span data-ttu-id="e39e0-122">Określa nazwę grupy zasobów, do której należy serwer pochodzenia.</span><span class="sxs-lookup"><span data-stu-id="e39e0-122">Specifies the name of the resource group to which the origin server belongs.</span></span>

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

### <span data-ttu-id="e39e0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e39e0-123">CommonParameters</span></span>
<span data-ttu-id="e39e0-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e39e0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e39e0-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e39e0-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e39e0-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e39e0-126">INPUTS</span></span>

### <span data-ttu-id="e39e0-127">Microsoft. Azure. Commands. CDN. models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="e39e0-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="e39e0-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e39e0-128">OUTPUTS</span></span>

### <span data-ttu-id="e39e0-129">Microsoft. Azure. Commands. CDN. MODELES. Origin. PSOrigin</span><span class="sxs-lookup"><span data-stu-id="e39e0-129">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="e39e0-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e39e0-130">NOTES</span></span>

## <span data-ttu-id="e39e0-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e39e0-131">RELATED LINKS</span></span>

[<span data-ttu-id="e39e0-132">Set-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="e39e0-132">Set-AzCdnOrigin</span></span>](./Set-AzCdnOrigin.md)


