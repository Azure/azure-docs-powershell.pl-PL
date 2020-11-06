---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespace.md
ms.openlocfilehash: d65e19cb86a2ba850311fa937e64432ee8588d02
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551735"
---
# <span data-ttu-id="fc010-101">Get-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="fc010-101">Get-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="fc010-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fc010-102">SYNOPSIS</span></span>
<span data-ttu-id="fc010-103">Pobiera szczegóły obszaru nazw koncentratorów zdarzeń lub pobiera listę wszystkich obszarów nazw koncentratorów zdarzeń w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="fc010-103">Gets the details of an Event Hubs namespace, or gets a list of all Event Hubs namespaces in the current Azure subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc010-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fc010-104">SYNTAX</span></span>

```
Get-AzureRmEventHubNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc010-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fc010-105">DESCRIPTION</span></span>
<span data-ttu-id="fc010-106">Polecenie cmdlet Get-AzureRmEventHubNamespace pobiera szczegóły określonego obszaru nazw koncentratora zdarzeń lub listę wszystkich obszarów nazw koncentratorów zdarzeń w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="fc010-106">The Get-AzureRmEventHubNamespace cmdlet gets either the details of a specified Event Hubs namespace, or a list of all Event Hubs namespaces in the current Azure subscription.</span></span>
<span data-ttu-id="fc010-107">Jeśli podano nazwę obszaru nazw, zostanie zwrócona wartość szczegółów pojedynczego obszaru nazw koncentratorów zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="fc010-107">If the namespace name is provided, the details of a single Event Hubs namespace is returned.</span></span>
<span data-ttu-id="fc010-108">Jeśli nie podano nazwy obszaru nazw, zostanie zwrócona lista obszarów nazw.</span><span class="sxs-lookup"><span data-stu-id="fc010-108">If the namespace name is not provided, a list of namespaces is returned.</span></span>

## <span data-ttu-id="fc010-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fc010-109">EXAMPLES</span></span>

### <span data-ttu-id="fc010-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fc010-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="fc010-111">Umożliwia wyświetlenie szczegółów obszaru nazw Hubs (obszar_nazwname) \` \` w grupie zasobów \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="fc010-111">Gets the details of the Event Hubs namespace \`MyNamespaceName\` in the resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="fc010-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fc010-112">PARAMETERS</span></span>

### <span data-ttu-id="fc010-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc010-113">-DefaultProfile</span></span>
<span data-ttu-id="fc010-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fc010-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc010-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fc010-115">-Name</span></span>
<span data-ttu-id="fc010-116">Nazwa obszaru nazw EventHub</span><span class="sxs-lookup"><span data-stu-id="fc010-116">EventHub Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc010-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc010-117">-ResourceGroupName</span></span>
<span data-ttu-id="fc010-118">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="fc010-118">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc010-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc010-119">CommonParameters</span></span>
<span data-ttu-id="fc010-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc010-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="fc010-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc010-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc010-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fc010-122">INPUTS</span></span>

### <span data-ttu-id="fc010-123">System. String</span><span class="sxs-lookup"><span data-stu-id="fc010-123">System.String</span></span>


## <span data-ttu-id="fc010-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fc010-124">OUTPUTS</span></span>

### <span data-ttu-id="fc010-125">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. EventHub. modele. PSNamespaceAttributes, Microsoft. Azure. Commands. EventHub, Version = 0.5.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="fc010-125">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes, Microsoft.Azure.Commands.EventHub, Version=0.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>


## <span data-ttu-id="fc010-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fc010-126">NOTES</span></span>

## <span data-ttu-id="fc010-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fc010-127">RELATED LINKS</span></span>
