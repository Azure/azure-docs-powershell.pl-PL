---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/new-azurermanalysisservicesfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesFirewallRule.md
ms.openlocfilehash: 2a47c97ea189d4064edae7a871e21465d866f1f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543999"
---
# <span data-ttu-id="55005-101">New-AzureRmAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="55005-101">New-AzureRmAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="55005-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="55005-102">SYNOPSIS</span></span>
<span data-ttu-id="55005-103">Tworzy nową regułę zapory usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="55005-103">Creates a new Analysis Services firewall rule</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55005-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="55005-104">SYNTAX</span></span>

```
New-AzureRmAnalysisServicesFirewallRule [-FirewallRuleName] <String> [-RangeStart] <String>
 [-RangeEnd] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55005-105">Opis</span><span class="sxs-lookup"><span data-stu-id="55005-105">DESCRIPTION</span></span>
<span data-ttu-id="55005-106">New-AzureRmAnalysisServicesFirewallRule tworzy nowy obiekt reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="55005-106">The New-AzureRmAnalysisServicesFirewallRule creates a new firewall rule object.</span></span>

## <span data-ttu-id="55005-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="55005-107">EXAMPLES</span></span>

### <span data-ttu-id="55005-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="55005-108">Example 1</span></span>
```
PS C:\> New-AzureRmAnalysisServicesFirewallRule -FirewallRuleName rule1 -RangeStart 0.0.0.0 -RangeEnd 255.255.255.255
```

<span data-ttu-id="55005-109">Tworzy regułę zapory o nazwie RULE1 z zakresem początkowym 0.0.0.0 i zakresem końcowym 255.255.255.255.</span><span class="sxs-lookup"><span data-stu-id="55005-109">Creates a firewall rule named rule1 with start range 0.0.0.0 and end range 255.255.255.255</span></span>

## <span data-ttu-id="55005-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="55005-110">PARAMETERS</span></span>

### <span data-ttu-id="55005-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55005-111">-DefaultProfile</span></span>
<span data-ttu-id="55005-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="55005-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55005-113">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="55005-113">-FirewallRuleName</span></span>
<span data-ttu-id="55005-114">Nazwa reguły zapory</span><span class="sxs-lookup"><span data-stu-id="55005-114">Name of firewall rule</span></span>

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

### <span data-ttu-id="55005-115">-RangeEnd</span><span class="sxs-lookup"><span data-stu-id="55005-115">-RangeEnd</span></span>
<span data-ttu-id="55005-116">Koniec zakresu reguły zapory</span><span class="sxs-lookup"><span data-stu-id="55005-116">The range end of a firewall rule</span></span>

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

### <span data-ttu-id="55005-117">-RangeStart</span><span class="sxs-lookup"><span data-stu-id="55005-117">-RangeStart</span></span>
<span data-ttu-id="55005-118">Początek zakresu reguły zapory</span><span class="sxs-lookup"><span data-stu-id="55005-118">The range start of a firewall rule</span></span>

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

### <span data-ttu-id="55005-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55005-119">CommonParameters</span></span>
<span data-ttu-id="55005-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55005-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55005-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55005-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55005-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="55005-122">INPUTS</span></span>

### <span data-ttu-id="55005-123">System. String</span><span class="sxs-lookup"><span data-stu-id="55005-123">System.String</span></span>

## <span data-ttu-id="55005-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="55005-124">OUTPUTS</span></span>

### <span data-ttu-id="55005-125">Microsoft. Azure. Commands. AnalysisServices. models. PsAzureAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="55005-125">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="55005-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="55005-126">NOTES</span></span>

## <span data-ttu-id="55005-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="55005-127">RELATED LINKS</span></span>

[<span data-ttu-id="55005-128">Nowe — AzureRmAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="55005-128">New-AzureRmAnalysisServicesFirewallConfig</span></span>](./New-AzureRmAnalysisServicesFirewallConfig.md)
