---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: AFDBE48E-63B0-4A9E-9825-5246081AA129
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/publish-azcdnendpointcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Publish-AzCdnEndpointContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Publish-AzCdnEndpointContent.md
ms.openlocfilehash: 6e8ba9fb6fb65980113ae8093bc4e3c258861968
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504193"
---
# <span data-ttu-id="b458c-101">Publish-AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="b458c-101">Publish-AzCdnEndpointContent</span></span>

## <span data-ttu-id="b458c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b458c-102">SYNOPSIS</span></span>
<span data-ttu-id="b458c-103">Ładuje zawartość do punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="b458c-103">Loads content to an endpoint.</span></span>

## <span data-ttu-id="b458c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b458c-104">SYNTAX</span></span>

### <span data-ttu-id="b458c-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b458c-105">ByFieldsParameterSet (Default)</span></span>
```
Publish-AzCdnEndpointContent -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -LoadContent <String[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b458c-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b458c-106">ByObjectParameterSet</span></span>
```
Publish-AzCdnEndpointContent -CdnEndpoint <PSEndpoint> -LoadContent <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b458c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="b458c-107">DESCRIPTION</span></span>
<span data-ttu-id="b458c-108">Polecenie cmdlet **Publish-AzCdnEndpointContent** ładuje zawartość z serwera źródłowego dla punktu końcowego sieci dostarczania zawartości Azure (CDN, Content Delivery Network).</span><span class="sxs-lookup"><span data-stu-id="b458c-108">The **Publish-AzCdnEndpointContent** cmdlet loads content from an origin server for the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="b458c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b458c-109">EXAMPLES</span></span>

## <span data-ttu-id="b458c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b458c-110">PARAMETERS</span></span>

### <span data-ttu-id="b458c-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b458c-111">-CdnEndpoint</span></span>
<span data-ttu-id="b458c-112">Określa punkt końcowy sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="b458c-112">Specifies the CDN endpoint.</span></span>

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

### <span data-ttu-id="b458c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b458c-113">-DefaultProfile</span></span>
<span data-ttu-id="b458c-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="b458c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b458c-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="b458c-115">-EndpointName</span></span>
<span data-ttu-id="b458c-116">Określa nazwę punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="b458c-116">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="b458c-117">-LoadContent</span><span class="sxs-lookup"><span data-stu-id="b458c-117">-LoadContent</span></span>
<span data-ttu-id="b458c-118">Określa tablicę względnych ścieżek dla zawartości na serwerze pochodzenia, którą publikuje polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b458c-118">Specifies an array of relative paths for the content on the origin server that this cmdlet publishes.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b458c-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b458c-119">-PassThru</span></span>
<span data-ttu-id="b458c-120">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="b458c-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b458c-121">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="b458c-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b458c-122">-Refilename</span><span class="sxs-lookup"><span data-stu-id="b458c-122">-ProfileName</span></span>
<span data-ttu-id="b458c-123">Określa nazwę profilu, do którego należy serwer pochodzenia.</span><span class="sxs-lookup"><span data-stu-id="b458c-123">Specifies the name of the profile to which the origin server belongs.</span></span>

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

### <span data-ttu-id="b458c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b458c-124">-ResourceGroupName</span></span>
<span data-ttu-id="b458c-125">Określa nazwę grupy zasobów, do której należy serwer pochodzenia.</span><span class="sxs-lookup"><span data-stu-id="b458c-125">Specifies the name of the resource group to which the origin server belongs.</span></span>

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

### <span data-ttu-id="b458c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b458c-126">CommonParameters</span></span>
<span data-ttu-id="b458c-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b458c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b458c-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b458c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b458c-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b458c-129">INPUTS</span></span>

### <span data-ttu-id="b458c-130">Microsoft. Azure. Commands. CDN. models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="b458c-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="b458c-131">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b458c-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b458c-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b458c-132">OUTPUTS</span></span>

### <span data-ttu-id="b458c-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b458c-133">System.Boolean</span></span>

## <span data-ttu-id="b458c-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b458c-134">NOTES</span></span>

## <span data-ttu-id="b458c-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b458c-135">RELATED LINKS</span></span>

[<span data-ttu-id="b458c-136">Cofnięcie publikowania — AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="b458c-136">Unpublish-AzCdnEndpointContent</span></span>](./Unpublish-AzCdnEndpointContent.md)


