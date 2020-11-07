---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Get-AzEventHubNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Get-AzEventHubNetworkRuleSet.md
ms.openlocfilehash: 64dae906f7f28e119d8550ecf5bb31d1b6ca7b27
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891494"
---
# <span data-ttu-id="d865b-101">Get-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="d865b-101">Get-AzEventHubNetworkRuleSet</span></span>

## <span data-ttu-id="d865b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d865b-102">SYNOPSIS</span></span>
<span data-ttu-id="d865b-103">Pobiera szczegóły NetworkruleSety koncentratorów zdarzeń w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d865b-103">Gets the details of an Event Hubs NetworkruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="d865b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d865b-104">SYNTAX</span></span>

### <span data-ttu-id="d865b-105">NetworkRuleSetPropertiesSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d865b-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Get-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Namespace] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d865b-106">NetworkRuleSetNamespacePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="d865b-106">NetworkRuleSetNamespacePropertiesSet</span></span>
```
Get-AzEventHubNetworkRuleSet [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d865b-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d865b-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Get-AzEventHubNetworkRuleSet [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d865b-108">Opis</span><span class="sxs-lookup"><span data-stu-id="d865b-108">DESCRIPTION</span></span>
<span data-ttu-id="d865b-109">Pobiera szczegóły NetworkruleSety koncentratorów zdarzeń w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d865b-109">Gets the details of an Event Hubs NetworkruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="d865b-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d865b-110">EXAMPLES</span></span>

### <span data-ttu-id="d865b-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d865b-111">Example 1</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace Eventhub-Namespace1-1375
```

<span data-ttu-id="d865b-112">Zapoznaj się z informacjami o NetworkruleSetych koncentratorów zdarzeń przy użyciu parametrów resourceName i Namespace.</span><span class="sxs-lookup"><span data-stu-id="d865b-112">Get the details of Event Hubs NetworkruleSet of namespace using ResourceGroup and Namespace parameters.</span></span> 

### <span data-ttu-id="d865b-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="d865b-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -Namespace Eventhub-Namespace1-2389
```

<span data-ttu-id="d865b-114">Zapoznaj się z informacjami o NetworkruleSetych koncentratorów zdarzeń w obszarze nazw, które znajdują się w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d865b-114">Get the details of Event Hubs NetworkruleSet of namespace using  Namespace which is in the current subscription.</span></span>

### <span data-ttu-id="d865b-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="d865b-115">Example 3</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace1-2389
```

<span data-ttu-id="d865b-116">Uzyskiwanie szczegółowych informacji o NetworkruleSetych koncentratorów zdarzeń przy użyciu identyfikatora zasobu innej przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="d865b-116">Get the details of Event Hubs NetworkruleSet of namespace using Resource Id of other Namespace</span></span> 

## <span data-ttu-id="d865b-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d865b-117">PARAMETERS</span></span>

### <span data-ttu-id="d865b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d865b-118">-DefaultProfile</span></span>
<span data-ttu-id="d865b-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d865b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d865b-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d865b-120">-Namespace</span></span>
<span data-ttu-id="d865b-121">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="d865b-121">Namespace Name</span></span>

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

### <span data-ttu-id="d865b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d865b-122">-ResourceGroupName</span></span>
<span data-ttu-id="d865b-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="d865b-123">Resource Group Name</span></span>

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

### <span data-ttu-id="d865b-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d865b-124">-ResourceId</span></span>
<span data-ttu-id="d865b-125">Identyfikator zasobu obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="d865b-125">Namespace Resource Id</span></span>

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

### <span data-ttu-id="d865b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d865b-126">CommonParameters</span></span>
<span data-ttu-id="d865b-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d865b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="d865b-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d865b-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d865b-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d865b-129">INPUTS</span></span>

### <span data-ttu-id="d865b-130">System. String</span><span class="sxs-lookup"><span data-stu-id="d865b-130">System.String</span></span>

## <span data-ttu-id="d865b-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d865b-131">OUTPUTS</span></span>

### <span data-ttu-id="d865b-132">Microsoft. Azure. Commands. EventHub. modele. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="d865b-132">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="d865b-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d865b-133">NOTES</span></span>

## <span data-ttu-id="d865b-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d865b-134">RELATED LINKS</span></span>