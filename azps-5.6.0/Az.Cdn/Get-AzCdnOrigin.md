---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 91919242-59ED-4938-A3A3-23A66F85FBC1
online version: https://docs.microsoft.com/powershell/module/az.cdn/get-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOrigin.md
ms.openlocfilehash: 5c2aa677bd2f197cfae262ed54372d5172fe2a4e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009265"
---
# <span data-ttu-id="2e759-101">Get-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="2e759-101">Get-AzCdnOrigin</span></span>

## <span data-ttu-id="2e759-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e759-102">SYNOPSIS</span></span>
<span data-ttu-id="2e759-103">Pobiera serwer pochodzenia sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="2e759-103">Gets a CDN origin server.</span></span>

## <span data-ttu-id="2e759-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2e759-104">SYNTAX</span></span>

### <span data-ttu-id="2e759-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="2e759-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnOrigin [-OriginName <String>] -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2e759-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e759-106">ByResourceIdParameterSet</span></span>
```
Get-AzCdnOrigin [-OriginName <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2e759-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e759-107">ByObjectParameterSet</span></span>
```
Get-AzCdnOrigin [-OriginName <String>] -CdnEndpoint <PSEndpoint> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2e759-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="2e759-108">DESCRIPTION</span></span>
<span data-ttu-id="2e759-109">Polecenie **cmdlet Get-AzCdnOrigin** pobiera serwer pochodzenia Azure Content Delivery Network (CDN) i jego dane konfiguracyjne.</span><span class="sxs-lookup"><span data-stu-id="2e759-109">The **Get-AzCdnOrigin** cmdlet gets an Azure Content Delivery Network (CDN) origin server and its configuration data.</span></span>

## <span data-ttu-id="2e759-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2e759-110">EXAMPLES</span></span>

## <span data-ttu-id="2e759-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2e759-111">PARAMETERS</span></span>

### <span data-ttu-id="2e759-112">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="2e759-112">-CdnEndpoint</span></span>
<span data-ttu-id="2e759-113">Określa obiekt punktu końcowego sieci CDN, do którego należy pochodzenie.</span><span class="sxs-lookup"><span data-stu-id="2e759-113">Specifies the CDN endpoint object to which the origin belongs.</span></span>

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

### <span data-ttu-id="2e759-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e759-114">-DefaultProfile</span></span>
<span data-ttu-id="2e759-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="2e759-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2e759-116">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="2e759-116">-EndpointName</span></span>
<span data-ttu-id="2e759-117">Określa nazwę punktu końcowego, do którego należy serwer pochodzenia.</span><span class="sxs-lookup"><span data-stu-id="2e759-117">Specifies the name of the endpoint to which the origin server belongs.</span></span>

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

### <span data-ttu-id="2e759-118">-OriginName</span><span class="sxs-lookup"><span data-stu-id="2e759-118">-OriginName</span></span>
<span data-ttu-id="2e759-119">Określa nazwę serwera pochodzenia.</span><span class="sxs-lookup"><span data-stu-id="2e759-119">Specifies the name of the origin server.</span></span>

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

### <span data-ttu-id="2e759-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="2e759-120">-ProfileName</span></span>
<span data-ttu-id="2e759-121">Określa nazwę profilu, do którego należy serwer pochodzenia.</span><span class="sxs-lookup"><span data-stu-id="2e759-121">Specifies the name of the profile to which the origin server belongs.</span></span>

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

### <span data-ttu-id="2e759-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e759-122">-ResourceGroupName</span></span>
<span data-ttu-id="2e759-123">Określa nazwę grupy zasobów, do której należy serwer pochodzenia.</span><span class="sxs-lookup"><span data-stu-id="2e759-123">Specifies the name of the resource group to which the origin server belongs.</span></span>

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

### <span data-ttu-id="2e759-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2e759-124">-ResourceId</span></span>
<span data-ttu-id="2e759-125">Identyfikator zasobu pochodzenia sieci Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="2e759-125">The resource id of the Azure CDN origin.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e759-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e759-126">CommonParameters</span></span>
<span data-ttu-id="2e759-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e759-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e759-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2e759-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e759-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2e759-129">INPUTS</span></span>

### <span data-ttu-id="2e759-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="2e759-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="2e759-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2e759-131">OUTPUTS</span></span>

### <span data-ttu-id="2e759-132">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span><span class="sxs-lookup"><span data-stu-id="2e759-132">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="2e759-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2e759-133">NOTES</span></span>

## <span data-ttu-id="2e759-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2e759-134">RELATED LINKS</span></span>

[<span data-ttu-id="2e759-135">Set-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="2e759-135">Set-AzCdnOrigin</span></span>](./Set-AzCdnOrigin.md)


