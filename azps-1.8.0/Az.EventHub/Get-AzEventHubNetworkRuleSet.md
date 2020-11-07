---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNetworkRuleSet.md
ms.openlocfilehash: 29eab81028de58c8f23345249ef079f87380257a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709810"
---
# <span data-ttu-id="5d725-101">Get-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="5d725-101">Get-AzEventHubNetworkRuleSet</span></span>

## <span data-ttu-id="5d725-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5d725-102">SYNOPSIS</span></span>
<span data-ttu-id="5d725-103">Pobiera szczegóły NetwrokruleSety koncentratorów zdarzeń w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5d725-103">Gets the details of an Event Hubs NetwrokruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="5d725-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5d725-104">SYNTAX</span></span>

### <span data-ttu-id="5d725-105">NetworkRuleSetPropertiesSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5d725-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Get-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Namespace] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5d725-106">NetworkRuleSetNamespacePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="5d725-106">NetworkRuleSetNamespacePropertiesSet</span></span>
```
Get-AzEventHubNetworkRuleSet [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5d725-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d725-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Get-AzEventHubNetworkRuleSet [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5d725-108">Opis</span><span class="sxs-lookup"><span data-stu-id="5d725-108">DESCRIPTION</span></span>
<span data-ttu-id="5d725-109">Pobiera szczegóły NetwrokruleSety koncentratorów zdarzeń w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5d725-109">Gets the details of an Event Hubs NetwrokruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="5d725-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5d725-110">EXAMPLES</span></span>

### <span data-ttu-id="5d725-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5d725-111">Example 1</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace Eventhub-Namespace1-1375
```

<span data-ttu-id="5d725-112">Zapoznaj się z informacjami o NetwrokruleSetych koncentratorów zdarzeń przy użyciu parametrów resourceName i Namesape.</span><span class="sxs-lookup"><span data-stu-id="5d725-112">Get the details of Event Hubs NetwrokruleSet of namespace using ResourceGroup and Namesape parameters.</span></span> 

### <span data-ttu-id="5d725-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="5d725-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -Namespace Eventhub-Namespace1-2389
```

<span data-ttu-id="5d725-114">Zapoznaj się z informacjami o NetwrokruleSetych koncentratorów zdarzeń w obszarze nazw, które znajdują się w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="5d725-114">Get the details of Event Hubs NetwrokruleSet of namespace using  Namespace which is in the current subscription.</span></span>

### <span data-ttu-id="5d725-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="5d725-115">Example 3</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace1-2389
```

<span data-ttu-id="5d725-116">Uzyskiwanie szczegółowych informacji o NetwrokruleSetych koncentratorów zdarzeń przy użyciu identyfikatora zasobu innej przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="5d725-116">Get the details of Event Hubs NetwrokruleSet of namespace using Resource Id of other Namespace</span></span> 

## <span data-ttu-id="5d725-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5d725-117">PARAMETERS</span></span>

### <span data-ttu-id="5d725-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d725-118">-DefaultProfile</span></span>
<span data-ttu-id="5d725-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5d725-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d725-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="5d725-120">-Namespace</span></span>
<span data-ttu-id="5d725-121">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="5d725-121">Namespace Name</span></span>

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

### <span data-ttu-id="5d725-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d725-122">-ResourceGroupName</span></span>
<span data-ttu-id="5d725-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="5d725-123">Resource Group Name</span></span>

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

### <span data-ttu-id="5d725-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5d725-124">-ResourceId</span></span>
<span data-ttu-id="5d725-125">Identyfikator zasobu obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="5d725-125">Namespace Resource Id</span></span>

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

### <span data-ttu-id="5d725-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d725-126">CommonParameters</span></span>
<span data-ttu-id="5d725-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d725-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="5d725-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d725-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d725-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5d725-129">INPUTS</span></span>

### <span data-ttu-id="5d725-130">System. String</span><span class="sxs-lookup"><span data-stu-id="5d725-130">System.String</span></span>

## <span data-ttu-id="5d725-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5d725-131">OUTPUTS</span></span>

### <span data-ttu-id="5d725-132">Microsoft. Azure. Commands. EventHub. modele. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="5d725-132">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="5d725-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5d725-133">NOTES</span></span>

## <span data-ttu-id="5d725-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5d725-134">RELATED LINKS</span></span>