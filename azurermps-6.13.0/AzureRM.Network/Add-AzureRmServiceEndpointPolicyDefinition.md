---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmServiceEndpointPolicyDefinition.md
ms.openlocfilehash: ac58450295e0e2d988c12c308c0210b38ad71b4c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718299"
---
# <span data-ttu-id="7f3bd-101">Add-AzureRmServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="7f3bd-101">Add-AzureRmServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="7f3bd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7f3bd-102">SYNOPSIS</span></span>
<span data-ttu-id="7f3bd-103">Dodaje definicję zasad punktu końcowego usługi do określonych zasad.</span><span class="sxs-lookup"><span data-stu-id="7f3bd-103">Adds a service endpoint policy definition to a specified policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f3bd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7f3bd-104">SYNTAX</span></span>

```
Add-AzureRmServiceEndpointPolicyDefinition -Name <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-Description <String>] [-ServiceResource <System.Collections.Generic.List`1[System.String]>]
 [-Service <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f3bd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7f3bd-105">DESCRIPTION</span></span>
<span data-ttu-id="7f3bd-106">Polecenie cmdlet **Add-AzureRmServiceEndpointPolicyDefinition** umożliwia dodanie definicji zasad punktu końcowego usługi do zasad.</span><span class="sxs-lookup"><span data-stu-id="7f3bd-106">The **Add-AzureRmServiceEndpointPolicyDefinition** cmdlet add a service endpoint policy definition to the policy.</span></span>

## <span data-ttu-id="7f3bd-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7f3bd-107">EXAMPLES</span></span>

### <span data-ttu-id="7f3bd-108">Przykład 1: aktualizowanie definicji zasad punktu końcowego usługi w zasadzie punktu końcowego usługi</span><span class="sxs-lookup"><span data-stu-id="7f3bd-108">Example 1: Updates a service endpoint policy definition in a service endpoint policy</span></span>
```
$policydef= New-AzureRmServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ResourceGroupName "ResourceGroup01" -Service "Microsoft.Storage" -ServiceResources "subscriptions/sub1" -Description "New Definition"
```

<span data-ttu-id="7f3bd-109">To polecenie zaktualizowała definicję zasad punktu końcowego usługi o nazwie ServiceEndpointPolicyDefinition1, usłudze Microsoft. Storage, abonamentach/sub1 i opisie "Nowa definicja" należącym do grupy zasobów o nazwie ResourceGroup01 i przechowując ją w zmiennej $policydef.</span><span class="sxs-lookup"><span data-stu-id="7f3bd-109">This command updated the service endpoint policy definition with name ServiceEndpointPolicyDefinition1,  service Microsoft.Storage, service resources subscriptions/sub1 and description "New Definition" that belongs to the resource group named ResourceGroup01 and stores it in the $policydef variable.</span></span>

## <span data-ttu-id="7f3bd-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7f3bd-110">PARAMETERS</span></span>

### <span data-ttu-id="7f3bd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f3bd-111">-DefaultProfile</span></span>
<span data-ttu-id="7f3bd-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7f3bd-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f3bd-113">— Opis</span><span class="sxs-lookup"><span data-stu-id="7f3bd-113">-Description</span></span>
<span data-ttu-id="7f3bd-114">Opis definicji</span><span class="sxs-lookup"><span data-stu-id="7f3bd-114">The description of the definition</span></span>

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

### <span data-ttu-id="7f3bd-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7f3bd-115">-Name</span></span>
<span data-ttu-id="7f3bd-116">Nazwa definicji zasad punktu końcowego usługi</span><span class="sxs-lookup"><span data-stu-id="7f3bd-116">The name of the service endpoint policy definition</span></span>

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

### <span data-ttu-id="7f3bd-117">-Service</span><span class="sxs-lookup"><span data-stu-id="7f3bd-117">-Service</span></span>
<span data-ttu-id="7f3bd-118">Nazwa usługi</span><span class="sxs-lookup"><span data-stu-id="7f3bd-118">Name of the service</span></span>

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

### <span data-ttu-id="7f3bd-119">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="7f3bd-119">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="7f3bd-120">ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="7f3bd-120">The ServiceEndpointPolicy</span></span>

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

### <span data-ttu-id="7f3bd-121">-Serviceresource</span><span class="sxs-lookup"><span data-stu-id="7f3bd-121">-ServiceResource</span></span>
<span data-ttu-id="7f3bd-122">Lista zasobów usług</span><span class="sxs-lookup"><span data-stu-id="7f3bd-122">List of service resources</span></span>

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

### <span data-ttu-id="7f3bd-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f3bd-123">CommonParameters</span></span>
<span data-ttu-id="7f3bd-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f3bd-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="7f3bd-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f3bd-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f3bd-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7f3bd-126">INPUTS</span></span>

### <span data-ttu-id="7f3bd-127">Microsoft. Azure. Commands. Network. models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="7f3bd-127">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="7f3bd-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7f3bd-128">OUTPUTS</span></span>

### <span data-ttu-id="7f3bd-129">Microsoft. Azure. Commands. Network. models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="7f3bd-129">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="7f3bd-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7f3bd-130">NOTES</span></span>

## <span data-ttu-id="7f3bd-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7f3bd-131">RELATED LINKS</span></span>
