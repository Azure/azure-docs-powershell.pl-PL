---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 6A834F26-C3D1-46DA-A4A6-1BB5B69291D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSchema.md
ms.openlocfilehash: 12c3e54725abfd5addf33a3d31edcb8f8016e9dd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179234"
---
# <span data-ttu-id="89f4b-101">Get-AzOperationalInsightsSchema</span><span class="sxs-lookup"><span data-stu-id="89f4b-101">Get-AzOperationalInsightsSchema</span></span>

## <span data-ttu-id="89f4b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89f4b-102">SYNOPSIS</span></span>
<span data-ttu-id="89f4b-103">Zwraca schemat skojarzony z obszarem roboczym.</span><span class="sxs-lookup"><span data-stu-id="89f4b-103">Returns the schema associated with a workspace.</span></span>

## <span data-ttu-id="89f4b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="89f4b-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsSchema [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89f4b-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="89f4b-105">DESCRIPTION</span></span>
<span data-ttu-id="89f4b-106">Polecenie **cmdlet Get-AzOperationalInsightsSchema** zwraca schemat skojarzony z określonym obszarem roboczym w tej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="89f4b-106">The **Get-AzOperationalInsightsSchema** cmdlet returns the schema associated with the specified workspace within that resource group.</span></span>

## <span data-ttu-id="89f4b-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="89f4b-107">EXAMPLES</span></span>

### <span data-ttu-id="89f4b-108">Przykład 1. Uzyskiwanie schematów dla obszaru roboczego programu Groove</span><span class="sxs-lookup"><span data-stu-id="89f4b-108">Example 1: Get the schemas for a workspace</span></span>
```
PS C:\>Get-AzOperationalInsightsSchema -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="89f4b-109">To polecenie pobiera schematy skojarzone z obszarem roboczym.</span><span class="sxs-lookup"><span data-stu-id="89f4b-109">This command gets the schemas associated with a workspace.</span></span>

## <span data-ttu-id="89f4b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="89f4b-110">PARAMETERS</span></span>

### <span data-ttu-id="89f4b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89f4b-111">-DefaultProfile</span></span>
<span data-ttu-id="89f4b-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="89f4b-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="89f4b-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89f4b-113">-ResourceGroupName</span></span>
<span data-ttu-id="89f4b-114">Określa nazwę grupy zasobów platformy Azure zawierającej obszar roboczy.</span><span class="sxs-lookup"><span data-stu-id="89f4b-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="89f4b-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="89f4b-115">-WorkspaceName</span></span>
<span data-ttu-id="89f4b-116">Określa nazwę obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="89f4b-116">Specifies a workspace name.</span></span>

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

### <span data-ttu-id="89f4b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89f4b-117">CommonParameters</span></span>
<span data-ttu-id="89f4b-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89f4b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89f4b-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89f4b-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89f4b-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="89f4b-120">INPUTS</span></span>

### <span data-ttu-id="89f4b-121">System.String</span><span class="sxs-lookup"><span data-stu-id="89f4b-121">System.String</span></span>

## <span data-ttu-id="89f4b-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="89f4b-122">OUTPUTS</span></span>

### <span data-ttu-id="89f4b-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSchemaResponse</span><span class="sxs-lookup"><span data-stu-id="89f4b-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSchemaResponse</span></span>

## <span data-ttu-id="89f4b-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="89f4b-124">NOTES</span></span>

## <span data-ttu-id="89f4b-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="89f4b-125">RELATED LINKS</span></span>

[<span data-ttu-id="89f4b-126">Polecenia cmdlet usługi Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="89f4b-126">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


