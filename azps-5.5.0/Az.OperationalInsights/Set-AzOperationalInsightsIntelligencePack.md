---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 23ED4D24-66BD-46E9-BB57-6E0DA679B733
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightsintelligencepack
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsIntelligencePack.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsIntelligencePack.md
ms.openlocfilehash: a8d799cec6278149cb4c08faf68584fb7968f85e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179219"
---
# <span data-ttu-id="802ac-101">Set-AzOperationalInsightsIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="802ac-101">Set-AzOperationalInsightsIntelligencePack</span></span>

## <span data-ttu-id="802ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="802ac-102">SYNOPSIS</span></span>
<span data-ttu-id="802ac-103">Włącza lub wyłącza określony pakiet analiz.</span><span class="sxs-lookup"><span data-stu-id="802ac-103">Enables or disables the specified Intelligence Pack.</span></span>

## <span data-ttu-id="802ac-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="802ac-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsIntelligencePack [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-IntelligencePackName] <String> [-Enabled] <Boolean> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="802ac-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="802ac-105">DESCRIPTION</span></span>
<span data-ttu-id="802ac-106">Polecenie **cmdlet Set-AzOperationalInsightsIntelligencePack** włącza określony  pakiet analizy, jeśli jest włączony,  jest ustawiony na $True i wyłącza go, jeśli dla ustawienia Włączone ustawiono $False.</span><span class="sxs-lookup"><span data-stu-id="802ac-106">The **Set-AzOperationalInsightsIntelligencePack** cmdlet enables the specified Intelligence Pack if *Enabled* is set to $True and disables it if *Enabled* is set to $False.</span></span>

## <span data-ttu-id="802ac-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="802ac-107">EXAMPLES</span></span>

### <span data-ttu-id="802ac-108">Przykład 1. Ustawianie pakietów analizy</span><span class="sxs-lookup"><span data-stu-id="802ac-108">Example 1: Set Intelligence Packs</span></span>
```
PS C:\>Set-AzOperationalInsightsIntelligencePack -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -IntelligencePackName "ContosoWorkspace" -Enabled $True
```

<span data-ttu-id="802ac-109">To polecenie włącza określony pakiet analiz.</span><span class="sxs-lookup"><span data-stu-id="802ac-109">This command enables the specified Intelligence Pack.</span></span>

## <span data-ttu-id="802ac-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="802ac-110">PARAMETERS</span></span>

### <span data-ttu-id="802ac-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="802ac-111">-DefaultProfile</span></span>
<span data-ttu-id="802ac-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="802ac-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="802ac-113">— włączone</span><span class="sxs-lookup"><span data-stu-id="802ac-113">-Enabled</span></span>
```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="802ac-114">-IntelligencePackName</span><span class="sxs-lookup"><span data-stu-id="802ac-114">-IntelligencePackName</span></span>
<span data-ttu-id="802ac-115">Określa nazwę pakietu analiz.</span><span class="sxs-lookup"><span data-stu-id="802ac-115">Specifies the Intelligence Pack name.</span></span>

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

### <span data-ttu-id="802ac-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="802ac-116">-ResourceGroupName</span></span>
<span data-ttu-id="802ac-117">Określa nazwę grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="802ac-117">Specifies the resource group name</span></span>

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

### <span data-ttu-id="802ac-118">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="802ac-118">-WorkspaceName</span></span>
<span data-ttu-id="802ac-119">Określa nazwę obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="802ac-119">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="802ac-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="802ac-120">CommonParameters</span></span>
<span data-ttu-id="802ac-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="802ac-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="802ac-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="802ac-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="802ac-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="802ac-123">INPUTS</span></span>

### <span data-ttu-id="802ac-124">System.String</span><span class="sxs-lookup"><span data-stu-id="802ac-124">System.String</span></span>

### <span data-ttu-id="802ac-125">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="802ac-125">System.Boolean</span></span>

## <span data-ttu-id="802ac-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="802ac-126">OUTPUTS</span></span>

### <span data-ttu-id="802ac-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="802ac-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack</span></span>

## <span data-ttu-id="802ac-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="802ac-128">NOTES</span></span>

## <span data-ttu-id="802ac-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="802ac-129">RELATED LINKS</span></span>

[<span data-ttu-id="802ac-130">Polecenia cmdlet usługi Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="802ac-130">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


