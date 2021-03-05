---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 112D5C69-3F4F-4BB6-9DA4-52757146B0EF
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspacesharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceSharedKey.md
ms.openlocfilehash: 2cf7f548db74a7c7393fcd52bb7183c54f5f4e60
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001002"
---
# <span data-ttu-id="df548-101">Get-AzOperationalInsightsWorkspaceSharedKey</span><span class="sxs-lookup"><span data-stu-id="df548-101">Get-AzOperationalInsightsWorkspaceSharedKey</span></span>

## <span data-ttu-id="df548-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df548-102">SYNOPSIS</span></span>
<span data-ttu-id="df548-103">Pobiera klucze udostępnione dla obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="df548-103">Gets the shared keys for a workspace.</span></span>

## <span data-ttu-id="df548-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="df548-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspaceSharedKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="df548-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="df548-105">DESCRIPTION</span></span>
<span data-ttu-id="df548-106">Polecenie **cmdlet Get-AzOperationalInsightsWorkspaceSharedKey** wyświetla listę kluczy udostępnionych obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="df548-106">The **Get-AzOperationalInsightsWorkspaceSharedKey** cmdlet lists the shared keys for a workspace.</span></span>
<span data-ttu-id="df548-107">Klucze są używane do łączenia agentów szczegółowych informacji operacyjnych z obszarem roboczym.</span><span class="sxs-lookup"><span data-stu-id="df548-107">The keys are used to connect Operational Insights agents to the workspace.</span></span>

## <span data-ttu-id="df548-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="df548-108">EXAMPLES</span></span>

### <span data-ttu-id="df548-109">Przykład 1. Uzyskiwanie kluczy udostępnionych według nazwy obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="df548-109">Example 1: Get shared keys by workspace name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspaceSharedKey -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="df548-110">To polecenie pobiera klucze udostępnione dla obszaru roboczego o nazwie MyWorkspace w grupie zasobów o nazwie ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="df548-110">This command gets the shared keys for the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="df548-111">Przykład 2. Uzyskiwanie kluczy udostępnionych przy użyciu potoku</span><span class="sxs-lookup"><span data-stu-id="df548-111">Example 2: Get shared keys by using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzOperationalInsightsWorkspaceSharedKey
```

<span data-ttu-id="df548-112">To polecenie pobiera obszar roboczy o nazwie MyWorkspace za pomocą polecenia cmdlet programu Get-AzOperationalInsightsWorkspace, Get-AzOperationalInsightsWorkspace następnie przekazuje go do polecenia cmdlet **Get-AzOperationalInsightsWorkspaceSharedKey.**</span><span class="sxs-lookup"><span data-stu-id="df548-112">This command gets the workspace named MyWorkspace using the Get-AzOperationalInsightsWorkspace cmdlet, and then passes the workspace to the **Get-AzOperationalInsightsWorkspaceSharedKey** cmdlet.</span></span>
<span data-ttu-id="df548-113">Polecenie pobiera klucze udostępnione dla tego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="df548-113">The command gets the shared keys for that workspace.</span></span>

## <span data-ttu-id="df548-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="df548-114">PARAMETERS</span></span>

### <span data-ttu-id="df548-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df548-115">-DefaultProfile</span></span>
<span data-ttu-id="df548-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="df548-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="df548-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="df548-117">-Name</span></span>
<span data-ttu-id="df548-118">Określa nazwę obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="df548-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="df548-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df548-119">-ResourceGroupName</span></span>
<span data-ttu-id="df548-120">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="df548-120">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="df548-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df548-121">CommonParameters</span></span>
<span data-ttu-id="df548-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df548-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df548-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df548-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df548-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="df548-124">INPUTS</span></span>

### <span data-ttu-id="df548-125">System.String</span><span class="sxs-lookup"><span data-stu-id="df548-125">System.String</span></span>

## <span data-ttu-id="df548-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="df548-126">OUTPUTS</span></span>

### <span data-ttu-id="df548-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspaceKeys</span><span class="sxs-lookup"><span data-stu-id="df548-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspaceKeys</span></span>

## <span data-ttu-id="df548-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="df548-128">NOTES</span></span>

## <span data-ttu-id="df548-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="df548-129">RELATED LINKS</span></span>

[<span data-ttu-id="df548-130">Polecenia cmdlet usługi Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="df548-130">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="df548-131">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="df548-131">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


