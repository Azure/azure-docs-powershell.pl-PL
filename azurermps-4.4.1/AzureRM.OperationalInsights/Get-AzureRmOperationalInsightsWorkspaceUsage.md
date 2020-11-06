---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 818A048F-7CBE-4845-BBC2-6420CE48199A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspaceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspaceUsage.md
ms.openlocfilehash: dfbf5833bd045c40315cb06d2e954688229ac557
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546156"
---
# <span data-ttu-id="809c6-101">Get-AzureRmOperationalInsightsWorkspaceUsage</span><span class="sxs-lookup"><span data-stu-id="809c6-101">Get-AzureRmOperationalInsightsWorkspaceUsage</span></span>

## <span data-ttu-id="809c6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="809c6-102">SYNOPSIS</span></span>
<span data-ttu-id="809c6-103">Pobiera dane dotyczące użycia obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="809c6-103">Gets the usage data for a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="809c6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="809c6-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsWorkspaceUsage [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="809c6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="809c6-105">DESCRIPTION</span></span>
<span data-ttu-id="809c6-106">Polecenie cmdlet **Get-AzureRmOperationalInsightsWorkspaceUsage** pobiera dane dotyczące użycia obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="809c6-106">The **Get-AzureRmOperationalInsightsWorkspaceUsage** cmdlet retrieves the usage data for a workspace.</span></span>
<span data-ttu-id="809c6-107">Dzięki temu jest to, ile danych zostało przeanalizowanych przez obszar roboczy w określonym czasie.</span><span class="sxs-lookup"><span data-stu-id="809c6-107">This exposes how much data has been analyzed by the workspace over a certain period.</span></span>

## <span data-ttu-id="809c6-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="809c6-108">EXAMPLES</span></span>

### <span data-ttu-id="809c6-109">Przykład 1: pobieranie danych użycia według nazwy obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="809c6-109">Example 1: Get usage data by workspace name</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspaceUsage -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="809c6-110">To polecenie pobiera szczegóły użycia obszaru roboczego o nazwie Moja przestrzeń robocza w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="809c6-110">This command gets the usage details for the workspace named MyWorkspace in the specified resource group.</span></span>

### <span data-ttu-id="809c6-111">Przykład 2: uzyskiwanie danych dotyczących użycia przy użyciu rurociągu</span><span class="sxs-lookup"><span data-stu-id="809c6-111">Example 2: Get usage data using the pipeline</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzureOperationalInsightsWorkspaceUsage
```

<span data-ttu-id="809c6-112">To polecenie pobiera obszar roboczy o nazwie webworkspace za pomocą polecenia cmdlet Get-AzureRmOperationalInsightsWorkspace, a następnie przekazuje obszar roboczy do bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="809c6-112">This command gets the workspace named MyWorkSpace using the Get-AzureRmOperationalInsightsWorkspace cmdlet, and then passes the workspace to the current cmdlet.</span></span>
<span data-ttu-id="809c6-113">Polecenie pobiera dane dotyczące użycia tego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="809c6-113">The command gets the usage details for that workspace.</span></span>

## <span data-ttu-id="809c6-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="809c6-114">PARAMETERS</span></span>

### <span data-ttu-id="809c6-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="809c6-115">-Name</span></span>
<span data-ttu-id="809c6-116">Określa nazwę obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="809c6-116">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="809c6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="809c6-117">-ResourceGroupName</span></span>
<span data-ttu-id="809c6-118">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="809c6-118">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="809c6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="809c6-119">-DefaultProfile</span></span>
<span data-ttu-id="809c6-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="809c6-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="809c6-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="809c6-121">CommonParameters</span></span>
<span data-ttu-id="809c6-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="809c6-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="809c6-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="809c6-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="809c6-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="809c6-124">INPUTS</span></span>

## <span data-ttu-id="809c6-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="809c6-125">OUTPUTS</span></span>

### <span data-ttu-id="809c6-126">System. Collections. Generic. list "1 [Microsoft. Azure. Commands. OperationalInsights. modele. PSUsageMetric]</span><span class="sxs-lookup"><span data-stu-id="809c6-126">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.OperationalInsights.Models.PSUsageMetric]</span></span>

## <span data-ttu-id="809c6-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="809c6-127">NOTES</span></span>

## <span data-ttu-id="809c6-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="809c6-128">RELATED LINKS</span></span>

[<span data-ttu-id="809c6-129">Polecenia cmdlet usługi Azure Operations Insights</span><span class="sxs-lookup"><span data-stu-id="809c6-129">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="809c6-130">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="809c6-130">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


