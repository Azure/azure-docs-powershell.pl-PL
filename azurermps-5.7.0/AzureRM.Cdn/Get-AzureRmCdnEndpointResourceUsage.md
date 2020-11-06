---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnendpointresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpointResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpointResourceUsage.md
ms.openlocfilehash: 82daa7f202dce698a84d17292a199fbd8f85bca5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553031"
---
# <span data-ttu-id="d0b94-101">Get-AzureRmCdnEndpointResourceUsage</span><span class="sxs-lookup"><span data-stu-id="d0b94-101">Get-AzureRmCdnEndpointResourceUsage</span></span>

## <span data-ttu-id="d0b94-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d0b94-102">SYNOPSIS</span></span>
<span data-ttu-id="d0b94-103">{{Wpisz w postaci streszczenia}}</span><span class="sxs-lookup"><span data-stu-id="d0b94-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d0b94-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d0b94-104">SYNTAX</span></span>

### <span data-ttu-id="d0b94-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d0b94-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzureRmCdnEndpointResourceUsage [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d0b94-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0b94-106">ByObjectParameterSet</span></span>
```
Get-AzureRmCdnEndpointResourceUsage [-EndpointName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d0b94-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d0b94-107">DESCRIPTION</span></span>
<span data-ttu-id="d0b94-108">{{Wpisz opis}}</span><span class="sxs-lookup"><span data-stu-id="d0b94-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="d0b94-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d0b94-109">EXAMPLES</span></span>

### <span data-ttu-id="d0b94-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d0b94-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="d0b94-111">{{Dodaj opis przykładu}}</span><span class="sxs-lookup"><span data-stu-id="d0b94-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="d0b94-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d0b94-112">PARAMETERS</span></span>

### <span data-ttu-id="d0b94-113">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="d0b94-113">-CdnEndpoint</span></span>
<span data-ttu-id="d0b94-114">Obiekt punktu końcowego sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="d0b94-114">The CDN endpoint object.</span></span>

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

### <span data-ttu-id="d0b94-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0b94-115">-DefaultProfile</span></span>
<span data-ttu-id="d0b94-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="d0b94-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d0b94-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="d0b94-117">-EndpointName</span></span>
<span data-ttu-id="d0b94-118">Nazwa punktu końcowego usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="d0b94-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="d0b94-119">-Refilename</span><span class="sxs-lookup"><span data-stu-id="d0b94-119">-ProfileName</span></span>
<span data-ttu-id="d0b94-120">Nazwa profilu usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="d0b94-120">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="d0b94-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0b94-121">-ResourceGroupName</span></span>
<span data-ttu-id="d0b94-122">Grupa zasobów profilu usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="d0b94-122">The resource group of the Azure CDN Profile.</span></span>

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

### <span data-ttu-id="d0b94-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0b94-123">CommonParameters</span></span>
<span data-ttu-id="d0b94-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0b94-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0b94-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0b94-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0b94-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d0b94-126">INPUTS</span></span>

### <span data-ttu-id="d0b94-127">Microsoft. Azure. Commands. CDN. models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="d0b94-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="d0b94-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d0b94-128">OUTPUTS</span></span>

### <span data-ttu-id="d0b94-129">Microsoft. Azure. Commands. CDN. modele. PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="d0b94-129">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="d0b94-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d0b94-130">NOTES</span></span>

## <span data-ttu-id="d0b94-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d0b94-131">RELATED LINKS</span></span>

