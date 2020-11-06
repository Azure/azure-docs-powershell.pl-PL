---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespace.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 971312367815c8dc9c8c4f3f8fb6f2face0b7408
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551880"
---
# <span data-ttu-id="47b4f-101">Get-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="47b4f-101">Get-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="47b4f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="47b4f-102">SYNOPSIS</span></span>
<span data-ttu-id="47b4f-103">Pobiera szczegóły obszaru nazw koncentratorów zdarzeń lub pobiera listę wszystkich obszarów nazw koncentratorów zdarzeń w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="47b4f-103">Gets the details of an Event Hubs namespace, or gets a list of all Event Hubs namespaces in the current Azure subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47b4f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="47b4f-104">SYNTAX</span></span>

```
Get-AzureRmEventHubNamespace [[-ResourceGroupName] <String>] [-Name <String>]
```

## <span data-ttu-id="47b4f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="47b4f-105">DESCRIPTION</span></span>
<span data-ttu-id="47b4f-106">Polecenie cmdlet Get-AzureRmEventHubNamespace pobiera szczegóły określonego obszaru nazw koncentratora zdarzeń lub listę wszystkich obszarów nazw koncentratorów zdarzeń w bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="47b4f-106">The Get-AzureRmEventHubNamespace cmdlet gets either the details of a specified Event Hubs namespace, or a list of all Event Hubs namespaces in the current Azure subscription.</span></span>
<span data-ttu-id="47b4f-107">Jeśli podano nazwę obszaru nazw, zostanie zwrócona wartość szczegółów pojedynczego obszaru nazw koncentratorów zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="47b4f-107">If the namespace name is provided, the details of a single Event Hubs namespace is returned.</span></span>
<span data-ttu-id="47b4f-108">Jeśli nie podano nazwy obszaru nazw, zostanie zwrócona lista obszarów nazw.</span><span class="sxs-lookup"><span data-stu-id="47b4f-108">If the namespace name is not provided, a list of namespaces is returned.</span></span>

## <span data-ttu-id="47b4f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="47b4f-109">EXAMPLES</span></span>

### <span data-ttu-id="47b4f-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="47b4f-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="47b4f-111">Umożliwia wyświetlenie szczegółów obszaru nazw Hubs (obszar_nazwname) \` \` w grupie zasobów \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="47b4f-111">Gets the details of the Event Hubs namespace \`MyNamespaceName\` in the resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="47b4f-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="47b4f-112">PARAMETERS</span></span>

### <span data-ttu-id="47b4f-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47b4f-113">-ResourceGroupName</span></span>
<span data-ttu-id="47b4f-114">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="47b4f-114">Resource group name.</span></span>

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

### <span data-ttu-id="47b4f-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="47b4f-115">-Name</span></span>
<span data-ttu-id="47b4f-116">Nazwa obszaru nazw EventHub.</span><span class="sxs-lookup"><span data-stu-id="47b4f-116">EventHub Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="47b4f-117">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="47b4f-117">INPUTS</span></span>

### <span data-ttu-id="47b4f-118">System. String</span><span class="sxs-lookup"><span data-stu-id="47b4f-118">System.String</span></span>

## <span data-ttu-id="47b4f-119">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="47b4f-119">OUTPUTS</span></span>

### <span data-ttu-id="47b4f-120">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. EventHub. modele. NamespaceAttributes, Microsoft. Azure. Commands. EventHub, Version = 0.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="47b4f-120">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.NamespaceAttributes, Microsoft.Azure.Commands.EventHub, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="47b4f-121">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="47b4f-121">NOTES</span></span>

## <span data-ttu-id="47b4f-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="47b4f-122">RELATED LINKS</span></span>

