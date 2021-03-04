---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/get-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNamespace.md
ms.openlocfilehash: e550afd0b7f580c46b15bd8b6ac68b3b0ad1bc89
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957226"
---
# <span data-ttu-id="a33c9-101">Get-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="a33c9-101">Get-AzEventHubNamespace</span></span>

## <span data-ttu-id="a33c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a33c9-102">SYNOPSIS</span></span>
<span data-ttu-id="a33c9-103">Pobiera szczegóły przestrzeni nazw centrum zdarzeń lub pobiera listę wszystkich przestrzeni nazw centrum zdarzeń w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a33c9-103">Gets the details of an Event Hubs namespace, or gets a list of all Event Hubs namespaces in the current Azure subscription.</span></span>

## <span data-ttu-id="a33c9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a33c9-104">SYNTAX</span></span>

```
Get-AzEventHubNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a33c9-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="a33c9-105">DESCRIPTION</span></span>
<span data-ttu-id="a33c9-106">Polecenie Get-AzEventHubNamespace cmdlet pobiera szczegóły przestrzeni nazw określonej przestrzeni nazw centrum zdarzeń lub listę wszystkich przestrzeni nazw centrum zdarzeń w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a33c9-106">The Get-AzEventHubNamespace cmdlet gets either the details of a specified Event Hubs namespace, or a list of all Event Hubs namespaces in the current Azure subscription.</span></span>
<span data-ttu-id="a33c9-107">Jeśli podano nazwę przestrzeni nazw, zwracane są szczegóły przestrzeni nazw pojedynczych centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="a33c9-107">If the namespace name is provided, the details of a single Event Hubs namespace is returned.</span></span>
<span data-ttu-id="a33c9-108">Jeśli nazwa przestrzeni nazw nie jest podano, jest zwracana lista przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="a33c9-108">If the namespace name is not provided, a list of namespaces is returned.</span></span>

## <span data-ttu-id="a33c9-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a33c9-109">EXAMPLES</span></span>

### <span data-ttu-id="a33c9-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a33c9-110">Example 1</span></span>
```
PS C:\> Get-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName

Name                   : MyNamespaceName
Id                     : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName      : Default-EventHub-WestCentralUS
Location               : West US
Sku                    : Name : Standard , Capacity : 1 , Tier : Standard
Tags                   :
ProvisioningState      : Succeeded
Status                 : Active
CreatedAt              : 5/24/2019 12:47:27 AM
UpdatedAt              : 5/24/2019 12:48:14 AM
ServiceBusEndpoint     : #########
Enabled                : True
KafkaEnabled           : True
IsAutoInflateEnabled   : True
MaximumThroughputUnits : 10
```

<span data-ttu-id="a33c9-111">Pobiera szczegółowe informacje o przestrzeni nazw \` MyNamespaceName \` w grupie zasobów \` Nazwa_grupy_zasobów. \`</span><span class="sxs-lookup"><span data-stu-id="a33c9-111">Gets the details of namespace \`MyNamespaceName\` in the resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="a33c9-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a33c9-112">PARAMETERS</span></span>

### <span data-ttu-id="a33c9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a33c9-113">-DefaultProfile</span></span>
<span data-ttu-id="a33c9-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a33c9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a33c9-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a33c9-115">-Name</span></span>
<span data-ttu-id="a33c9-116">Nazwa przestrzeni nazw aplikacji EventHub</span><span class="sxs-lookup"><span data-stu-id="a33c9-116">EventHub Namespace Name</span></span>

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

### <span data-ttu-id="a33c9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a33c9-117">-ResourceGroupName</span></span>
<span data-ttu-id="a33c9-118">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="a33c9-118">Resource Group Name</span></span>

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

### <span data-ttu-id="a33c9-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a33c9-119">CommonParameters</span></span>
<span data-ttu-id="a33c9-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a33c9-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a33c9-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a33c9-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a33c9-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a33c9-122">INPUTS</span></span>

### <span data-ttu-id="a33c9-123">System.String</span><span class="sxs-lookup"><span data-stu-id="a33c9-123">System.String</span></span>

## <span data-ttu-id="a33c9-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a33c9-124">OUTPUTS</span></span>

### <span data-ttu-id="a33c9-125">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="a33c9-125">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="a33c9-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a33c9-126">NOTES</span></span>

## <span data-ttu-id="a33c9-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a33c9-127">RELATED LINKS</span></span>
