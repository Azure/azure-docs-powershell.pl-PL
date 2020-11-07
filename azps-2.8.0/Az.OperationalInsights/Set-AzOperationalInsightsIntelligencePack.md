---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 23ED4D24-66BD-46E9-BB57-6E0DA679B733
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightsintelligencepack
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsIntelligencePack.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsIntelligencePack.md
ms.openlocfilehash: 5e54e18a0b35a3845c65d76b564924e6c17a8ca0
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/13/2020
ms.locfileid: "93897093"
---
# <span data-ttu-id="e246c-101">Set-AzOperationalInsightsIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="e246c-101">Set-AzOperationalInsightsIntelligencePack</span></span>

## <span data-ttu-id="e246c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e246c-102">SYNOPSIS</span></span>
<span data-ttu-id="e246c-103">Włączanie lub wyłączanie określonego pakietu analiz.</span><span class="sxs-lookup"><span data-stu-id="e246c-103">Enables or disables the specified Intelligence Pack.</span></span>

## <span data-ttu-id="e246c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e246c-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsIntelligencePack [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-IntelligencePackName] <String> [-Enabled] <Boolean> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e246c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e246c-105">DESCRIPTION</span></span>
<span data-ttu-id="e246c-106">Polecenie cmdlet **Set-AzOperationalInsightsIntelligencePack** umożliwia włączenie określonego pakietu analiz, *Jeśli jest* ustawiony na $true i wyłączenie go, jeśli *włączono* opcję $false.</span><span class="sxs-lookup"><span data-stu-id="e246c-106">The **Set-AzOperationalInsightsIntelligencePack** cmdlet enables the specified Intelligence Pack if *Enabled* is set to $True and disables it if *Enabled* is set to $False.</span></span>

## <span data-ttu-id="e246c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e246c-107">EXAMPLES</span></span>

### <span data-ttu-id="e246c-108">Przykład 1: Ustawianie pakietów analiz</span><span class="sxs-lookup"><span data-stu-id="e246c-108">Example 1: Set Intelligence Packs</span></span>
```
PS C:\>Set-AzOperationalInsightsIntelligencePack -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -IntelligencePackName "ContosoWorkspace" -Enabled $True
```

<span data-ttu-id="e246c-109">To polecenie umożliwia włączenie określonego pakietu analiz.</span><span class="sxs-lookup"><span data-stu-id="e246c-109">This command enables the specified Intelligence Pack.</span></span>

## <span data-ttu-id="e246c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e246c-110">PARAMETERS</span></span>

### <span data-ttu-id="e246c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e246c-111">-DefaultProfile</span></span>
<span data-ttu-id="e246c-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="e246c-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e246c-113">-Enabled</span><span class="sxs-lookup"><span data-stu-id="e246c-113">-Enabled</span></span>
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

### <span data-ttu-id="e246c-114">-IntelligencePackName</span><span class="sxs-lookup"><span data-stu-id="e246c-114">-IntelligencePackName</span></span>
<span data-ttu-id="e246c-115">Określa nazwę pakietu analizy.</span><span class="sxs-lookup"><span data-stu-id="e246c-115">Specifies the Intelligence Pack name.</span></span>

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

### <span data-ttu-id="e246c-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e246c-116">-ResourceGroupName</span></span>
<span data-ttu-id="e246c-117">Określa nazwę grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="e246c-117">Specifies the resource group name</span></span>

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

### <span data-ttu-id="e246c-118">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="e246c-118">-WorkspaceName</span></span>
<span data-ttu-id="e246c-119">Określa nazwę obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="e246c-119">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="e246c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e246c-120">CommonParameters</span></span>
<span data-ttu-id="e246c-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e246c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e246c-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e246c-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e246c-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e246c-123">INPUTS</span></span>

### <span data-ttu-id="e246c-124">System. String</span><span class="sxs-lookup"><span data-stu-id="e246c-124">System.String</span></span>

### <span data-ttu-id="e246c-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e246c-125">System.Boolean</span></span>

## <span data-ttu-id="e246c-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e246c-126">OUTPUTS</span></span>

### <span data-ttu-id="e246c-127">Microsoft. Azure. Commands. OperationalInsights. models. PSIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="e246c-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack</span></span>

## <span data-ttu-id="e246c-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e246c-128">NOTES</span></span>

## <span data-ttu-id="e246c-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e246c-129">RELATED LINKS</span></span>

[<span data-ttu-id="e246c-130">Polecenia cmdlet usługi Azure Operations Insights</span><span class="sxs-lookup"><span data-stu-id="e246c-130">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)


