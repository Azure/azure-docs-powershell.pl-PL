---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 3d406bf0dffb0ee250e1494fc05727d0a4c983ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552660"
---
# <span data-ttu-id="8c521-101">Remove-AzureRmServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8c521-101">Remove-AzureRmServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="8c521-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8c521-102">SYNOPSIS</span></span>
<span data-ttu-id="8c521-103">{{Wpisz w postaci streszczenia}}</span><span class="sxs-lookup"><span data-stu-id="8c521-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8c521-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8c521-104">SYNTAX</span></span>

```
Remove-AzureRmServiceEndpointPolicyDefinition [-Name <String>] -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c521-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8c521-105">DESCRIPTION</span></span>
<span data-ttu-id="8c521-106">Polecenie cmdlet **Remove-AzureRmServiceEndpointPolicy** usuwa zasadę punktu końcowego usługi.</span><span class="sxs-lookup"><span data-stu-id="8c521-106">The **Remove-AzureRmServiceEndpointPolicy** cmdlet removes a service endpoint policy.</span></span>

## <span data-ttu-id="8c521-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8c521-107">EXAMPLES</span></span>

### <span data-ttu-id="8c521-108">Przykład 1. usuwa zasadę punktu końcowego usługi przy użyciu nazwy</span><span class="sxs-lookup"><span data-stu-id="8c521-108">Example 1: Removes a service endpoint policy using name</span></span>
```
Remove-AzureRmServiceEndpointPolicyDefinition -Name "PolicyDef1"
```

<span data-ttu-id="8c521-109">To polecenie usuwa zasadę punktu końcowego usługi o nazwie PolicyDef1</span><span class="sxs-lookup"><span data-stu-id="8c521-109">This command removes a service endpoint policy with name PolicyDef1</span></span>

## <span data-ttu-id="8c521-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8c521-110">PARAMETERS</span></span>

### <span data-ttu-id="8c521-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c521-111">-DefaultProfile</span></span>
<span data-ttu-id="8c521-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8c521-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c521-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8c521-113">-Name</span></span>
<span data-ttu-id="8c521-114">Nazwa definicji punktu końcowego usługi</span><span class="sxs-lookup"><span data-stu-id="8c521-114">The name of the service endpoint definition</span></span>

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

### <span data-ttu-id="8c521-115">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="8c521-115">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="8c521-116">ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="8c521-116">The ServiceEndpointPolicy</span></span>

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

### <span data-ttu-id="8c521-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c521-117">CommonParameters</span></span>
<span data-ttu-id="8c521-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c521-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="8c521-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c521-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c521-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8c521-120">INPUTS</span></span>

### <span data-ttu-id="8c521-121">Microsoft. Azure. Commands. Network. models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="8c521-121">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="8c521-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8c521-122">OUTPUTS</span></span>

### <span data-ttu-id="8c521-123">Microsoft. Azure. Commands. Network. models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="8c521-123">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="8c521-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8c521-124">NOTES</span></span>

## <span data-ttu-id="8c521-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8c521-125">RELATED LINKS</span></span>
