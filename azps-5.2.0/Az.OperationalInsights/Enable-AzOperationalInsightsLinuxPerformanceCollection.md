---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 10141D75-B58D-42B0-B0A6-92FF630E534C
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/enable-azoperationalinsightslinuxperformancecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsLinuxPerformanceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsLinuxPerformanceCollection.md
ms.openlocfilehash: 3a914aa970282d5157c9c72de0e328d7b927a238
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345841"
---
# <span data-ttu-id="cc9da-101">Enable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="cc9da-101">Enable-AzOperationalInsightsLinuxPerformanceCollection</span></span>

## <span data-ttu-id="cc9da-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cc9da-102">SYNOPSIS</span></span>
<span data-ttu-id="cc9da-103">Rozpoczyna zbieranie liczników wydajności z komputerów z systemem Linux.</span><span class="sxs-lookup"><span data-stu-id="cc9da-103">Starts collection of performance counters from Linux computers.</span></span>

## <span data-ttu-id="cc9da-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cc9da-104">SYNTAX</span></span>

### <span data-ttu-id="cc9da-105">ByWorkspaceName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="cc9da-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzOperationalInsightsLinuxPerformanceCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc9da-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="cc9da-106">ByWorkspaceObject</span></span>
```
Enable-AzOperationalInsightsLinuxPerformanceCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc9da-107">Opis</span><span class="sxs-lookup"><span data-stu-id="cc9da-107">DESCRIPTION</span></span>
<span data-ttu-id="cc9da-108">Polecenie cmdlet **enable-AzOperationalInsightsLinuxPerformanceCollection** rozpoczyna zbieranie liczników wydajności z podłączonych komputerów Linux w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="cc9da-108">The **Enable-AzOperationalInsightsLinuxPerformanceCollection** cmdlet starts collection of performance counters from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="cc9da-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cc9da-109">EXAMPLES</span></span>

## <span data-ttu-id="cc9da-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cc9da-110">PARAMETERS</span></span>

### <span data-ttu-id="cc9da-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc9da-111">-DefaultProfile</span></span>
<span data-ttu-id="cc9da-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="cc9da-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cc9da-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc9da-113">-ResourceGroupName</span></span>
<span data-ttu-id="cc9da-114">Określa nazwę grupy zasobów zawierającej komputery z systemem Linux.</span><span class="sxs-lookup"><span data-stu-id="cc9da-114">Specifies the name of a resource group that contains Linux computers.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc9da-115">-Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="cc9da-115">-Workspace</span></span>
<span data-ttu-id="cc9da-116">Określa obszar roboczy, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc9da-116">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cc9da-117">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="cc9da-117">-WorkspaceName</span></span>
<span data-ttu-id="cc9da-118">Określa nazwę obszaru roboczego, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc9da-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc9da-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cc9da-119">-Confirm</span></span>
<span data-ttu-id="cc9da-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc9da-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc9da-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc9da-121">-WhatIf</span></span>
<span data-ttu-id="cc9da-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc9da-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc9da-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="cc9da-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc9da-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc9da-124">CommonParameters</span></span>
<span data-ttu-id="cc9da-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc9da-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc9da-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc9da-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc9da-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cc9da-127">INPUTS</span></span>

### <span data-ttu-id="cc9da-128">Microsoft. Azure. Commands. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="cc9da-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="cc9da-129">System. String</span><span class="sxs-lookup"><span data-stu-id="cc9da-129">System.String</span></span>

## <span data-ttu-id="cc9da-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cc9da-130">OUTPUTS</span></span>

### <span data-ttu-id="cc9da-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="cc9da-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="cc9da-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cc9da-132">NOTES</span></span>
* <span data-ttu-id="cc9da-133">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, operacyjne, Insights</span><span class="sxs-lookup"><span data-stu-id="cc9da-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="cc9da-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cc9da-134">RELATED LINKS</span></span>

[<span data-ttu-id="cc9da-135">Disable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="cc9da-135">Disable-AzOperationalInsightsLinuxPerformanceCollection</span></span>](./Disable-AzOperationalInsightsLinuxPerformanceCollection.md)


