---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 818A048F-7CBE-4845-BBC2-6420CE48199A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspaceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceUsage.md
ms.openlocfilehash: 88a416f48bc94756c24295f0db3cce1efdfc8ffe
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94318960"
---
# <span data-ttu-id="40038-101">Get-AzOperationalInsightsWorkspaceUsage</span><span class="sxs-lookup"><span data-stu-id="40038-101">Get-AzOperationalInsightsWorkspaceUsage</span></span>

## <span data-ttu-id="40038-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="40038-102">SYNOPSIS</span></span>
<span data-ttu-id="40038-103">Pobiera dane dotyczące użycia obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="40038-103">Gets the usage data for a workspace.</span></span>

## <span data-ttu-id="40038-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="40038-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspaceUsage [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40038-105">Opis</span><span class="sxs-lookup"><span data-stu-id="40038-105">DESCRIPTION</span></span>
<span data-ttu-id="40038-106">Polecenie cmdlet **Get-AzOperationalInsightsWorkspaceUsage** pobiera dane dotyczące użycia obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="40038-106">The **Get-AzOperationalInsightsWorkspaceUsage** cmdlet retrieves the usage data for a workspace.</span></span>
<span data-ttu-id="40038-107">Dzięki temu jest to, ile danych zostało przeanalizowanych przez obszar roboczy w określonym czasie.</span><span class="sxs-lookup"><span data-stu-id="40038-107">This exposes how much data has been analyzed by the workspace over a certain period.</span></span>

## <span data-ttu-id="40038-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="40038-108">EXAMPLES</span></span>

### <span data-ttu-id="40038-109">Przykład 1: pobieranie danych użycia według nazwy obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="40038-109">Example 1: Get usage data by workspace name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspaceUsage -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="40038-110">To polecenie pobiera szczegóły użycia obszaru roboczego o nazwie Moja przestrzeń robocza w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="40038-110">This command gets the usage details for the workspace named MyWorkspace in the specified resource group.</span></span>

### <span data-ttu-id="40038-111">Przykład 2: uzyskiwanie danych dotyczących użycia przy użyciu rurociągu</span><span class="sxs-lookup"><span data-stu-id="40038-111">Example 2: Get usage data using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzOperationalInsightsWorkspaceUsage
```

<span data-ttu-id="40038-112">To polecenie pobiera obszar roboczy o nazwie webworkspace za pomocą polecenia cmdlet Get-AzOperationalInsightsWorkspace, a następnie przekazuje obszar roboczy do bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40038-112">This command gets the workspace named MyWorkSpace using the Get-AzOperationalInsightsWorkspace cmdlet, and then passes the workspace to the current cmdlet.</span></span>
<span data-ttu-id="40038-113">Polecenie pobiera dane dotyczące użycia tego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="40038-113">The command gets the usage details for that workspace.</span></span>

## <span data-ttu-id="40038-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="40038-114">PARAMETERS</span></span>

### <span data-ttu-id="40038-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40038-115">-DefaultProfile</span></span>
<span data-ttu-id="40038-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="40038-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="40038-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="40038-117">-Name</span></span>
<span data-ttu-id="40038-118">Określa nazwę obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="40038-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="40038-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40038-119">-ResourceGroupName</span></span>
<span data-ttu-id="40038-120">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="40038-120">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="40038-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40038-121">CommonParameters</span></span>
<span data-ttu-id="40038-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40038-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40038-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40038-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40038-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="40038-124">INPUTS</span></span>

### <span data-ttu-id="40038-125">System. String</span><span class="sxs-lookup"><span data-stu-id="40038-125">System.String</span></span>

## <span data-ttu-id="40038-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="40038-126">OUTPUTS</span></span>

### <span data-ttu-id="40038-127">Microsoft. Azure. Commands. OperationalInsights. models. PSUsageMetric</span><span class="sxs-lookup"><span data-stu-id="40038-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSUsageMetric</span></span>

## <span data-ttu-id="40038-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="40038-128">NOTES</span></span>

## <span data-ttu-id="40038-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="40038-129">RELATED LINKS</span></span>

[<span data-ttu-id="40038-130">Polecenia cmdlet usługi Azure Operations Insights</span><span class="sxs-lookup"><span data-stu-id="40038-130">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="40038-131">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="40038-131">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


