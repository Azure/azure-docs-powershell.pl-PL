---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNamespace.md
ms.openlocfilehash: ba2209f7b58951bdc52976fb3cbab10fa15da98a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180690"
---
# <span data-ttu-id="4de7f-101">Get-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="4de7f-101">Get-AzEventHubNamespace</span></span>

## <span data-ttu-id="4de7f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4de7f-102">SYNOPSIS</span></span>
<span data-ttu-id="4de7f-103">Pobiera szczegóły przestrzeni nazw centrum zdarzeń lub pobiera listę wszystkich przestrzeni nazw centrum zdarzeń w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="4de7f-103">Gets the details of an Event Hubs namespace, or gets a list of all Event Hubs namespaces in the current Azure subscription.</span></span>

## <span data-ttu-id="4de7f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4de7f-104">SYNTAX</span></span>

```
Get-AzEventHubNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4de7f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="4de7f-105">DESCRIPTION</span></span>
<span data-ttu-id="4de7f-106">Polecenie Get-AzEventHubNamespace pobiera szczegóły przestrzeni nazw określonej przestrzeni nazw centrum zdarzeń lub listę wszystkich przestrzeni nazw centrum zdarzeń w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="4de7f-106">The Get-AzEventHubNamespace cmdlet gets either the details of a specified Event Hubs namespace, or a list of all Event Hubs namespaces in the current Azure subscription.</span></span>
<span data-ttu-id="4de7f-107">Jeśli podano nazwę przestrzeni nazw, zwracane są szczegóły przestrzeni nazw pojedynczych centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="4de7f-107">If the namespace name is provided, the details of a single Event Hubs namespace is returned.</span></span>
<span data-ttu-id="4de7f-108">Jeśli nazwa przestrzeni nazw nie jest podano, jest zwracana lista przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="4de7f-108">If the namespace name is not provided, a list of namespaces is returned.</span></span>

## <span data-ttu-id="4de7f-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4de7f-109">EXAMPLES</span></span>

### <span data-ttu-id="4de7f-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4de7f-110">Example 1</span></span>
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

<span data-ttu-id="4de7f-111">Pobiera szczegóły przestrzeni nazw \` MyNamespaceName \` w grupie zasobów \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="4de7f-111">Gets the details of namespace \`MyNamespaceName\` in the resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="4de7f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4de7f-112">PARAMETERS</span></span>

### <span data-ttu-id="4de7f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4de7f-113">-DefaultProfile</span></span>
<span data-ttu-id="4de7f-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4de7f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4de7f-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="4de7f-115">-Name</span></span>
<span data-ttu-id="4de7f-116">Nazwa przestrzeni nazw aplikacji EventHub</span><span class="sxs-lookup"><span data-stu-id="4de7f-116">EventHub Namespace Name</span></span>

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

### <span data-ttu-id="4de7f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4de7f-117">-ResourceGroupName</span></span>
<span data-ttu-id="4de7f-118">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="4de7f-118">Resource Group Name</span></span>

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

### <span data-ttu-id="4de7f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4de7f-119">CommonParameters</span></span>
<span data-ttu-id="4de7f-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4de7f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4de7f-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4de7f-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4de7f-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4de7f-122">INPUTS</span></span>

### <span data-ttu-id="4de7f-123">System.String</span><span class="sxs-lookup"><span data-stu-id="4de7f-123">System.String</span></span>

## <span data-ttu-id="4de7f-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4de7f-124">OUTPUTS</span></span>

### <span data-ttu-id="4de7f-125">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="4de7f-125">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="4de7f-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4de7f-126">NOTES</span></span>

## <span data-ttu-id="4de7f-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4de7f-127">RELATED LINKS</span></span>
