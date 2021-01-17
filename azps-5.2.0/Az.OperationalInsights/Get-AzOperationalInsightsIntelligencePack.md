---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 0F9D72C1-2E42-4A67-9FDE-6344F5DE6C30
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsintelligencepack
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsIntelligencePack.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsIntelligencePack.md
ms.openlocfilehash: e197a5df0993ffbb97415bdc4e72ed9ea7603713
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98370279"
---
# <span data-ttu-id="fbf1b-101">Get-AzOperationalInsightsIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="fbf1b-101">Get-AzOperationalInsightsIntelligencePack</span></span>

## <span data-ttu-id="fbf1b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fbf1b-102">SYNOPSIS</span></span>
<span data-ttu-id="fbf1b-103">Pobiera dostępne pakiety analiz.</span><span class="sxs-lookup"><span data-stu-id="fbf1b-103">Gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="fbf1b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fbf1b-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsIntelligencePack [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fbf1b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fbf1b-105">DESCRIPTION</span></span>
<span data-ttu-id="fbf1b-106">Polecenie cmdlet **Get-AzOperationalInsightsIntelligencePack** Pobiera dostępne pakiety analiz.</span><span class="sxs-lookup"><span data-stu-id="fbf1b-106">The **Get-AzOperationalInsightsIntelligencePack** cmdlet gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="fbf1b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fbf1b-107">EXAMPLES</span></span>

### <span data-ttu-id="fbf1b-108">Przykład 1: pobieranie pakietów analiz</span><span class="sxs-lookup"><span data-stu-id="fbf1b-108">Example 1: Get Intelligence Packs</span></span>
```
PS C:\>Get-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="fbf1b-109">To polecenie pobiera dostępne pakiety analiz.</span><span class="sxs-lookup"><span data-stu-id="fbf1b-109">This command gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="fbf1b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fbf1b-110">PARAMETERS</span></span>

### <span data-ttu-id="fbf1b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbf1b-111">-DefaultProfile</span></span>
<span data-ttu-id="fbf1b-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="fbf1b-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fbf1b-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbf1b-113">-ResourceGroupName</span></span>
<span data-ttu-id="fbf1b-114">Określa nazwę grupy zasobów platformy Azure zawierającej obszar roboczy.</span><span class="sxs-lookup"><span data-stu-id="fbf1b-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="fbf1b-115">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="fbf1b-115">-WorkspaceName</span></span>
<span data-ttu-id="fbf1b-116">Określa nazwę obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="fbf1b-116">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbf1b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbf1b-117">CommonParameters</span></span>
<span data-ttu-id="fbf1b-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbf1b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbf1b-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbf1b-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbf1b-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fbf1b-120">INPUTS</span></span>

### <span data-ttu-id="fbf1b-121">System. String</span><span class="sxs-lookup"><span data-stu-id="fbf1b-121">System.String</span></span>

## <span data-ttu-id="fbf1b-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fbf1b-122">OUTPUTS</span></span>

### <span data-ttu-id="fbf1b-123">Microsoft. Azure. Commands. OperationalInsights. models. PSIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="fbf1b-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack</span></span>

## <span data-ttu-id="fbf1b-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fbf1b-124">NOTES</span></span>

## <span data-ttu-id="fbf1b-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fbf1b-125">RELATED LINKS</span></span>

[<span data-ttu-id="fbf1b-126">Polecenia cmdlet usługi Azure Operations Insights</span><span class="sxs-lookup"><span data-stu-id="fbf1b-126">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


