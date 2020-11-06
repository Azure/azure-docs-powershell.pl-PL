---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 818A048F-7CBE-4845-BBC2-6420CE48199A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightsworkspaceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspaceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspaceUsage.md
ms.openlocfilehash: 091f9b57d7e40c20b52f82ec9d6c17e6d90dad3a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527998"
---
# <span data-ttu-id="3af7f-101">Get-AzureRmOperationalInsightsWorkspaceUsage</span><span class="sxs-lookup"><span data-stu-id="3af7f-101">Get-AzureRmOperationalInsightsWorkspaceUsage</span></span>

## <span data-ttu-id="3af7f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3af7f-102">SYNOPSIS</span></span>
<span data-ttu-id="3af7f-103">Pobiera dane dotyczące użycia obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="3af7f-103">Gets the usage data for a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3af7f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3af7f-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsWorkspaceUsage [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3af7f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3af7f-105">DESCRIPTION</span></span>
<span data-ttu-id="3af7f-106">Polecenie cmdlet **Get-AzureRmOperationalInsightsWorkspaceUsage** pobiera dane dotyczące użycia obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="3af7f-106">The **Get-AzureRmOperationalInsightsWorkspaceUsage** cmdlet retrieves the usage data for a workspace.</span></span>
<span data-ttu-id="3af7f-107">Dzięki temu jest to, ile danych zostało przeanalizowanych przez obszar roboczy w określonym czasie.</span><span class="sxs-lookup"><span data-stu-id="3af7f-107">This exposes how much data has been analyzed by the workspace over a certain period.</span></span>

## <span data-ttu-id="3af7f-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3af7f-108">EXAMPLES</span></span>

### <span data-ttu-id="3af7f-109">Przykład 1: pobieranie danych użycia według nazwy obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="3af7f-109">Example 1: Get usage data by workspace name</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspaceUsage -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="3af7f-110">To polecenie pobiera szczegóły użycia obszaru roboczego o nazwie Moja przestrzeń robocza w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="3af7f-110">This command gets the usage details for the workspace named MyWorkspace in the specified resource group.</span></span>

### <span data-ttu-id="3af7f-111">Przykład 2: uzyskiwanie danych dotyczących użycia przy użyciu rurociągu</span><span class="sxs-lookup"><span data-stu-id="3af7f-111">Example 2: Get usage data using the pipeline</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzureOperationalInsightsWorkspaceUsage
```

<span data-ttu-id="3af7f-112">To polecenie pobiera obszar roboczy o nazwie webworkspace za pomocą polecenia cmdlet Get-AzureRmOperationalInsightsWorkspace, a następnie przekazuje obszar roboczy do bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3af7f-112">This command gets the workspace named MyWorkSpace using the Get-AzureRmOperationalInsightsWorkspace cmdlet, and then passes the workspace to the current cmdlet.</span></span>
<span data-ttu-id="3af7f-113">Polecenie pobiera dane dotyczące użycia tego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="3af7f-113">The command gets the usage details for that workspace.</span></span>

## <span data-ttu-id="3af7f-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3af7f-114">PARAMETERS</span></span>

### <span data-ttu-id="3af7f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3af7f-115">-DefaultProfile</span></span>
<span data-ttu-id="3af7f-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="3af7f-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3af7f-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3af7f-117">-Name</span></span>
<span data-ttu-id="3af7f-118">Określa nazwę obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="3af7f-118">Specifies the workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3af7f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3af7f-119">-ResourceGroupName</span></span>
<span data-ttu-id="3af7f-120">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3af7f-120">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3af7f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3af7f-121">CommonParameters</span></span>
<span data-ttu-id="3af7f-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3af7f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3af7f-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3af7f-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3af7f-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3af7f-124">INPUTS</span></span>

### <span data-ttu-id="3af7f-125">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="3af7f-125">None</span></span>
<span data-ttu-id="3af7f-126">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="3af7f-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3af7f-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3af7f-127">OUTPUTS</span></span>

### <span data-ttu-id="3af7f-128">System. Collections. Generic. list "1 [Microsoft. Azure. Commands. OperationalInsights. modele. PSUsageMetric]</span><span class="sxs-lookup"><span data-stu-id="3af7f-128">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.OperationalInsights.Models.PSUsageMetric]</span></span>

## <span data-ttu-id="3af7f-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3af7f-129">NOTES</span></span>

## <span data-ttu-id="3af7f-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3af7f-130">RELATED LINKS</span></span>

[<span data-ttu-id="3af7f-131">Polecenia cmdlet usługi Azure Operations Insights</span><span class="sxs-lookup"><span data-stu-id="3af7f-131">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="3af7f-132">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="3af7f-132">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


