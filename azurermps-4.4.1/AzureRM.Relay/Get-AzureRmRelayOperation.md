---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayOperation.md
ms.openlocfilehash: 8cd5e0a74f26f4744e2c086b4d689a8d06ebf5b7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716884"
---
# <span data-ttu-id="081ac-101">Get-AzureRmRelayOperation</span><span class="sxs-lookup"><span data-stu-id="081ac-101">Get-AzureRmRelayOperation</span></span>

## <span data-ttu-id="081ac-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="081ac-102">SYNOPSIS</span></span>
<span data-ttu-id="081ac-103">Lista obsługiwanych operacji przekazywania</span><span class="sxs-lookup"><span data-stu-id="081ac-103">List supported Relay Operations</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="081ac-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="081ac-104">SYNTAX</span></span>

```
Get-AzureRmRelayOperation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="081ac-105">Opis</span><span class="sxs-lookup"><span data-stu-id="081ac-105">DESCRIPTION</span></span>
<span data-ttu-id="081ac-106">Polecenie cmdlet **Get-AzureRmRelayOperation** zawiera listę obsługiwanych operacji przekazywania.</span><span class="sxs-lookup"><span data-stu-id="081ac-106">The **Get-AzureRmRelayOperation** cmdlet Lists the Relay supported Operations.</span></span>

## <span data-ttu-id="081ac-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="081ac-107">EXAMPLES</span></span>

### <span data-ttu-id="081ac-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="081ac-108">Example 1</span></span>
```
PS C:\> Get-AzureRmRelayOperation
```

<span data-ttu-id="081ac-109">Lista obsługiwanych operacji przekaźnika</span><span class="sxs-lookup"><span data-stu-id="081ac-109">Lists Relay supported operations</span></span>

## <span data-ttu-id="081ac-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="081ac-110">PARAMETERS</span></span>

### <span data-ttu-id="081ac-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="081ac-111">-DefaultProfile</span></span>
<span data-ttu-id="081ac-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="081ac-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="081ac-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="081ac-113">CommonParameters</span></span>
<span data-ttu-id="081ac-114">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="081ac-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="081ac-115">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="081ac-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="081ac-116">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="081ac-116">INPUTS</span></span>

### <span data-ttu-id="081ac-117">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="081ac-117">None</span></span>

## <span data-ttu-id="081ac-118">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="081ac-118">OUTPUTS</span></span>

### <span data-ttu-id="081ac-119">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. Relay. modele. OperationAttributes, Microsoft. Azure. Commands</span><span class="sxs-lookup"><span data-stu-id="081ac-119">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Relay.Models.OperationAttributes, Microsoft.Azure.Commands.Relay, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="081ac-120">Wyświetlanie nazwy</span><span class="sxs-lookup"><span data-stu-id="081ac-120">Name                                                                            Display</span></span>
----                                                                            -------
<span data-ttu-id="081ac-121">Microsoft.Relay/checkNamespaceAvailability/action Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/register/action Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/write Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/read Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/Delete Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/authorizationRules/write Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/authorizationRules/delete Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/authorizationRules/listkeys/action Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/HybridConnections/write Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/HybridConnections/read Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/HybridConnections/Delete Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/HybridConnections/authorizationRules/write Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/HybridConnections/authorizationRules/delete Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/HybridConnections/authorizationRules/listkeys/action Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/WcfRelays/write Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/WcfRelays/read Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/WcfRelays/Delete Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/WcfRelays/authorizationRules/write Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/WcfRelays/authorizationRules/delete Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/WcfRelays/authorizationRules/listkeys/action Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes</span><span class="sxs-lookup"><span data-stu-id="081ac-121">Microsoft.Relay/checkNamespaceAvailability/action                               Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/register/action                                                 Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/write                                                Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/read                                                 Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/Delete                                               Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/authorizationRules/write                             Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/authorizationRules/delete                            Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/authorizationRules/listkeys/action                   Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/HybridConnections/write                              Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/HybridConnections/read                               Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/HybridConnections/Delete                             Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/HybridConnections/authorizationRules/write           Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/HybridConnections/authorizationRules/delete          Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/HybridConnections/authorizationRules/listkeys/action Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/WcfRelays/write                                      Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/WcfRelays/read                                       Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/WcfRelays/Delete                                     Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/WcfRelays/authorizationRules/write                   Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/WcfRelays/authorizationRules/delete                  Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/WcfRelays/authorizationRules/listkeys/action         Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes</span></span>

## <span data-ttu-id="081ac-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="081ac-122">NOTES</span></span>

## <span data-ttu-id="081ac-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="081ac-123">RELATED LINKS</span></span>
