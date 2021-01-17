---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/new-azanalysisservicesfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallRule.md
ms.openlocfilehash: 9aecede69497bd1a8723720200ed73e12b4aa776
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98332809"
---
# <span data-ttu-id="01d06-101">New-AzAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="01d06-101">New-AzAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="01d06-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="01d06-102">SYNOPSIS</span></span>
<span data-ttu-id="01d06-103">Tworzy nową regułę zapory usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="01d06-103">Creates a new Analysis Services firewall rule</span></span>

## <span data-ttu-id="01d06-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="01d06-104">SYNTAX</span></span>

```
New-AzAnalysisServicesFirewallRule [-FirewallRuleName] <String> [-RangeStart] <String> [-RangeEnd] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="01d06-105">Opis</span><span class="sxs-lookup"><span data-stu-id="01d06-105">DESCRIPTION</span></span>
<span data-ttu-id="01d06-106">New-AzAnalysisServicesFirewallRule tworzy nowy obiekt reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="01d06-106">The New-AzAnalysisServicesFirewallRule creates a new firewall rule object.</span></span>

## <span data-ttu-id="01d06-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="01d06-107">EXAMPLES</span></span>

### <span data-ttu-id="01d06-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="01d06-108">Example 1</span></span>
```
PS C:\> New-AzAnalysisServicesFirewallRule -FirewallRuleName rule1 -RangeStart 0.0.0.0 -RangeEnd 255.255.255.255
```

<span data-ttu-id="01d06-109">Tworzy regułę zapory o nazwie RULE1 z zakresem początkowym 0.0.0.0 i zakresem końcowym 255.255.255.255.</span><span class="sxs-lookup"><span data-stu-id="01d06-109">Creates a firewall rule named rule1 with start range 0.0.0.0 and end range 255.255.255.255</span></span>

## <span data-ttu-id="01d06-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="01d06-110">PARAMETERS</span></span>

### <span data-ttu-id="01d06-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01d06-111">-DefaultProfile</span></span>
<span data-ttu-id="01d06-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="01d06-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01d06-113">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="01d06-113">-FirewallRuleName</span></span>
<span data-ttu-id="01d06-114">Nazwa reguły zapory</span><span class="sxs-lookup"><span data-stu-id="01d06-114">Name of firewall rule</span></span>

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

### <span data-ttu-id="01d06-115">-RangeEnd</span><span class="sxs-lookup"><span data-stu-id="01d06-115">-RangeEnd</span></span>
<span data-ttu-id="01d06-116">Koniec zakresu reguły zapory</span><span class="sxs-lookup"><span data-stu-id="01d06-116">The range end of a firewall rule</span></span>

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

### <span data-ttu-id="01d06-117">-RangeStart</span><span class="sxs-lookup"><span data-stu-id="01d06-117">-RangeStart</span></span>
<span data-ttu-id="01d06-118">Początek zakresu reguły zapory</span><span class="sxs-lookup"><span data-stu-id="01d06-118">The range start of a firewall rule</span></span>

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

### <span data-ttu-id="01d06-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01d06-119">CommonParameters</span></span>
<span data-ttu-id="01d06-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01d06-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01d06-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01d06-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01d06-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="01d06-122">INPUTS</span></span>

### <span data-ttu-id="01d06-123">System. String</span><span class="sxs-lookup"><span data-stu-id="01d06-123">System.String</span></span>

## <span data-ttu-id="01d06-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="01d06-124">OUTPUTS</span></span>

### <span data-ttu-id="01d06-125">Microsoft. Azure. Commands. AnalysisServices. models. PsAzureAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="01d06-125">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="01d06-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="01d06-126">NOTES</span></span>

## <span data-ttu-id="01d06-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="01d06-127">RELATED LINKS</span></span>

[<span data-ttu-id="01d06-128">Nowe — AzAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="01d06-128">New-AzAnalysisServicesFirewallConfig</span></span>](./New-AzAnalysisServicesFirewallConfig.md)