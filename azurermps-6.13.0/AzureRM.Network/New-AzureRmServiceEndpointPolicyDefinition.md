---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 12d809ad4c1df021891ab5acf384415d64aa08a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551152"
---
# <span data-ttu-id="70a1e-101">New-AzureRmServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="70a1e-101">New-AzureRmServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="70a1e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="70a1e-102">SYNOPSIS</span></span>
<span data-ttu-id="70a1e-103">{{Wpisz w postaci streszczenia}}</span><span class="sxs-lookup"><span data-stu-id="70a1e-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="70a1e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="70a1e-104">SYNTAX</span></span>

```
New-AzureRmServiceEndpointPolicyDefinition -Name <String> [-Description <String>]
 [-ServiceResource <System.Collections.Generic.List`1[System.String]>] [-Service <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="70a1e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="70a1e-105">DESCRIPTION</span></span>
<span data-ttu-id="70a1e-106">Polecenie cmdlet **New-AzureRmServiceEndpointPolicyDefinition** umożliwia utworzenie definicji zasad punktu końcowego usługi.</span><span class="sxs-lookup"><span data-stu-id="70a1e-106">The **New-AzureRmServiceEndpointPolicyDefinition** cmdlet create a service endpoint policy definition.</span></span>

## <span data-ttu-id="70a1e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="70a1e-107">EXAMPLES</span></span>

### <span data-ttu-id="70a1e-108">Przykład 1. Tworzenie zasad punktu końcowego usługi</span><span class="sxs-lookup"><span data-stu-id="70a1e-108">Example 1: Creates a service endpoint policy</span></span>
```
$policydef= New-AzureRmServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ResourceGroupName "ResourceGroup01" -Service "Microsoft.Storage" -ServiceResources "subscriptions/sub1" -Description "New Definition"
```

<span data-ttu-id="70a1e-109">To polecenie tworzy definicję zasad punktu końcowego usługi o nazwie ServiceEndpointPolicyDefinition1, usłudze Microsoft. Storage, abonamentach/sub1 i opisie "Nowa definicja" należącym do grupy zasobów o nazwie ResourceGroup01 i przechowując ją w zmiennej $policydef.</span><span class="sxs-lookup"><span data-stu-id="70a1e-109">This command creates the service endpoint policy definition with name ServiceEndpointPolicyDefinition1,  service Microsoft.Storage, service resources subscriptions/sub1 and description "New Definition" that belongs to the resource group named ResourceGroup01 and stores it in the $policydef variable.</span></span>

## <span data-ttu-id="70a1e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="70a1e-110">PARAMETERS</span></span>

### <span data-ttu-id="70a1e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70a1e-111">-DefaultProfile</span></span>
<span data-ttu-id="70a1e-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="70a1e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70a1e-113">— Opis</span><span class="sxs-lookup"><span data-stu-id="70a1e-113">-Description</span></span>
<span data-ttu-id="70a1e-114">Opis definicji</span><span class="sxs-lookup"><span data-stu-id="70a1e-114">The description of the definition</span></span>

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

### <span data-ttu-id="70a1e-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="70a1e-115">-Name</span></span>
<span data-ttu-id="70a1e-116">Nazwa zasad punktu końcowego usługi</span><span class="sxs-lookup"><span data-stu-id="70a1e-116">The name of the service endpoint policy</span></span>

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

### <span data-ttu-id="70a1e-117">-Service</span><span class="sxs-lookup"><span data-stu-id="70a1e-117">-Service</span></span>
<span data-ttu-id="70a1e-118">Nazwa usługi</span><span class="sxs-lookup"><span data-stu-id="70a1e-118">Name of the service</span></span>

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

### <span data-ttu-id="70a1e-119">-Serviceresource</span><span class="sxs-lookup"><span data-stu-id="70a1e-119">-ServiceResource</span></span>
<span data-ttu-id="70a1e-120">Lista zasobów usług</span><span class="sxs-lookup"><span data-stu-id="70a1e-120">List of service resources</span></span>

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

### <span data-ttu-id="70a1e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70a1e-121">CommonParameters</span></span>
<span data-ttu-id="70a1e-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70a1e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="70a1e-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70a1e-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70a1e-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="70a1e-124">INPUTS</span></span>

### <span data-ttu-id="70a1e-125">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="70a1e-125">None</span></span>


## <span data-ttu-id="70a1e-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="70a1e-126">OUTPUTS</span></span>

### <span data-ttu-id="70a1e-127">Microsoft. Azure. Commands. Network. models. PSServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="70a1e-127">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span></span>


## <span data-ttu-id="70a1e-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="70a1e-128">NOTES</span></span>

## <span data-ttu-id="70a1e-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="70a1e-129">RELATED LINKS</span></span>
