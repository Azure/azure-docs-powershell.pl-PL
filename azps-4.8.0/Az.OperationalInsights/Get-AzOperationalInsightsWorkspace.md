---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: F94415DA-1A4A-4D37-A626-1EDF5D1EFE74
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 1a0d36c2e871bd0495216bce18d84dff60e1044d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063274"
---
# <span data-ttu-id="80f92-101">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="80f92-101">Get-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="80f92-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="80f92-102">SYNOPSIS</span></span>
<span data-ttu-id="80f92-103">Pobiera informacje o obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="80f92-103">Gets information about a workspace.</span></span>

## <span data-ttu-id="80f92-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="80f92-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80f92-105">Opis</span><span class="sxs-lookup"><span data-stu-id="80f92-105">DESCRIPTION</span></span>
<span data-ttu-id="80f92-106">Polecenie cmdlet **Get-AzOperationalInsightsWorkspace** pobiera informacje o istniejącym obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="80f92-106">The **Get-AzOperationalInsightsWorkspace** cmdlet gets information about an existing workspace.</span></span>
<span data-ttu-id="80f92-107">Jeśli określisz nazwę obszaru roboczego, to polecenie cmdlet będzie pobierać informacje o tym obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="80f92-107">If you specify a workspace name, this cmdlet gets information about that workspace.</span></span>
<span data-ttu-id="80f92-108">Jeśli nie określisz nazwy, to polecenie cmdlet będzie pobierać informacje o wszystkich obszarach roboczych w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="80f92-108">If you do not specify a name, this cmdlet gets information about all workspaces in a resource group.</span></span>
<span data-ttu-id="80f92-109">Jeśli nie określisz nazwy i grupy zasobów, to polecenie cmdlet będzie pobierać informacje o wszystkich obszarach roboczych w ramach abonamentu.</span><span class="sxs-lookup"><span data-stu-id="80f92-109">If you do not specify a name and resource group, this cmdlet gets information about all workspaces in a subscription.</span></span>

## <span data-ttu-id="80f92-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="80f92-110">EXAMPLES</span></span>

### <span data-ttu-id="80f92-111">Przykład 1. Uzyskaj obszar roboczy według nazwy</span><span class="sxs-lookup"><span data-stu-id="80f92-111">Example 1: Get a workspace by name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -Name "MyWorkspace" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="80f92-112">To polecenie pobiera obszar roboczy o nazwie Moja przestrzeń robocza w grupie zasobów o nazwie ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="80f92-112">This command gets a workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="80f92-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="80f92-113">PARAMETERS</span></span>

### <span data-ttu-id="80f92-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80f92-114">-DefaultProfile</span></span>
<span data-ttu-id="80f92-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="80f92-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="80f92-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="80f92-116">-Name</span></span>
<span data-ttu-id="80f92-117">Określa nazwę obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="80f92-117">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80f92-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80f92-118">-ResourceGroupName</span></span>
<span data-ttu-id="80f92-119">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="80f92-119">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80f92-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80f92-120">CommonParameters</span></span>
<span data-ttu-id="80f92-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80f92-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80f92-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80f92-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80f92-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="80f92-123">INPUTS</span></span>

### <span data-ttu-id="80f92-124">System. String</span><span class="sxs-lookup"><span data-stu-id="80f92-124">System.String</span></span>

## <span data-ttu-id="80f92-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="80f92-125">OUTPUTS</span></span>

### <span data-ttu-id="80f92-126">Microsoft. Azure. Commands. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="80f92-126">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="80f92-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="80f92-127">NOTES</span></span>

## <span data-ttu-id="80f92-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="80f92-128">RELATED LINKS</span></span>

[<span data-ttu-id="80f92-129">Polecenia cmdlet usługi Azure Operations Insights</span><span class="sxs-lookup"><span data-stu-id="80f92-129">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


