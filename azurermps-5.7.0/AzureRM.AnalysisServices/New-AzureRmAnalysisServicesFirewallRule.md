---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/new-azurermanalysisservicesfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesFirewallRule.md
ms.openlocfilehash: 74a6d563772e84c7356c400b674cbab960ee8dd6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549803"
---
# <span data-ttu-id="b4549-101">New-AzureRmAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b4549-101">New-AzureRmAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="b4549-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b4549-102">SYNOPSIS</span></span>
<span data-ttu-id="b4549-103">Tworzy nową regułę zapory usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="b4549-103">Creates a new Analysis Services firewall rule</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b4549-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b4549-104">SYNTAX</span></span>

```
New-AzureRmAnalysisServicesFirewallRule [-FirewallRuleName] <String> [-RangeStart] <String> [-RangeEnd] <String>
```

## <span data-ttu-id="b4549-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b4549-105">DESCRIPTION</span></span>
<span data-ttu-id="b4549-106">New-AzureRmAnalysisServicesFirewallRule tworzy nowy obiekt reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="b4549-106">The New-AzureRmAnalysisServicesFirewallRule creates a new firewall rule object.</span></span>

## <span data-ttu-id="b4549-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b4549-107">EXAMPLES</span></span>

### <span data-ttu-id="b4549-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b4549-108">Example 1</span></span>
```
PS C:\> New-AzureRmAnalysisServicesFirewallRule -FirewallRuleName rule1 -RangeStart 0.0.0.0 -RangeEnd 255.255.255.255
```

<span data-ttu-id="b4549-109">Tworzy regułę zapory o nazwie RULE1 z zakresem początkowym 0.0.0.0 i zakresem końcowym 255.255.255.255.</span><span class="sxs-lookup"><span data-stu-id="b4549-109">Creates a firewall rule named rule1 with start range 0.0.0.0 and end range 255.255.255.255</span></span>

## <span data-ttu-id="b4549-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b4549-110">PARAMETERS</span></span>

### <span data-ttu-id="b4549-111">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="b4549-111">-FirewallRuleName</span></span>
<span data-ttu-id="b4549-112">Nazwa reguły zapory</span><span class="sxs-lookup"><span data-stu-id="b4549-112">Name of firewall rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4549-113">-RangeStart</span><span class="sxs-lookup"><span data-stu-id="b4549-113">-RangeStart</span></span>
<span data-ttu-id="b4549-114">Początek zakresu reguły zapory</span><span class="sxs-lookup"><span data-stu-id="b4549-114">The range start of a firewall rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4549-115">-RangeEnd</span><span class="sxs-lookup"><span data-stu-id="b4549-115">-RangeEnd</span></span>
<span data-ttu-id="b4549-116">Koniec zakresu reguły zapory</span><span class="sxs-lookup"><span data-stu-id="b4549-116">The range end of a firewall rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="b4549-117">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b4549-117">INPUTS</span></span>

## <span data-ttu-id="b4549-118">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b4549-118">OUTPUTS</span></span>

### <span data-ttu-id="b4549-119">Microsoft. Azure. Commands. AnalysisServices. models. AzureAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b4549-119">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="b4549-120">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b4549-120">RELATED LINKS</span></span>

[<span data-ttu-id="b4549-121">Nowe — AzureRmAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="b4549-121">New-AzureRmAnalysisServicesFirewallConfig</span></span>](./New-AzureRmAnalysisServicesFirewallConfig.md)
