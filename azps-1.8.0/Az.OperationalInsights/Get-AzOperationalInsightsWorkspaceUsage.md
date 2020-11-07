---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 818A048F-7CBE-4845-BBC2-6420CE48199A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspaceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceUsage.md
ms.openlocfilehash: 04a62f4929e89dd4bff4d088d84325b0bdbb140b
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/13/2020
ms.locfileid: "93710898"
---
# <span data-ttu-id="7208d-101">Get-AzOperationalInsightsWorkspaceUsage</span><span class="sxs-lookup"><span data-stu-id="7208d-101">Get-AzOperationalInsightsWorkspaceUsage</span></span>

## <span data-ttu-id="7208d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7208d-102">SYNOPSIS</span></span>
<span data-ttu-id="7208d-103">Pobiera dane dotyczące użycia obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="7208d-103">Gets the usage data for a workspace.</span></span>

## <span data-ttu-id="7208d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7208d-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspaceUsage [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7208d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7208d-105">DESCRIPTION</span></span>
<span data-ttu-id="7208d-106">Polecenie cmdlet **Get-AzOperationalInsightsWorkspaceUsage** pobiera dane dotyczące użycia obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="7208d-106">The **Get-AzOperationalInsightsWorkspaceUsage** cmdlet retrieves the usage data for a workspace.</span></span>
<span data-ttu-id="7208d-107">Dzięki temu jest to, ile danych zostało przeanalizowanych przez obszar roboczy w określonym czasie.</span><span class="sxs-lookup"><span data-stu-id="7208d-107">This exposes how much data has been analyzed by the workspace over a certain period.</span></span>

## <span data-ttu-id="7208d-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7208d-108">EXAMPLES</span></span>

### <span data-ttu-id="7208d-109">Przykład 1: pobieranie danych użycia według nazwy obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="7208d-109">Example 1: Get usage data by workspace name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspaceUsage -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="7208d-110">To polecenie pobiera szczegóły użycia obszaru roboczego o nazwie Moja przestrzeń robocza w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="7208d-110">This command gets the usage details for the workspace named MyWorkspace in the specified resource group.</span></span>

### <span data-ttu-id="7208d-111">Przykład 2: uzyskiwanie danych dotyczących użycia przy użyciu rurociągu</span><span class="sxs-lookup"><span data-stu-id="7208d-111">Example 2: Get usage data using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzOperationalInsightsWorkspaceUsage
```

<span data-ttu-id="7208d-112">To polecenie pobiera obszar roboczy o nazwie webworkspace za pomocą polecenia cmdlet Get-AzOperationalInsightsWorkspace, a następnie przekazuje obszar roboczy do bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7208d-112">This command gets the workspace named MyWorkSpace using the Get-AzOperationalInsightsWorkspace cmdlet, and then passes the workspace to the current cmdlet.</span></span>
<span data-ttu-id="7208d-113">Polecenie pobiera dane dotyczące użycia tego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="7208d-113">The command gets the usage details for that workspace.</span></span>

## <span data-ttu-id="7208d-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7208d-114">PARAMETERS</span></span>

### <span data-ttu-id="7208d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7208d-115">-DefaultProfile</span></span>
<span data-ttu-id="7208d-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="7208d-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7208d-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7208d-117">-Name</span></span>
<span data-ttu-id="7208d-118">Określa nazwę obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="7208d-118">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7208d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7208d-119">-ResourceGroupName</span></span>
<span data-ttu-id="7208d-120">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7208d-120">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="7208d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7208d-121">CommonParameters</span></span>
<span data-ttu-id="7208d-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7208d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7208d-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7208d-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7208d-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7208d-124">INPUTS</span></span>

### <span data-ttu-id="7208d-125">System. String</span><span class="sxs-lookup"><span data-stu-id="7208d-125">System.String</span></span>

## <span data-ttu-id="7208d-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7208d-126">OUTPUTS</span></span>

### <span data-ttu-id="7208d-127">Microsoft. Azure. Commands. OperationalInsights. models. PSUsageMetric</span><span class="sxs-lookup"><span data-stu-id="7208d-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSUsageMetric</span></span>

## <span data-ttu-id="7208d-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7208d-128">NOTES</span></span>

## <span data-ttu-id="7208d-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7208d-129">RELATED LINKS</span></span>

[<span data-ttu-id="7208d-130">Polecenia cmdlet usługi Azure Operations Insights</span><span class="sxs-lookup"><span data-stu-id="7208d-130">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)

[<span data-ttu-id="7208d-131">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="7208d-131">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


