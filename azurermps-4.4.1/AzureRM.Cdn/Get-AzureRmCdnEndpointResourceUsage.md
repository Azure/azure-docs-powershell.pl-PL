---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpointResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpointResourceUsage.md
ms.openlocfilehash: f9d9d307959d53748afe7219ccb4cbce631c5b1e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554212"
---
# <span data-ttu-id="8f027-101">Get-AzureRmCdnEndpointResourceUsage</span><span class="sxs-lookup"><span data-stu-id="8f027-101">Get-AzureRmCdnEndpointResourceUsage</span></span>

## <span data-ttu-id="8f027-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8f027-102">SYNOPSIS</span></span>
<span data-ttu-id="8f027-103">{{Wpisz w postaci streszczenia}}</span><span class="sxs-lookup"><span data-stu-id="8f027-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f027-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8f027-104">SYNTAX</span></span>

### <span data-ttu-id="8f027-105">Parametr ustawiony dla parametrów pól (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="8f027-105">Parameter Set for fields parameters (Default)</span></span>
```
Get-AzureRmCdnEndpointResourceUsage [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f027-106">Zestaw parametrów dla parametrów obiektu</span><span class="sxs-lookup"><span data-stu-id="8f027-106">Parameter Set for object parameters</span></span>
```
Get-AzureRmCdnEndpointResourceUsage [-EndpointName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f027-107">Opis</span><span class="sxs-lookup"><span data-stu-id="8f027-107">DESCRIPTION</span></span>
<span data-ttu-id="8f027-108">{{Wpisz opis}}</span><span class="sxs-lookup"><span data-stu-id="8f027-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="8f027-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8f027-109">EXAMPLES</span></span>

### <span data-ttu-id="8f027-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8f027-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="8f027-111">{{Dodaj opis przykładu}}</span><span class="sxs-lookup"><span data-stu-id="8f027-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="8f027-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8f027-112">PARAMETERS</span></span>

### <span data-ttu-id="8f027-113">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="8f027-113">-CdnEndpoint</span></span>
<span data-ttu-id="8f027-114">Obiekt punktu końcowego sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="8f027-114">The CDN endpoint object.</span></span>

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

### <span data-ttu-id="8f027-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="8f027-115">-EndpointName</span></span>
<span data-ttu-id="8f027-116">Nazwa punktu końcowego usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="8f027-116">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="8f027-117">-Refilename</span><span class="sxs-lookup"><span data-stu-id="8f027-117">-ProfileName</span></span>
<span data-ttu-id="8f027-118">Nazwa profilu usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="8f027-118">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="8f027-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f027-119">-ResourceGroupName</span></span>
<span data-ttu-id="8f027-120">Grupa zasobów profilu usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="8f027-120">The resource group of the Azure CDN Profile.</span></span>

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

### <span data-ttu-id="8f027-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f027-121">-DefaultProfile</span></span>
<span data-ttu-id="8f027-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8f027-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f027-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f027-123">CommonParameters</span></span>
<span data-ttu-id="8f027-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f027-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f027-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f027-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f027-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8f027-126">INPUTS</span></span>

### <span data-ttu-id="8f027-127">Microsoft. Azure. Commands. CDN. models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="8f027-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="8f027-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8f027-128">OUTPUTS</span></span>

### <span data-ttu-id="8f027-129">Microsoft. Azure. Commands. CDN. modele. PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="8f027-129">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="8f027-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8f027-130">NOTES</span></span>

## <span data-ttu-id="8f027-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8f027-131">RELATED LINKS</span></span>

