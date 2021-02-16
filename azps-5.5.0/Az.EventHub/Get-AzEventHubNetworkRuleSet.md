---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNetworkRuleSet.md
ms.openlocfilehash: 773f21c189833bf8dd9817d224b83eaf29dd644e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185931"
---
# <span data-ttu-id="408b4-101">Get-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="408b4-101">Get-AzEventHubNetworkRuleSet</span></span>

## <span data-ttu-id="408b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="408b4-102">SYNOPSIS</span></span>
<span data-ttu-id="408b4-103">Pobiera szczegółowe informacje o centrum zdarzeń NetworkruleSet przestrzeni nazw w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="408b4-103">Gets the details of an Event Hubs NetworkruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="408b4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="408b4-104">SYNTAX</span></span>

### <span data-ttu-id="408b4-105">NetworkRuleSetPropertiesSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="408b4-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Get-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Namespace] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="408b4-106">NetworkRuleSetNamespacePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="408b4-106">NetworkRuleSetNamespacePropertiesSet</span></span>
```
Get-AzEventHubNetworkRuleSet [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="408b4-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="408b4-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Get-AzEventHubNetworkRuleSet [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="408b4-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="408b4-108">DESCRIPTION</span></span>
<span data-ttu-id="408b4-109">Pobiera szczegółowe informacje o centrum zdarzeń NetworkruleSet przestrzeni nazw w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="408b4-109">Gets the details of an Event Hubs NetworkruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="408b4-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="408b4-110">EXAMPLES</span></span>

### <span data-ttu-id="408b4-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="408b4-111">Example 1</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace Eventhub-Namespace1-1375
```

<span data-ttu-id="408b4-112">Uzyskaj szczegółowe informacje na temat zestawu networkruleset centrum zdarzeń przestrzeni nazw przy użyciu parametrów ResourceGroup i Namespace.</span><span class="sxs-lookup"><span data-stu-id="408b4-112">Get the details of Event Hubs NetworkruleSet of namespace using ResourceGroup and Namespace parameters.</span></span> 

### <span data-ttu-id="408b4-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="408b4-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -Namespace Eventhub-Namespace1-2389
```

<span data-ttu-id="408b4-114">Uzyskaj szczegółowe informacje na temat zestawu networkruleset centrum zdarzeń przestrzeni nazw przy użyciu przestrzeni nazw, która znajduje się w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="408b4-114">Get the details of Event Hubs NetworkruleSet of namespace using  Namespace which is in the current subscription.</span></span>

### <span data-ttu-id="408b4-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="408b4-115">Example 3</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace1-2389
```

<span data-ttu-id="408b4-116">Uzyskiwanie szczegółów dotyczących centrum zdarzeń NetworkruleSet przestrzeni nazw przy użyciu identyfikatora zasobu innej przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="408b4-116">Get the details of Event Hubs NetworkruleSet of namespace using Resource Id of other Namespace</span></span> 

## <span data-ttu-id="408b4-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="408b4-117">PARAMETERS</span></span>

### <span data-ttu-id="408b4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="408b4-118">-DefaultProfile</span></span>
<span data-ttu-id="408b4-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="408b4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="408b4-120">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="408b4-120">-Namespace</span></span>
<span data-ttu-id="408b4-121">Nazwa przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="408b4-121">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetPropertiesSet, NetworkRuleSetNamespacePropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="408b4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="408b4-122">-ResourceGroupName</span></span>
<span data-ttu-id="408b4-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="408b4-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetNamespacePropertiesSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="408b4-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="408b4-124">-ResourceId</span></span>
<span data-ttu-id="408b4-125">Identyfikator zasobu przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="408b4-125">Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="408b4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="408b4-126">CommonParameters</span></span>
<span data-ttu-id="408b4-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="408b4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="408b4-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="408b4-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="408b4-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="408b4-129">INPUTS</span></span>

### <span data-ttu-id="408b4-130">System.String</span><span class="sxs-lookup"><span data-stu-id="408b4-130">System.String</span></span>

## <span data-ttu-id="408b4-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="408b4-131">OUTPUTS</span></span>

### <span data-ttu-id="408b4-132">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="408b4-132">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="408b4-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="408b4-133">NOTES</span></span>

## <span data-ttu-id="408b4-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="408b4-134">RELATED LINKS</span></span>