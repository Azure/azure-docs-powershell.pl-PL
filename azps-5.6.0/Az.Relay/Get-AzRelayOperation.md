---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/powershell/module/az.relay/get-azrelayoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayOperation.md
ms.openlocfilehash: 72f9e3290af5aad665213c1ffdebf5f3b2edcf92
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000602"
---
# <span data-ttu-id="9b95a-101">Get-AzRelayOperation</span><span class="sxs-lookup"><span data-stu-id="9b95a-101">Get-AzRelayOperation</span></span>

## <span data-ttu-id="9b95a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b95a-102">SYNOPSIS</span></span>
<span data-ttu-id="9b95a-103">Operacje przekazywania obsługiwane na liście</span><span class="sxs-lookup"><span data-stu-id="9b95a-103">List supported Relay Operations</span></span>

## <span data-ttu-id="9b95a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9b95a-104">SYNTAX</span></span>

```
Get-AzRelayOperation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b95a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="9b95a-105">DESCRIPTION</span></span>
<span data-ttu-id="9b95a-106">Polecenie **cmdlet Get-AzRelayOperation** wyświetla listę operacji obsługiwanych przez przekazywanie.</span><span class="sxs-lookup"><span data-stu-id="9b95a-106">The **Get-AzRelayOperation** cmdlet Lists the Relay supported Operations.</span></span>

## <span data-ttu-id="9b95a-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9b95a-107">EXAMPLES</span></span>

### <span data-ttu-id="9b95a-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9b95a-108">Example 1</span></span>
```
PS C:\> Get-AzRelayOperation

Name                                                                            Display
----                                                                            -------
Microsoft.Relay/checkNamespaceAvailability/action                               Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/register/action                                                 Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/write                                                Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/read                                                 Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/Delete                                               Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/authorizationRules/write                             Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/authorizationRules/delete                            Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/authorizationRules/listkeys/action                   Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/HybridConnections/write                              Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/HybridConnections/read                               Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/HybridConnections/Delete                             Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/HybridConnections/authorizationRules/write           Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/HybridConnections/authorizationRules/delete          Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/HybridConnections/authorizationRules/listkeys/action Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/WcfRelays/write                                      Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/WcfRelays/read                                       Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/WcfRelays/Delete                                     Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/WcfRelays/authorizationRules/write                   Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/WcfRelays/authorizationRules/delete                  Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/WcfRelays/authorizationRules/listkeys/action         Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
```

<span data-ttu-id="9b95a-109">Operacje obsługiwane przez przekazywanie list</span><span class="sxs-lookup"><span data-stu-id="9b95a-109">Lists Relay supported operations</span></span>

## <span data-ttu-id="9b95a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9b95a-110">PARAMETERS</span></span>

### <span data-ttu-id="9b95a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b95a-111">-DefaultProfile</span></span>
<span data-ttu-id="9b95a-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9b95a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b95a-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b95a-113">CommonParameters</span></span>
<span data-ttu-id="9b95a-114">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b95a-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b95a-115">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b95a-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b95a-116">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9b95a-116">INPUTS</span></span>

### <span data-ttu-id="9b95a-117">Brak</span><span class="sxs-lookup"><span data-stu-id="9b95a-117">None</span></span>

## <span data-ttu-id="9b95a-118">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9b95a-118">OUTPUTS</span></span>

### <span data-ttu-id="9b95a-119">Microsoft.Azure.Commands.Relay.Models.PSOperationAttributes</span><span class="sxs-lookup"><span data-stu-id="9b95a-119">Microsoft.Azure.Commands.Relay.Models.PSOperationAttributes</span></span>

## <span data-ttu-id="9b95a-120">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9b95a-120">NOTES</span></span>

## <span data-ttu-id="9b95a-121">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9b95a-121">RELATED LINKS</span></span>
