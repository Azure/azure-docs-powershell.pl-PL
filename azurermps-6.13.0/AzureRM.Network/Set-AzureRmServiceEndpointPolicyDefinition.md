---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 1348eff2e4a2ac755ac0f425ddb29816438199b7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717384"
---
# <span data-ttu-id="e7765-101">Set-AzureRmServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e7765-101">Set-AzureRmServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="e7765-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e7765-102">SYNOPSIS</span></span>
<span data-ttu-id="e7765-103">{{Wpisz w postaci streszczenia}}</span><span class="sxs-lookup"><span data-stu-id="e7765-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7765-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e7765-104">SYNTAX</span></span>

```
Set-AzureRmServiceEndpointPolicyDefinition -Name <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-Description <String>] [-ServiceResource <System.Collections.Generic.List`1[System.String]>]
 [-Service <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7765-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e7765-105">DESCRIPTION</span></span>
<span data-ttu-id="e7765-106">Polecenie cmdlet **Set-AzureRmServiceEndpointPolicyDefinition** Tworzenie definicji zasad punktu końcowego usługi.</span><span class="sxs-lookup"><span data-stu-id="e7765-106">The **Set-AzureRmServiceEndpointPolicyDefinition** cmdlet create a service endpoint policy definition.</span></span>

## <span data-ttu-id="e7765-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e7765-107">EXAMPLES</span></span>

### <span data-ttu-id="e7765-108">Przykład 1: aktualizowanie definicji zasad punktu końcowego usługi w zasadzie punktu końcowego usługi</span><span class="sxs-lookup"><span data-stu-id="e7765-108">Example 1: Updates a service endpoint policy definition in a service endpoint policy</span></span>
```
$serviceEndpointPolicy = Set-AzureRmServiceEndpointPolicyDefinition -Name "Policydef1" -ServiceEndpointPolicy $serviceEndpointPolicy
```

<span data-ttu-id="e7765-109">To polecenie aktualizuje definicję zasad punktu końcowego usługi o nazwie Policydef1 w zasadach punktu końcowego usługi zdefiniowanych przez $ServiceEndpointPolicy obiektu.</span><span class="sxs-lookup"><span data-stu-id="e7765-109">This command updates a service endpoint policy definition named Policydef1 in the service endpoint policy defined by the object $ServiceEndpointPolicy.</span></span>

## <span data-ttu-id="e7765-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e7765-110">PARAMETERS</span></span>

### <span data-ttu-id="e7765-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7765-111">-DefaultProfile</span></span>
<span data-ttu-id="e7765-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e7765-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7765-113">— Opis</span><span class="sxs-lookup"><span data-stu-id="e7765-113">-Description</span></span>
<span data-ttu-id="e7765-114">Opis definicji</span><span class="sxs-lookup"><span data-stu-id="e7765-114">The description of the definition</span></span>

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

### <span data-ttu-id="e7765-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e7765-115">-Name</span></span>
<span data-ttu-id="e7765-116">Nazwa reguły</span><span class="sxs-lookup"><span data-stu-id="e7765-116">The name of the rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7765-117">-Service</span><span class="sxs-lookup"><span data-stu-id="e7765-117">-Service</span></span>
<span data-ttu-id="e7765-118">Nazwa usługi</span><span class="sxs-lookup"><span data-stu-id="e7765-118">Name of the service</span></span>

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

### <span data-ttu-id="e7765-119">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="e7765-119">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="e7765-120">NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e7765-120">The NetworkSecurityGroup</span></span>

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

### <span data-ttu-id="e7765-121">-Serviceresource</span><span class="sxs-lookup"><span data-stu-id="e7765-121">-ServiceResource</span></span>
<span data-ttu-id="e7765-122">Lista zasobów usług</span><span class="sxs-lookup"><span data-stu-id="e7765-122">List of service resources</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7765-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7765-123">CommonParameters</span></span>
<span data-ttu-id="e7765-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7765-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="e7765-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7765-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7765-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e7765-126">INPUTS</span></span>

### <span data-ttu-id="e7765-127">Microsoft. Azure. Commands. Network. models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="e7765-127">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="e7765-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e7765-128">OUTPUTS</span></span>

### <span data-ttu-id="e7765-129">Microsoft. Azure. Commands. Network. models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="e7765-129">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="e7765-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e7765-130">NOTES</span></span>

## <span data-ttu-id="e7765-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e7765-131">RELATED LINKS</span></span>
