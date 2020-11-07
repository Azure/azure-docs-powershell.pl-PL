---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNamespace.md
ms.openlocfilehash: c39a85fe148461d5daa680a62b5cfd09b4a3e4e3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709812"
---
# <span data-ttu-id="b7b0c-101">Get-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="b7b0c-101">Get-AzEventHubNamespace</span></span>

## <span data-ttu-id="b7b0c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b7b0c-102">SYNOPSIS</span></span>
<span data-ttu-id="b7b0c-103">Pobiera szczegóły obszaru nazw koncentratorów zdarzeń lub pobiera listę wszystkich obszarów nazw koncentratorów zdarzeń w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b7b0c-103">Gets the details of an Event Hubs namespace, or gets a list of all Event Hubs namespaces in the current Azure subscription.</span></span>

## <span data-ttu-id="b7b0c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b7b0c-104">SYNTAX</span></span>

```
Get-AzEventHubNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7b0c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b7b0c-105">DESCRIPTION</span></span>
<span data-ttu-id="b7b0c-106">Polecenie cmdlet Get-AzEventHubNamespace pobiera szczegóły określonego obszaru nazw koncentratora zdarzeń lub listę wszystkich obszarów nazw koncentratorów zdarzeń w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b7b0c-106">The Get-AzEventHubNamespace cmdlet gets either the details of a specified Event Hubs namespace, or a list of all Event Hubs namespaces in the current Azure subscription.</span></span>
<span data-ttu-id="b7b0c-107">Jeśli podano nazwę obszaru nazw, zostanie zwrócona wartość szczegółów pojedynczego obszaru nazw koncentratorów zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="b7b0c-107">If the namespace name is provided, the details of a single Event Hubs namespace is returned.</span></span>
<span data-ttu-id="b7b0c-108">Jeśli nie podano nazwy obszaru nazw, zostanie zwrócona lista obszarów nazw.</span><span class="sxs-lookup"><span data-stu-id="b7b0c-108">If the namespace name is not provided, a list of namespaces is returned.</span></span>

## <span data-ttu-id="b7b0c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b7b0c-109">EXAMPLES</span></span>

### <span data-ttu-id="b7b0c-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b7b0c-110">Example 1</span></span>
```
PS C:\> Get-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="b7b0c-111">Pobiera szczegóły obszaru nazw NamespaceName \` \` w MyResourceGroupName grupy zasobów \` \` .</span><span class="sxs-lookup"><span data-stu-id="b7b0c-111">Gets the details of namespace \`MyNamespaceName\` in the resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="b7b0c-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b7b0c-112">PARAMETERS</span></span>

### <span data-ttu-id="b7b0c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7b0c-113">-DefaultProfile</span></span>
<span data-ttu-id="b7b0c-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b7b0c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7b0c-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b7b0c-115">-Name</span></span>
<span data-ttu-id="b7b0c-116">Nazwa obszaru nazw EventHub</span><span class="sxs-lookup"><span data-stu-id="b7b0c-116">EventHub Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7b0c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7b0c-117">-ResourceGroupName</span></span>
<span data-ttu-id="b7b0c-118">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="b7b0c-118">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7b0c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7b0c-119">CommonParameters</span></span>
<span data-ttu-id="b7b0c-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7b0c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7b0c-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7b0c-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7b0c-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b7b0c-122">INPUTS</span></span>

### <span data-ttu-id="b7b0c-123">System. String</span><span class="sxs-lookup"><span data-stu-id="b7b0c-123">System.String</span></span>

## <span data-ttu-id="b7b0c-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b7b0c-124">OUTPUTS</span></span>

### <span data-ttu-id="b7b0c-125">Microsoft. Azure. Commands. EventHub. modele. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="b7b0c-125">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="b7b0c-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b7b0c-126">NOTES</span></span>

## <span data-ttu-id="b7b0c-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b7b0c-127">RELATED LINKS</span></span>
