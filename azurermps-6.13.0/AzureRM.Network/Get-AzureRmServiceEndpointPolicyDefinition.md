---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 547b38fd30f09a305c63054b2f27d33db5ae6a86
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550276"
---
# <span data-ttu-id="00fdd-101">Get-AzureRmServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="00fdd-101">Get-AzureRmServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="00fdd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="00fdd-102">SYNOPSIS</span></span>
<span data-ttu-id="00fdd-103">{{Wpisz w postaci streszczenia}}</span><span class="sxs-lookup"><span data-stu-id="00fdd-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="00fdd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="00fdd-104">SYNTAX</span></span>

```
Get-AzureRmServiceEndpointPolicyDefinition [-Name <String>] -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00fdd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="00fdd-105">DESCRIPTION</span></span>
<span data-ttu-id="00fdd-106">Polecenie cmdlet **Get-AzureRmServiceEndpointPolicyDefinition** pobiera definicję zasad punktu końcowego usługi.</span><span class="sxs-lookup"><span data-stu-id="00fdd-106">The **Get-AzureRmServiceEndpointPolicyDefinition** cmdlet gets a service endpoint policy definition.</span></span>

## <span data-ttu-id="00fdd-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="00fdd-107">EXAMPLES</span></span>

### <span data-ttu-id="00fdd-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="00fdd-108">Example 1</span></span>
```
$policydef= Get-AzureRmServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ServiceEndpointPolicy $Policy
```

<span data-ttu-id="00fdd-109">To polecenie pobiera definicję zasad punktu końcowego usługi o nazwie ServiceEndpointPolicyDefinition1 w ServiceEndpointPolicy $Policy zapisuje ją w zmiennej $policydef.</span><span class="sxs-lookup"><span data-stu-id="00fdd-109">This command gets the service endpoint policy definition named ServiceEndpointPolicyDefinition1 in ServiceEndpointPolicy $Policy stores it in the $policydef variable.</span></span>

## <span data-ttu-id="00fdd-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="00fdd-110">PARAMETERS</span></span>

### <span data-ttu-id="00fdd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00fdd-111">-DefaultProfile</span></span>
<span data-ttu-id="00fdd-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="00fdd-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00fdd-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="00fdd-113">-Name</span></span>
<span data-ttu-id="00fdd-114">Nazwa definicji zasad punktu końcowego usługi</span><span class="sxs-lookup"><span data-stu-id="00fdd-114">The name of the service endpoint policy definition</span></span>

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

### <span data-ttu-id="00fdd-115">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="00fdd-115">-ResourceId</span></span>
<span data-ttu-id="00fdd-116">{{Opis ResourceId (wypełnienie)}}</span><span class="sxs-lookup"><span data-stu-id="00fdd-116">{{Fill ResourceId Description}}</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00fdd-117">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="00fdd-117">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="00fdd-118">Zasady punktu końcowego usługi</span><span class="sxs-lookup"><span data-stu-id="00fdd-118">The Service endpoint policy</span></span>

```yaml
Type: PSServiceEndpointPolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="00fdd-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="00fdd-119">-Confirm</span></span>
<span data-ttu-id="00fdd-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00fdd-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00fdd-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00fdd-121">-WhatIf</span></span>
<span data-ttu-id="00fdd-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00fdd-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="00fdd-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="00fdd-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00fdd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00fdd-124">CommonParameters</span></span>
<span data-ttu-id="00fdd-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00fdd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00fdd-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00fdd-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00fdd-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="00fdd-127">INPUTS</span></span>

### <span data-ttu-id="00fdd-128">Microsoft. Azure. Commands. Network. models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="00fdd-128">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="00fdd-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="00fdd-129">OUTPUTS</span></span>

### <span data-ttu-id="00fdd-130">Microsoft. Azure. Commands. Network. models. PSServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="00fdd-130">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="00fdd-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="00fdd-131">NOTES</span></span>

## <span data-ttu-id="00fdd-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="00fdd-132">RELATED LINKS</span></span>
