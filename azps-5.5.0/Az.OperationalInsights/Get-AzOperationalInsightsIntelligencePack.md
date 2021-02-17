---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 0F9D72C1-2E42-4A67-9FDE-6344F5DE6C30
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsintelligencepack
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsIntelligencePack.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsIntelligencePack.md
ms.openlocfilehash: e197a5df0993ffbb97415bdc4e72ed9ea7603713
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202355"
---
# <span data-ttu-id="62b84-101">Get-AzOperationalInsightsIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="62b84-101">Get-AzOperationalInsightsIntelligencePack</span></span>

## <span data-ttu-id="62b84-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62b84-102">SYNOPSIS</span></span>
<span data-ttu-id="62b84-103">Pobiera dostępne pakiety analiz.</span><span class="sxs-lookup"><span data-stu-id="62b84-103">Gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="62b84-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="62b84-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsIntelligencePack [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62b84-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="62b84-105">DESCRIPTION</span></span>
<span data-ttu-id="62b84-106">Polecenie **cmdlet Get-AzOperationalInsightsIntelligencePack** pobiera dostępne pakiety intelligence.</span><span class="sxs-lookup"><span data-stu-id="62b84-106">The **Get-AzOperationalInsightsIntelligencePack** cmdlet gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="62b84-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="62b84-107">EXAMPLES</span></span>

### <span data-ttu-id="62b84-108">Przykład 1. Uzyskiwanie pakietów analizy</span><span class="sxs-lookup"><span data-stu-id="62b84-108">Example 1: Get Intelligence Packs</span></span>
```
PS C:\>Get-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="62b84-109">To polecenie pobiera dostępne pakiety analizy.</span><span class="sxs-lookup"><span data-stu-id="62b84-109">This command gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="62b84-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="62b84-110">PARAMETERS</span></span>

### <span data-ttu-id="62b84-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62b84-111">-DefaultProfile</span></span>
<span data-ttu-id="62b84-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="62b84-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="62b84-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62b84-113">-ResourceGroupName</span></span>
<span data-ttu-id="62b84-114">Określa nazwę grupy zasobów platformy Azure zawierającej obszar roboczy.</span><span class="sxs-lookup"><span data-stu-id="62b84-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="62b84-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="62b84-115">-WorkspaceName</span></span>
<span data-ttu-id="62b84-116">Określa nazwę obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="62b84-116">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="62b84-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62b84-117">CommonParameters</span></span>
<span data-ttu-id="62b84-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62b84-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62b84-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62b84-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62b84-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="62b84-120">INPUTS</span></span>

### <span data-ttu-id="62b84-121">System.String</span><span class="sxs-lookup"><span data-stu-id="62b84-121">System.String</span></span>

## <span data-ttu-id="62b84-122">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="62b84-122">OUTPUTS</span></span>

### <span data-ttu-id="62b84-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="62b84-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack</span></span>

## <span data-ttu-id="62b84-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="62b84-124">NOTES</span></span>

## <span data-ttu-id="62b84-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="62b84-125">RELATED LINKS</span></span>

[<span data-ttu-id="62b84-126">Polecenia cmdlet usługi Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="62b84-126">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


