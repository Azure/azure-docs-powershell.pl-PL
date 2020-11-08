---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 91919242-59ED-4938-A3A3-23A66F85FBC1
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOrigin.md
ms.openlocfilehash: e5e27dba4519d16ebc304f3d6cca99f32f23e341
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94234007"
---
# <span data-ttu-id="c9d22-101">Get-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="c9d22-101">Get-AzCdnOrigin</span></span>

## <span data-ttu-id="c9d22-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c9d22-102">SYNOPSIS</span></span>
<span data-ttu-id="c9d22-103">Pobiera serwer pochodzenia sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="c9d22-103">Gets a CDN origin server.</span></span>

## <span data-ttu-id="c9d22-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c9d22-104">SYNTAX</span></span>

### <span data-ttu-id="c9d22-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c9d22-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnOrigin [-OriginName <String>] -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c9d22-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9d22-106">ByResourceIdParameterSet</span></span>
```
Get-AzCdnOrigin [-OriginName <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c9d22-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9d22-107">ByObjectParameterSet</span></span>
```
Get-AzCdnOrigin [-OriginName <String>] -CdnEndpoint <PSEndpoint> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c9d22-108">Opis</span><span class="sxs-lookup"><span data-stu-id="c9d22-108">DESCRIPTION</span></span>
<span data-ttu-id="c9d22-109">Polecenie cmdlet **Get-AzCdnOrigin** pobiera serwer pochodzenia sieci dostarczania zawartości platformy Azure (CDN) i jego dane konfiguracyjne.</span><span class="sxs-lookup"><span data-stu-id="c9d22-109">The **Get-AzCdnOrigin** cmdlet gets an Azure Content Delivery Network (CDN) origin server and its configuration data.</span></span>

## <span data-ttu-id="c9d22-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c9d22-110">EXAMPLES</span></span>

## <span data-ttu-id="c9d22-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c9d22-111">PARAMETERS</span></span>

### <span data-ttu-id="c9d22-112">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="c9d22-112">-CdnEndpoint</span></span>
<span data-ttu-id="c9d22-113">Określa obiekt punktu końcowego sieci CDN, do którego należy pochodzenie.</span><span class="sxs-lookup"><span data-stu-id="c9d22-113">Specifies the CDN endpoint object to which the origin belongs.</span></span>

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

### <span data-ttu-id="c9d22-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9d22-114">-DefaultProfile</span></span>
<span data-ttu-id="c9d22-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="c9d22-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c9d22-116">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="c9d22-116">-EndpointName</span></span>
<span data-ttu-id="c9d22-117">Określa nazwę punktu końcowego, do którego należy serwer pochodzenia.</span><span class="sxs-lookup"><span data-stu-id="c9d22-117">Specifies the name of the endpoint to which the origin server belongs.</span></span>

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

### <span data-ttu-id="c9d22-118">-Originname</span><span class="sxs-lookup"><span data-stu-id="c9d22-118">-OriginName</span></span>
<span data-ttu-id="c9d22-119">Określa nazwę serwera pochodzenia.</span><span class="sxs-lookup"><span data-stu-id="c9d22-119">Specifies the name of the origin server.</span></span>

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

### <span data-ttu-id="c9d22-120">-Refilename</span><span class="sxs-lookup"><span data-stu-id="c9d22-120">-ProfileName</span></span>
<span data-ttu-id="c9d22-121">Określa nazwę profilu, do którego należy serwer pochodzenia.</span><span class="sxs-lookup"><span data-stu-id="c9d22-121">Specifies the name of the profile to which the origin server belongs.</span></span>

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

### <span data-ttu-id="c9d22-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9d22-122">-ResourceGroupName</span></span>
<span data-ttu-id="c9d22-123">Określa nazwę grupy zasobów, do której należy serwer pochodzenia.</span><span class="sxs-lookup"><span data-stu-id="c9d22-123">Specifies the name of the resource group to which the origin server belongs.</span></span>

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

### <span data-ttu-id="c9d22-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c9d22-124">-ResourceId</span></span>
<span data-ttu-id="c9d22-125">Identyfikator zasobu pochodzenia usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="c9d22-125">The resource id of the Azure CDN origin.</span></span>

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

### <span data-ttu-id="c9d22-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9d22-126">CommonParameters</span></span>
<span data-ttu-id="c9d22-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9d22-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9d22-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c9d22-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9d22-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c9d22-129">INPUTS</span></span>

### <span data-ttu-id="c9d22-130">Microsoft. Azure. Commands. CDN. models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="c9d22-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="c9d22-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c9d22-131">OUTPUTS</span></span>

### <span data-ttu-id="c9d22-132">Microsoft. Azure. Commands. CDN. MODELES. Origin. PSOrigin</span><span class="sxs-lookup"><span data-stu-id="c9d22-132">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="c9d22-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c9d22-133">NOTES</span></span>

## <span data-ttu-id="c9d22-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c9d22-134">RELATED LINKS</span></span>

[<span data-ttu-id="c9d22-135">Set-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="c9d22-135">Set-AzCdnOrigin</span></span>](./Set-AzCdnOrigin.md)


