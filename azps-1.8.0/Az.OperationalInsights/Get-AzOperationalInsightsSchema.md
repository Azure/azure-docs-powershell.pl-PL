---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 6A834F26-C3D1-46DA-A4A6-1BB5B69291D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSchema.md
ms.openlocfilehash: 077272f15d37645de86f144424fddd7e5f026908
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/13/2020
ms.locfileid: "93710902"
---
# <span data-ttu-id="b7ea4-101">Get-AzOperationalInsightsSchema</span><span class="sxs-lookup"><span data-stu-id="b7ea4-101">Get-AzOperationalInsightsSchema</span></span>

## <span data-ttu-id="b7ea4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b7ea4-102">SYNOPSIS</span></span>
<span data-ttu-id="b7ea4-103">Zwraca schemat skojarzony z obszarem roboczym.</span><span class="sxs-lookup"><span data-stu-id="b7ea4-103">Returns the schema associated with a workspace.</span></span>

## <span data-ttu-id="b7ea4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b7ea4-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsSchema [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7ea4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b7ea4-105">DESCRIPTION</span></span>
<span data-ttu-id="b7ea4-106">Polecenie cmdlet **Get-AzOperationalInsightsSchema** zwraca schemat skojarzony z określonym obszarem roboczym w tej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="b7ea4-106">The **Get-AzOperationalInsightsSchema** cmdlet returns the schema associated with the specified workspace within that resource group.</span></span>

## <span data-ttu-id="b7ea4-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b7ea4-107">EXAMPLES</span></span>

### <span data-ttu-id="b7ea4-108">Przykład 1. Pobieranie schematów dla obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="b7ea4-108">Example 1: Get the schemas for a workspace</span></span>
```
PS C:\>Get-AzOperationalInsightsSchema -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="b7ea4-109">To polecenie umożliwia pobieranie schematów skojarzonych z obszarem roboczym.</span><span class="sxs-lookup"><span data-stu-id="b7ea4-109">This command gets the schemas associated with a workspace.</span></span>

## <span data-ttu-id="b7ea4-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b7ea4-110">PARAMETERS</span></span>

### <span data-ttu-id="b7ea4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7ea4-111">-DefaultProfile</span></span>
<span data-ttu-id="b7ea4-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="b7ea4-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b7ea4-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7ea4-113">-ResourceGroupName</span></span>
<span data-ttu-id="b7ea4-114">Określa nazwę grupy zasobów platformy Azure zawierającej obszar roboczy.</span><span class="sxs-lookup"><span data-stu-id="b7ea4-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="b7ea4-115">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="b7ea4-115">-WorkspaceName</span></span>
<span data-ttu-id="b7ea4-116">Określa nazwę obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="b7ea4-116">Specifies a workspace name.</span></span>

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

### <span data-ttu-id="b7ea4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7ea4-117">CommonParameters</span></span>
<span data-ttu-id="b7ea4-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7ea4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7ea4-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7ea4-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7ea4-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b7ea4-120">INPUTS</span></span>

### <span data-ttu-id="b7ea4-121">System. String</span><span class="sxs-lookup"><span data-stu-id="b7ea4-121">System.String</span></span>

## <span data-ttu-id="b7ea4-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b7ea4-122">OUTPUTS</span></span>

### <span data-ttu-id="b7ea4-123">Microsoft. Azure. Commands. OperationalInsights. models. PSSearchGetSchemaResponse</span><span class="sxs-lookup"><span data-stu-id="b7ea4-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSchemaResponse</span></span>

## <span data-ttu-id="b7ea4-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b7ea4-124">NOTES</span></span>

## <span data-ttu-id="b7ea4-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b7ea4-125">RELATED LINKS</span></span>

[<span data-ttu-id="b7ea4-126">Polecenia cmdlet usługi Azure Operations Insights</span><span class="sxs-lookup"><span data-stu-id="b7ea4-126">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)


