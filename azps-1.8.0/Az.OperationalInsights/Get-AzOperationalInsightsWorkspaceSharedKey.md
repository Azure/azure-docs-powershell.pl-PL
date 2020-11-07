---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 112D5C69-3F4F-4BB6-9DA4-52757146B0EF
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspacesharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceSharedKey.md
ms.openlocfilehash: 7328eda5e6821b7c403bf949460747fbf7d215e7
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/13/2020
ms.locfileid: "93710896"
---
# <span data-ttu-id="58141-101">Get-AzOperationalInsightsWorkspaceSharedKey</span><span class="sxs-lookup"><span data-stu-id="58141-101">Get-AzOperationalInsightsWorkspaceSharedKey</span></span>

## <span data-ttu-id="58141-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="58141-102">SYNOPSIS</span></span>
<span data-ttu-id="58141-103">Pobiera klucze współużytkowane dla obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="58141-103">Gets the shared keys for a workspace.</span></span>

## <span data-ttu-id="58141-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="58141-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspaceSharedKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58141-105">Opis</span><span class="sxs-lookup"><span data-stu-id="58141-105">DESCRIPTION</span></span>
<span data-ttu-id="58141-106">Polecenie cmdlet **Get-AzOperationalInsightsWorkspaceSharedKey** zawiera listę kluczy współużytkowanych dla obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="58141-106">The **Get-AzOperationalInsightsWorkspaceSharedKey** cmdlet lists the shared keys for a workspace.</span></span>
<span data-ttu-id="58141-107">Klucze służą do łączenia agentów usługi Insights z obszarem roboczym.</span><span class="sxs-lookup"><span data-stu-id="58141-107">The keys are used to connect Operational Insights agents to the workspace.</span></span>

## <span data-ttu-id="58141-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="58141-108">EXAMPLES</span></span>

### <span data-ttu-id="58141-109">Przykład 1: pobieranie kluczy współużytkowanych według nazwy obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="58141-109">Example 1: Get shared keys by workspace name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspaceSharedKey -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="58141-110">To polecenie pobiera klucze udostępnione dla obszaru roboczego o nazwie Moja przestrzeń robocza w grupie zasobów o nazwie ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="58141-110">This command gets the shared keys for the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="58141-111">Przykład 2: pobieranie kluczy współużytkowanych za pomocą potoku</span><span class="sxs-lookup"><span data-stu-id="58141-111">Example 2: Get shared keys by using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzOperationalInsightsWorkspaceSharedKey
```

<span data-ttu-id="58141-112">To polecenie pobiera obszar roboczy o nazwie webworkspace za pomocą polecenia cmdlet Get-AzOperationalInsightsWorkspace, a następnie przekazuje obszar roboczy do polecenia cmdlet **Get-AzOperationalInsightsWorkspaceSharedKey** .</span><span class="sxs-lookup"><span data-stu-id="58141-112">This command gets the workspace named MyWorkspace using the Get-AzOperationalInsightsWorkspace cmdlet, and then passes the workspace to the **Get-AzOperationalInsightsWorkspaceSharedKey** cmdlet.</span></span>
<span data-ttu-id="58141-113">Polecenie pobiera klucze współużytkowane dla tego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="58141-113">The command gets the shared keys for that workspace.</span></span>

## <span data-ttu-id="58141-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="58141-114">PARAMETERS</span></span>

### <span data-ttu-id="58141-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58141-115">-DefaultProfile</span></span>
<span data-ttu-id="58141-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="58141-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="58141-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="58141-117">-Name</span></span>
<span data-ttu-id="58141-118">Określa nazwę obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="58141-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="58141-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58141-119">-ResourceGroupName</span></span>
<span data-ttu-id="58141-120">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="58141-120">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="58141-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58141-121">CommonParameters</span></span>
<span data-ttu-id="58141-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58141-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58141-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58141-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58141-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="58141-124">INPUTS</span></span>

### <span data-ttu-id="58141-125">System. String</span><span class="sxs-lookup"><span data-stu-id="58141-125">System.String</span></span>

## <span data-ttu-id="58141-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="58141-126">OUTPUTS</span></span>

### <span data-ttu-id="58141-127">Microsoft. Azure. Commands. OperationalInsights. models. PSWorkspaceKeys</span><span class="sxs-lookup"><span data-stu-id="58141-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspaceKeys</span></span>

## <span data-ttu-id="58141-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="58141-128">NOTES</span></span>

## <span data-ttu-id="58141-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="58141-129">RELATED LINKS</span></span>

[<span data-ttu-id="58141-130">Polecenia cmdlet usługi Azure Operations Insights</span><span class="sxs-lookup"><span data-stu-id="58141-130">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)

[<span data-ttu-id="58141-131">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="58141-131">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


