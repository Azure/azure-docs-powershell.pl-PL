---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: AFDBE48E-63B0-4A9E-9825-5246081AA129
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Publish-AzureRmCdnEndpointContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Publish-AzureRmCdnEndpointContent.md
ms.openlocfilehash: 1df36c7816894f8ccfc642eac307a84b485ba7ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550060"
---
# <span data-ttu-id="dd6f7-101">Publish-AzureRmCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="dd6f7-101">Publish-AzureRmCdnEndpointContent</span></span>

## <span data-ttu-id="dd6f7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dd6f7-102">SYNOPSIS</span></span>
<span data-ttu-id="dd6f7-103">Ładuje zawartość do punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="dd6f7-103">Loads content to an endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dd6f7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dd6f7-104">SYNTAX</span></span>

### <span data-ttu-id="dd6f7-105">Parametr ustawiony dla parametrów pól (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="dd6f7-105">Parameter Set for fields parameters (Default)</span></span>
```
Publish-AzureRmCdnEndpointContent -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -LoadContent <String[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dd6f7-106">Zestaw parametrów dla parametrów obiektu</span><span class="sxs-lookup"><span data-stu-id="dd6f7-106">Parameter Set for object parameters</span></span>
```
Publish-AzureRmCdnEndpointContent -CdnEndpoint <PSEndpoint> -LoadContent <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd6f7-107">Opis</span><span class="sxs-lookup"><span data-stu-id="dd6f7-107">DESCRIPTION</span></span>
<span data-ttu-id="dd6f7-108">Polecenie cmdlet **Publish-AzureRmCdnEndpointContent** ładuje zawartość z serwera źródłowego dla punktu końcowego sieci dostarczania zawartości Azure (CDN, Content Delivery Network).</span><span class="sxs-lookup"><span data-stu-id="dd6f7-108">The **Publish-AzureRmCdnEndpointContent** cmdlet loads content from an origin server for the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="dd6f7-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dd6f7-109">EXAMPLES</span></span>

## <span data-ttu-id="dd6f7-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dd6f7-110">PARAMETERS</span></span>

### <span data-ttu-id="dd6f7-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="dd6f7-111">-CdnEndpoint</span></span>
<span data-ttu-id="dd6f7-112">Sepcifies punkt końcowy sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="dd6f7-112">Sepcifies the CDN endpoint.</span></span>

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

### <span data-ttu-id="dd6f7-113">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="dd6f7-113">-EndpointName</span></span>
<span data-ttu-id="dd6f7-114">Określa nazwę punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="dd6f7-114">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="dd6f7-115">-LoadContent</span><span class="sxs-lookup"><span data-stu-id="dd6f7-115">-LoadContent</span></span>
<span data-ttu-id="dd6f7-116">Określa tablicę względnych ścieżek dla zawartości na serwerze pochodzenia, którą publikuje polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd6f7-116">Specifies an array of relative paths for the content on the origin server that this cmdlet publishes.</span></span>

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

### <span data-ttu-id="dd6f7-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dd6f7-117">-PassThru</span></span>
<span data-ttu-id="dd6f7-118">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="dd6f7-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="dd6f7-119">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="dd6f7-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="dd6f7-120">-Refilename</span><span class="sxs-lookup"><span data-stu-id="dd6f7-120">-ProfileName</span></span>
<span data-ttu-id="dd6f7-121">Określa nazwę profilu, do którego należy serwer pochodzenia.</span><span class="sxs-lookup"><span data-stu-id="dd6f7-121">Specifies the name of the profile to which the origin server belongs.</span></span>

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

### <span data-ttu-id="dd6f7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd6f7-122">-ResourceGroupName</span></span>
<span data-ttu-id="dd6f7-123">Określa nazwę grupy zasobów, do której należy serwer pochodzenia.</span><span class="sxs-lookup"><span data-stu-id="dd6f7-123">Specifies the name of the resource group to which the origin server belongs.</span></span>

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

### <span data-ttu-id="dd6f7-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd6f7-124">-DefaultProfile</span></span>
<span data-ttu-id="dd6f7-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="dd6f7-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd6f7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd6f7-126">CommonParameters</span></span>
<span data-ttu-id="dd6f7-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd6f7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd6f7-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd6f7-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd6f7-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dd6f7-129">INPUTS</span></span>

### <span data-ttu-id="dd6f7-130">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="dd6f7-130">PSEndpoint</span></span>
<span data-ttu-id="dd6f7-131">Parametr "CdnEndpoint" akceptuje wartość typu "PSEndpoint" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="dd6f7-131">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="dd6f7-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dd6f7-132">OUTPUTS</span></span>

### <span data-ttu-id="dd6f7-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dd6f7-133">System.Boolean</span></span>

## <span data-ttu-id="dd6f7-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dd6f7-134">NOTES</span></span>

## <span data-ttu-id="dd6f7-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dd6f7-135">RELATED LINKS</span></span>

[<span data-ttu-id="dd6f7-136">Cofnięcie publikowania — AzureRmCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="dd6f7-136">Unpublish-AzureRmCdnEndpointContent</span></span>](./Unpublish-AzureRmCdnEndpointContent.md)


