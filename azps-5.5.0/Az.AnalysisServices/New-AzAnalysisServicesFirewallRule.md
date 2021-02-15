---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/new-azanalysisservicesfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallRule.md
ms.openlocfilehash: 9aecede69497bd1a8723720200ed73e12b4aa776
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182403"
---
# <span data-ttu-id="3eb0f-101">New-AzAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="3eb0f-101">New-AzAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="3eb0f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3eb0f-102">SYNOPSIS</span></span>
<span data-ttu-id="3eb0f-103">Tworzy nową regułę zapory usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="3eb0f-103">Creates a new Analysis Services firewall rule</span></span>

## <span data-ttu-id="3eb0f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3eb0f-104">SYNTAX</span></span>

```
New-AzAnalysisServicesFirewallRule [-FirewallRuleName] <String> [-RangeStart] <String> [-RangeEnd] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3eb0f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="3eb0f-105">DESCRIPTION</span></span>
<span data-ttu-id="3eb0f-106">Ta New-AzAnalysisServicesFirewallRule utworzy nowy obiekt reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="3eb0f-106">The New-AzAnalysisServicesFirewallRule creates a new firewall rule object.</span></span>

## <span data-ttu-id="3eb0f-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3eb0f-107">EXAMPLES</span></span>

### <span data-ttu-id="3eb0f-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3eb0f-108">Example 1</span></span>
```
PS C:\> New-AzAnalysisServicesFirewallRule -FirewallRuleName rule1 -RangeStart 0.0.0.0 -RangeEnd 255.255.255.255
```

<span data-ttu-id="3eb0f-109">Tworzy regułę zapory o nazwie reguła1 z zakresem rozpoczęcia 0.0.0.0 i zakresem zakończenia 255.255.255.255.</span><span class="sxs-lookup"><span data-stu-id="3eb0f-109">Creates a firewall rule named rule1 with start range 0.0.0.0 and end range 255.255.255.255</span></span>

## <span data-ttu-id="3eb0f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3eb0f-110">PARAMETERS</span></span>

### <span data-ttu-id="3eb0f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3eb0f-111">-DefaultProfile</span></span>
<span data-ttu-id="3eb0f-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3eb0f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3eb0f-113">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="3eb0f-113">-FirewallRuleName</span></span>
<span data-ttu-id="3eb0f-114">Nazwa reguły zapory</span><span class="sxs-lookup"><span data-stu-id="3eb0f-114">Name of firewall rule</span></span>

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

### <span data-ttu-id="3eb0f-115">-RangeEnd</span><span class="sxs-lookup"><span data-stu-id="3eb0f-115">-RangeEnd</span></span>
<span data-ttu-id="3eb0f-116">Zakres końca reguły zapory</span><span class="sxs-lookup"><span data-stu-id="3eb0f-116">The range end of a firewall rule</span></span>

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

### <span data-ttu-id="3eb0f-117">-RangeStart</span><span class="sxs-lookup"><span data-stu-id="3eb0f-117">-RangeStart</span></span>
<span data-ttu-id="3eb0f-118">Początek zakresu reguły zapory</span><span class="sxs-lookup"><span data-stu-id="3eb0f-118">The range start of a firewall rule</span></span>

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

### <span data-ttu-id="3eb0f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3eb0f-119">CommonParameters</span></span>
<span data-ttu-id="3eb0f-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3eb0f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3eb0f-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3eb0f-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3eb0f-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3eb0f-122">INPUTS</span></span>

### <span data-ttu-id="3eb0f-123">System.String</span><span class="sxs-lookup"><span data-stu-id="3eb0f-123">System.String</span></span>

## <span data-ttu-id="3eb0f-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3eb0f-124">OUTPUTS</span></span>

### <span data-ttu-id="3eb0f-125">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="3eb0f-125">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="3eb0f-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3eb0f-126">NOTES</span></span>

## <span data-ttu-id="3eb0f-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3eb0f-127">RELATED LINKS</span></span>

[<span data-ttu-id="3eb0f-128">New-AzAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="3eb0f-128">New-AzAnalysisServicesFirewallConfig</span></span>](./New-AzAnalysisServicesFirewallConfig.md)