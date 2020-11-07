---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 0F9D72C1-2E42-4A67-9FDE-6344F5DE6C30
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsintelligencepack
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsIntelligencePack.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsIntelligencePack.md
ms.openlocfilehash: fa4df1d2b2149a0bc9c637ffefd5c60e52fa0059
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/13/2020
ms.locfileid: "93710914"
---
# <span data-ttu-id="fe5d6-101">Get-AzOperationalInsightsIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="fe5d6-101">Get-AzOperationalInsightsIntelligencePack</span></span>

## <span data-ttu-id="fe5d6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fe5d6-102">SYNOPSIS</span></span>
<span data-ttu-id="fe5d6-103">Pobiera dostępne pakiety analiz.</span><span class="sxs-lookup"><span data-stu-id="fe5d6-103">Gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="fe5d6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fe5d6-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsIntelligencePack [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe5d6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fe5d6-105">DESCRIPTION</span></span>
<span data-ttu-id="fe5d6-106">Polecenie cmdlet **Get-AzOperationalInsightsIntelligencePack** Pobiera dostępne pakiety analiz.</span><span class="sxs-lookup"><span data-stu-id="fe5d6-106">The **Get-AzOperationalInsightsIntelligencePack** cmdlet gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="fe5d6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fe5d6-107">EXAMPLES</span></span>

### <span data-ttu-id="fe5d6-108">Przykład 1: pobieranie pakietów analiz</span><span class="sxs-lookup"><span data-stu-id="fe5d6-108">Example 1: Get Intelligence Packs</span></span>
```
PS C:\>Get-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="fe5d6-109">To polecenie pobiera dostępne pakiety analiz.</span><span class="sxs-lookup"><span data-stu-id="fe5d6-109">This command gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="fe5d6-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fe5d6-110">PARAMETERS</span></span>

### <span data-ttu-id="fe5d6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe5d6-111">-DefaultProfile</span></span>
<span data-ttu-id="fe5d6-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="fe5d6-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fe5d6-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe5d6-113">-ResourceGroupName</span></span>
<span data-ttu-id="fe5d6-114">Określa nazwę grupy zasobów platformy Azure zawierającej obszar roboczy.</span><span class="sxs-lookup"><span data-stu-id="fe5d6-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="fe5d6-115">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="fe5d6-115">-WorkspaceName</span></span>
<span data-ttu-id="fe5d6-116">Określa nazwę obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="fe5d6-116">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="fe5d6-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe5d6-117">CommonParameters</span></span>
<span data-ttu-id="fe5d6-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe5d6-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe5d6-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe5d6-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe5d6-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fe5d6-120">INPUTS</span></span>

### <span data-ttu-id="fe5d6-121">System. String</span><span class="sxs-lookup"><span data-stu-id="fe5d6-121">System.String</span></span>

## <span data-ttu-id="fe5d6-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fe5d6-122">OUTPUTS</span></span>

### <span data-ttu-id="fe5d6-123">Microsoft. Azure. Commands. OperationalInsights. models. PSIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="fe5d6-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack</span></span>

## <span data-ttu-id="fe5d6-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fe5d6-124">NOTES</span></span>

## <span data-ttu-id="fe5d6-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fe5d6-125">RELATED LINKS</span></span>

[<span data-ttu-id="fe5d6-126">Polecenia cmdlet usługi Azure Operations Insights</span><span class="sxs-lookup"><span data-stu-id="fe5d6-126">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)

