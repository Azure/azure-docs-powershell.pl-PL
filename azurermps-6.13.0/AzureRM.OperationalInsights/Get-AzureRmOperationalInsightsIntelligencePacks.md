---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 0F9D72C1-2E42-4A67-9FDE-6344F5DE6C30
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightsintelligencepacks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsIntelligencePacks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsIntelligencePacks.md
ms.openlocfilehash: d5877e29db7c678122af93d3e5d2d6281183e410
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716776"
---
# <span data-ttu-id="44a19-101">Get-AzureRmOperationalInsightsIntelligencePacks</span><span class="sxs-lookup"><span data-stu-id="44a19-101">Get-AzureRmOperationalInsightsIntelligencePacks</span></span>

## <span data-ttu-id="44a19-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="44a19-102">SYNOPSIS</span></span>
<span data-ttu-id="44a19-103">Pobiera dostępne pakiety analiz.</span><span class="sxs-lookup"><span data-stu-id="44a19-103">Gets the available Intelligence Packs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="44a19-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="44a19-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsIntelligencePacks [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="44a19-105">Opis</span><span class="sxs-lookup"><span data-stu-id="44a19-105">DESCRIPTION</span></span>
<span data-ttu-id="44a19-106">Polecenie cmdlet **Get-AzureRmOperationalInsightsIntelligencePacks** Pobiera dostępne pakiety analiz.</span><span class="sxs-lookup"><span data-stu-id="44a19-106">The **Get-AzureRmOperationalInsightsIntelligencePacks** cmdlet gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="44a19-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="44a19-107">EXAMPLES</span></span>

### <span data-ttu-id="44a19-108">Przykład 1: pobieranie pakietów analiz</span><span class="sxs-lookup"><span data-stu-id="44a19-108">Example 1: Get Intelligence Packs</span></span>
```
PS C:\>Get-AzureOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="44a19-109">To polecenie pobiera dostępne pakiety analiz.</span><span class="sxs-lookup"><span data-stu-id="44a19-109">This command gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="44a19-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="44a19-110">PARAMETERS</span></span>

### <span data-ttu-id="44a19-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44a19-111">-DefaultProfile</span></span>
<span data-ttu-id="44a19-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="44a19-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="44a19-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44a19-113">-ResourceGroupName</span></span>
<span data-ttu-id="44a19-114">Określa nazwę grupy zasobów platformy Azure zawierającej obszar roboczy.</span><span class="sxs-lookup"><span data-stu-id="44a19-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="44a19-115">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="44a19-115">-WorkspaceName</span></span>
<span data-ttu-id="44a19-116">Określa nazwę obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="44a19-116">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="44a19-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44a19-117">CommonParameters</span></span>
<span data-ttu-id="44a19-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44a19-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44a19-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44a19-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44a19-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="44a19-120">INPUTS</span></span>

### <span data-ttu-id="44a19-121">System. String</span><span class="sxs-lookup"><span data-stu-id="44a19-121">System.String</span></span>

## <span data-ttu-id="44a19-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="44a19-122">OUTPUTS</span></span>

### <span data-ttu-id="44a19-123">Microsoft. Azure. Commands. OperationalInsights. models. PSIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="44a19-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack</span></span>

## <span data-ttu-id="44a19-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="44a19-124">NOTES</span></span>

## <span data-ttu-id="44a19-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="44a19-125">RELATED LINKS</span></span>

[<span data-ttu-id="44a19-126">Polecenia cmdlet usługi Azure Operations Insights</span><span class="sxs-lookup"><span data-stu-id="44a19-126">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


