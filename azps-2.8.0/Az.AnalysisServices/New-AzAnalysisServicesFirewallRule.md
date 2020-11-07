---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/new-azanalysisservicesfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallRule.md
ms.openlocfilehash: 7fb766bfa65d37fd8491e93593b3ea423938fd3f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707131"
---
# <span data-ttu-id="cc2ef-101">New-AzAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="cc2ef-101">New-AzAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="cc2ef-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cc2ef-102">SYNOPSIS</span></span>
<span data-ttu-id="cc2ef-103">Tworzy nową regułę zapory usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="cc2ef-103">Creates a new Analysis Services firewall rule</span></span>

## <span data-ttu-id="cc2ef-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cc2ef-104">SYNTAX</span></span>

```
New-AzAnalysisServicesFirewallRule [-FirewallRuleName] <String> [-RangeStart] <String> [-RangeEnd] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cc2ef-105">Opis</span><span class="sxs-lookup"><span data-stu-id="cc2ef-105">DESCRIPTION</span></span>
<span data-ttu-id="cc2ef-106">New-AzAnalysisServicesFirewallRule tworzy nowy obiekt reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="cc2ef-106">The New-AzAnalysisServicesFirewallRule creates a new firewall rule object.</span></span>

## <span data-ttu-id="cc2ef-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cc2ef-107">EXAMPLES</span></span>

### <span data-ttu-id="cc2ef-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cc2ef-108">Example 1</span></span>
```
PS C:\> New-AzAnalysisServicesFirewallRule -FirewallRuleName rule1 -RangeStart 0.0.0.0 -RangeEnd 255.255.255.255
```

<span data-ttu-id="cc2ef-109">Tworzy regułę zapory o nazwie RULE1 z zakresem początkowym 0.0.0.0 i zakresem końcowym 255.255.255.255.</span><span class="sxs-lookup"><span data-stu-id="cc2ef-109">Creates a firewall rule named rule1 with start range 0.0.0.0 and end range 255.255.255.255</span></span>

## <span data-ttu-id="cc2ef-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cc2ef-110">PARAMETERS</span></span>

### <span data-ttu-id="cc2ef-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc2ef-111">-DefaultProfile</span></span>
<span data-ttu-id="cc2ef-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cc2ef-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc2ef-113">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="cc2ef-113">-FirewallRuleName</span></span>
<span data-ttu-id="cc2ef-114">Nazwa reguły zapory</span><span class="sxs-lookup"><span data-stu-id="cc2ef-114">Name of firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc2ef-115">-RangeEnd</span><span class="sxs-lookup"><span data-stu-id="cc2ef-115">-RangeEnd</span></span>
<span data-ttu-id="cc2ef-116">Koniec zakresu reguły zapory</span><span class="sxs-lookup"><span data-stu-id="cc2ef-116">The range end of a firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc2ef-117">-RangeStart</span><span class="sxs-lookup"><span data-stu-id="cc2ef-117">-RangeStart</span></span>
<span data-ttu-id="cc2ef-118">Początek zakresu reguły zapory</span><span class="sxs-lookup"><span data-stu-id="cc2ef-118">The range start of a firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc2ef-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc2ef-119">CommonParameters</span></span>
<span data-ttu-id="cc2ef-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc2ef-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc2ef-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc2ef-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc2ef-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cc2ef-122">INPUTS</span></span>

### <span data-ttu-id="cc2ef-123">System. String</span><span class="sxs-lookup"><span data-stu-id="cc2ef-123">System.String</span></span>

## <span data-ttu-id="cc2ef-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cc2ef-124">OUTPUTS</span></span>

### <span data-ttu-id="cc2ef-125">Microsoft. Azure. Commands. AnalysisServices. models. PsAzureAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="cc2ef-125">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="cc2ef-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cc2ef-126">NOTES</span></span>

## <span data-ttu-id="cc2ef-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cc2ef-127">RELATED LINKS</span></span>

[<span data-ttu-id="cc2ef-128">Nowe — AzAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="cc2ef-128">New-AzAnalysisServicesFirewallConfig</span></span>](./New-AzAnalysisServicesFirewallConfig.md)