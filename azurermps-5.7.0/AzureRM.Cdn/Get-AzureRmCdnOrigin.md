---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 91919242-59ED-4938-A3A3-23A66F85FBC1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnOrigin.md
ms.openlocfilehash: b4800b77441a82fc0e9966be16f91c9d81a2214a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716641"
---
# <span data-ttu-id="ff4ed-101">Get-AzureRmCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="ff4ed-101">Get-AzureRmCdnOrigin</span></span>

## <span data-ttu-id="ff4ed-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ff4ed-102">SYNOPSIS</span></span>
<span data-ttu-id="ff4ed-103">Pobiera serwer pochodzenia sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="ff4ed-103">Gets a CDN origin server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff4ed-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ff4ed-104">SYNTAX</span></span>

### <span data-ttu-id="ff4ed-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ff4ed-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzureRmCdnOrigin [-OriginName <String>] -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ff4ed-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff4ed-106">ByObjectParameterSet</span></span>
```
Get-AzureRmCdnOrigin [-OriginName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ff4ed-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ff4ed-107">DESCRIPTION</span></span>
<span data-ttu-id="ff4ed-108">Polecenie cmdlet **Get-AzureRmCdnOrigin** pobiera serwer pochodzenia sieci dostarczania zawartości platformy Azure (CDN) i jego dane konfiguracyjne.</span><span class="sxs-lookup"><span data-stu-id="ff4ed-108">The **Get-AzureRmCdnOrigin** cmdlet gets an Azure Content Delivery Network (CDN) origin server and its configuration data.</span></span>

## <span data-ttu-id="ff4ed-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ff4ed-109">EXAMPLES</span></span>

## <span data-ttu-id="ff4ed-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ff4ed-110">PARAMETERS</span></span>

### <span data-ttu-id="ff4ed-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="ff4ed-111">-CdnEndpoint</span></span>
<span data-ttu-id="ff4ed-112">Określa obiekt punktu końcowego sieci CDN, do którego należy pochodzenie.</span><span class="sxs-lookup"><span data-stu-id="ff4ed-112">Specifies the CDN endpoint object to which the origin belongs.</span></span>

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

### <span data-ttu-id="ff4ed-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff4ed-113">-DefaultProfile</span></span>
<span data-ttu-id="ff4ed-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="ff4ed-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ff4ed-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="ff4ed-115">-EndpointName</span></span>
<span data-ttu-id="ff4ed-116">Określa nazwę punktu końcowego, do którego należy serwer pochodzenia.</span><span class="sxs-lookup"><span data-stu-id="ff4ed-116">Specifies the name of the endpoint to which the origin server belongs.</span></span>

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

### <span data-ttu-id="ff4ed-117">-Originname</span><span class="sxs-lookup"><span data-stu-id="ff4ed-117">-OriginName</span></span>
<span data-ttu-id="ff4ed-118">Określa nazwę serwera pochodzenia.</span><span class="sxs-lookup"><span data-stu-id="ff4ed-118">Specifies the name of the origin server.</span></span>

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

### <span data-ttu-id="ff4ed-119">-Refilename</span><span class="sxs-lookup"><span data-stu-id="ff4ed-119">-ProfileName</span></span>
<span data-ttu-id="ff4ed-120">Określa nazwę profilu, do którego należy serwer pochodzenia.</span><span class="sxs-lookup"><span data-stu-id="ff4ed-120">Specifies the name of the profile to which the origin server belongs.</span></span>

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

### <span data-ttu-id="ff4ed-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff4ed-121">-ResourceGroupName</span></span>
<span data-ttu-id="ff4ed-122">Określa nazwę grupy zasobów, do której należy serwer pochodzenia.</span><span class="sxs-lookup"><span data-stu-id="ff4ed-122">Specifies the name of the resource group to which the origin server belongs.</span></span>

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

### <span data-ttu-id="ff4ed-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff4ed-123">CommonParameters</span></span>
<span data-ttu-id="ff4ed-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff4ed-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff4ed-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff4ed-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff4ed-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ff4ed-126">INPUTS</span></span>

### <span data-ttu-id="ff4ed-127">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="ff4ed-127">PSEndpoint</span></span>
<span data-ttu-id="ff4ed-128">Parametr "CdnEndpoint" akceptuje wartość typu "PSEndpoint" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="ff4ed-128">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="ff4ed-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ff4ed-129">OUTPUTS</span></span>

###  
<span data-ttu-id="ff4ed-130">To polecenie cmdlet zwraca obiekt serwera źródłowego.</span><span class="sxs-lookup"><span data-stu-id="ff4ed-130">This cmdlet returns an origin server object.</span></span>

## <span data-ttu-id="ff4ed-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ff4ed-131">NOTES</span></span>

## <span data-ttu-id="ff4ed-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ff4ed-132">RELATED LINKS</span></span>

[<span data-ttu-id="ff4ed-133">Set-AzureRmCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="ff4ed-133">Set-AzureRmCdnOrigin</span></span>](./Set-AzureRmCdnOrigin.md)


