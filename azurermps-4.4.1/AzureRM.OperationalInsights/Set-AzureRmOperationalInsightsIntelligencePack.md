---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 23ED4D24-66BD-46E9-BB57-6E0DA679B733
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsIntelligencePack.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsIntelligencePack.md
ms.openlocfilehash: 266ee7c7dd8327a43de20faf0687e2f6a67ca6ed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716674"
---
# <span data-ttu-id="97078-101">Set-AzureRmOperationalInsightsIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="97078-101">Set-AzureRmOperationalInsightsIntelligencePack</span></span>

## <span data-ttu-id="97078-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="97078-102">SYNOPSIS</span></span>
<span data-ttu-id="97078-103">Włączanie lub wyłączanie określonego pakietu analiz.</span><span class="sxs-lookup"><span data-stu-id="97078-103">Enables or disables the specified Intelligence Pack.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97078-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="97078-104">SYNTAX</span></span>

```
Set-AzureRmOperationalInsightsIntelligencePack [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-IntelligencePackName] <String> [-Enabled] <Boolean> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="97078-105">Opis</span><span class="sxs-lookup"><span data-stu-id="97078-105">DESCRIPTION</span></span>
<span data-ttu-id="97078-106">Polecenie cmdlet **Set-AzureRmOperationalInsightsIntelligencePack** umożliwia włączenie określonego pakietu analiz, *Jeśli jest* ustawiony na $true i wyłączenie go, jeśli *włączono* opcję $false.</span><span class="sxs-lookup"><span data-stu-id="97078-106">The **Set-AzureRmOperationalInsightsIntelligencePack** cmdlet enables the specified Intelligence Pack if *Enabled* is set to $True and disables it if *Enabled* is set to $False.</span></span>

## <span data-ttu-id="97078-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="97078-107">EXAMPLES</span></span>

### <span data-ttu-id="97078-108">Przykład 1: Ustawianie pakietów analiz</span><span class="sxs-lookup"><span data-stu-id="97078-108">Example 1: Set Intelligence Packs</span></span>
```
PS C:\>Set-AzureOperationalInsightsIntelligencePack -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -IntelligencePackName "ContosoWorkspace" -Enabled $True
```

<span data-ttu-id="97078-109">To polecenie umożliwia włączenie określonego pakietu analiz.</span><span class="sxs-lookup"><span data-stu-id="97078-109">This command enables the specified Intelligence Pack.</span></span>

## <span data-ttu-id="97078-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="97078-110">PARAMETERS</span></span>

### <span data-ttu-id="97078-111">-Enabled</span><span class="sxs-lookup"><span data-stu-id="97078-111">-Enabled</span></span>
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

### <span data-ttu-id="97078-112">-IntelligencePackName</span><span class="sxs-lookup"><span data-stu-id="97078-112">-IntelligencePackName</span></span>
<span data-ttu-id="97078-113">Określa nazwę pakietu analizy.</span><span class="sxs-lookup"><span data-stu-id="97078-113">Specifies the Intelligence Pack name.</span></span>

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

### <span data-ttu-id="97078-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97078-114">-ResourceGroupName</span></span>
<span data-ttu-id="97078-115">Określa nazwę grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="97078-115">Specifies the resource group name</span></span>

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

### <span data-ttu-id="97078-116">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="97078-116">-WorkspaceName</span></span>
<span data-ttu-id="97078-117">Określa nazwę obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="97078-117">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="97078-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97078-118">-DefaultProfile</span></span>
<span data-ttu-id="97078-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="97078-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="97078-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97078-120">CommonParameters</span></span>
<span data-ttu-id="97078-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97078-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97078-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97078-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97078-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="97078-123">INPUTS</span></span>

## <span data-ttu-id="97078-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="97078-124">OUTPUTS</span></span>

## <span data-ttu-id="97078-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="97078-125">NOTES</span></span>

## <span data-ttu-id="97078-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="97078-126">RELATED LINKS</span></span>

[<span data-ttu-id="97078-127">Polecenia cmdlet usługi Azure Operations Insights</span><span class="sxs-lookup"><span data-stu-id="97078-127">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


