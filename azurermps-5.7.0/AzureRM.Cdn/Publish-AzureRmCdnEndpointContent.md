---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: AFDBE48E-63B0-4A9E-9825-5246081AA129
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/publish-azurermcdnendpointcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Publish-AzureRmCdnEndpointContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Publish-AzureRmCdnEndpointContent.md
ms.openlocfilehash: 09bd1ae2c4c16bdc6af5103ec4e2854005961094
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716640"
---
# <span data-ttu-id="ecdf9-101">Publish-AzureRmCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="ecdf9-101">Publish-AzureRmCdnEndpointContent</span></span>

## <span data-ttu-id="ecdf9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ecdf9-102">SYNOPSIS</span></span>
<span data-ttu-id="ecdf9-103">Ładuje zawartość do punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="ecdf9-103">Loads content to an endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ecdf9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ecdf9-104">SYNTAX</span></span>

### <span data-ttu-id="ecdf9-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ecdf9-105">ByFieldsParameterSet (Default)</span></span>
```
Publish-AzureRmCdnEndpointContent -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -LoadContent <String[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ecdf9-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ecdf9-106">ByObjectParameterSet</span></span>
```
Publish-AzureRmCdnEndpointContent -CdnEndpoint <PSEndpoint> -LoadContent <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ecdf9-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ecdf9-107">DESCRIPTION</span></span>
<span data-ttu-id="ecdf9-108">Polecenie cmdlet **Publish-AzureRmCdnEndpointContent** ładuje zawartość z serwera źródłowego dla punktu końcowego sieci dostarczania zawartości Azure (CDN, Content Delivery Network).</span><span class="sxs-lookup"><span data-stu-id="ecdf9-108">The **Publish-AzureRmCdnEndpointContent** cmdlet loads content from an origin server for the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="ecdf9-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ecdf9-109">EXAMPLES</span></span>

## <span data-ttu-id="ecdf9-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ecdf9-110">PARAMETERS</span></span>

### <span data-ttu-id="ecdf9-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="ecdf9-111">-CdnEndpoint</span></span>
<span data-ttu-id="ecdf9-112">Sepcifies punkt końcowy sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="ecdf9-112">Sepcifies the CDN endpoint.</span></span>

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

### <span data-ttu-id="ecdf9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecdf9-113">-DefaultProfile</span></span>
<span data-ttu-id="ecdf9-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="ecdf9-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ecdf9-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="ecdf9-115">-EndpointName</span></span>
<span data-ttu-id="ecdf9-116">Określa nazwę punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="ecdf9-116">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="ecdf9-117">-LoadContent</span><span class="sxs-lookup"><span data-stu-id="ecdf9-117">-LoadContent</span></span>
<span data-ttu-id="ecdf9-118">Określa tablicę względnych ścieżek dla zawartości na serwerze pochodzenia, którą publikuje polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ecdf9-118">Specifies an array of relative paths for the content on the origin server that this cmdlet publishes.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecdf9-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ecdf9-119">-PassThru</span></span>
<span data-ttu-id="ecdf9-120">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="ecdf9-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ecdf9-121">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="ecdf9-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecdf9-122">-Refilename</span><span class="sxs-lookup"><span data-stu-id="ecdf9-122">-ProfileName</span></span>
<span data-ttu-id="ecdf9-123">Określa nazwę profilu, do którego należy serwer pochodzenia.</span><span class="sxs-lookup"><span data-stu-id="ecdf9-123">Specifies the name of the profile to which the origin server belongs.</span></span>

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

### <span data-ttu-id="ecdf9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecdf9-124">-ResourceGroupName</span></span>
<span data-ttu-id="ecdf9-125">Określa nazwę grupy zasobów, do której należy serwer pochodzenia.</span><span class="sxs-lookup"><span data-stu-id="ecdf9-125">Specifies the name of the resource group to which the origin server belongs.</span></span>

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

### <span data-ttu-id="ecdf9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecdf9-126">CommonParameters</span></span>
<span data-ttu-id="ecdf9-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecdf9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecdf9-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ecdf9-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecdf9-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ecdf9-129">INPUTS</span></span>

### <span data-ttu-id="ecdf9-130">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="ecdf9-130">PSEndpoint</span></span>
<span data-ttu-id="ecdf9-131">Parametr "CdnEndpoint" akceptuje wartość typu "PSEndpoint" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="ecdf9-131">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="ecdf9-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ecdf9-132">OUTPUTS</span></span>

### <span data-ttu-id="ecdf9-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ecdf9-133">System.Boolean</span></span>

## <span data-ttu-id="ecdf9-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ecdf9-134">NOTES</span></span>

## <span data-ttu-id="ecdf9-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ecdf9-135">RELATED LINKS</span></span>

[<span data-ttu-id="ecdf9-136">Cofnięcie publikowania — AzureRmCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="ecdf9-136">Unpublish-AzureRmCdnEndpointContent</span></span>](./Unpublish-AzureRmCdnEndpointContent.md)


