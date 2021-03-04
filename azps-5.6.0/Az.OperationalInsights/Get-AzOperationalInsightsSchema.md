---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 6A834F26-C3D1-46DA-A4A6-1BB5B69291D0
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/get-azoperationalinsightsschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSchema.md
ms.openlocfilehash: 7f177b94b851f1a3702a153032c715f81badbcc3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008682"
---
# <span data-ttu-id="76ee5-101">Get-AzOperationalInsightsSchema</span><span class="sxs-lookup"><span data-stu-id="76ee5-101">Get-AzOperationalInsightsSchema</span></span>

## <span data-ttu-id="76ee5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76ee5-102">SYNOPSIS</span></span>
<span data-ttu-id="76ee5-103">Zwraca schemat skojarzony z obszarem roboczym.</span><span class="sxs-lookup"><span data-stu-id="76ee5-103">Returns the schema associated with a workspace.</span></span>

## <span data-ttu-id="76ee5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="76ee5-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsSchema [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76ee5-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="76ee5-105">DESCRIPTION</span></span>
<span data-ttu-id="76ee5-106">Polecenie **cmdlet Get-AzOperationalInsightsSchema** zwraca schemat skojarzony z określonym obszarem roboczym w tej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="76ee5-106">The **Get-AzOperationalInsightsSchema** cmdlet returns the schema associated with the specified workspace within that resource group.</span></span>

## <span data-ttu-id="76ee5-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="76ee5-107">EXAMPLES</span></span>

### <span data-ttu-id="76ee5-108">Przykład 1. Uzyskiwanie schematów dla obszaru roboczego programu Groove</span><span class="sxs-lookup"><span data-stu-id="76ee5-108">Example 1: Get the schemas for a workspace</span></span>
```
PS C:\>Get-AzOperationalInsightsSchema -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="76ee5-109">To polecenie pobiera schematy skojarzone z obszarem roboczym.</span><span class="sxs-lookup"><span data-stu-id="76ee5-109">This command gets the schemas associated with a workspace.</span></span>

## <span data-ttu-id="76ee5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="76ee5-110">PARAMETERS</span></span>

### <span data-ttu-id="76ee5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76ee5-111">-DefaultProfile</span></span>
<span data-ttu-id="76ee5-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="76ee5-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="76ee5-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76ee5-113">-ResourceGroupName</span></span>
<span data-ttu-id="76ee5-114">Określa nazwę grupy zasobów platformy Azure zawierającej obszar roboczy.</span><span class="sxs-lookup"><span data-stu-id="76ee5-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="76ee5-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="76ee5-115">-WorkspaceName</span></span>
<span data-ttu-id="76ee5-116">Określa nazwę obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="76ee5-116">Specifies a workspace name.</span></span>

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

### <span data-ttu-id="76ee5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76ee5-117">CommonParameters</span></span>
<span data-ttu-id="76ee5-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76ee5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76ee5-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76ee5-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76ee5-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="76ee5-120">INPUTS</span></span>

### <span data-ttu-id="76ee5-121">System.String</span><span class="sxs-lookup"><span data-stu-id="76ee5-121">System.String</span></span>

## <span data-ttu-id="76ee5-122">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="76ee5-122">OUTPUTS</span></span>

### <span data-ttu-id="76ee5-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSchemaResponse</span><span class="sxs-lookup"><span data-stu-id="76ee5-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSchemaResponse</span></span>

## <span data-ttu-id="76ee5-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="76ee5-124">NOTES</span></span>

## <span data-ttu-id="76ee5-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="76ee5-125">RELATED LINKS</span></span>

[<span data-ttu-id="76ee5-126">Polecenia cmdlet usługi Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="76ee5-126">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


