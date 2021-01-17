---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 47AFBAC7-8818-4788-B685-7AB4DCD6C2DE
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/disable-azoperationalinsightslinuxperformancecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsLinuxPerformanceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsLinuxPerformanceCollection.md
ms.openlocfilehash: 92fbc7e67bb81422e021a23810f3045b5cf32cba
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98350605"
---
# <span data-ttu-id="95388-101">Disable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="95388-101">Disable-AzOperationalInsightsLinuxPerformanceCollection</span></span>

## <span data-ttu-id="95388-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="95388-102">SYNOPSIS</span></span>
<span data-ttu-id="95388-103">Zatrzymuje zbieranie liczników wydajności z komputerów z systemem Linux.</span><span class="sxs-lookup"><span data-stu-id="95388-103">Stops collection of performance counters from Linux computers.</span></span>

## <span data-ttu-id="95388-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="95388-104">SYNTAX</span></span>

### <span data-ttu-id="95388-105">ByWorkspaceName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="95388-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzOperationalInsightsLinuxPerformanceCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95388-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="95388-106">ByWorkspaceObject</span></span>
```
Disable-AzOperationalInsightsLinuxPerformanceCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95388-107">Opis</span><span class="sxs-lookup"><span data-stu-id="95388-107">DESCRIPTION</span></span>
<span data-ttu-id="95388-108">Polecenie cmdlet **disable-AzOperationalInsightsLinuxPerformanceCollection** zatrzymuje zbieranie liczników wydajności z połączonych komputerów z systemem Linux w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="95388-108">The **Disable-AzOperationalInsightsLinuxPerformanceCollection** cmdlet stops collection of performance counters from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="95388-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="95388-109">EXAMPLES</span></span>

## <span data-ttu-id="95388-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="95388-110">PARAMETERS</span></span>

### <span data-ttu-id="95388-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95388-111">-DefaultProfile</span></span>
<span data-ttu-id="95388-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="95388-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="95388-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95388-113">-ResourceGroupName</span></span>
<span data-ttu-id="95388-114">Określa nazwę grupy zasobów zawierającej komputery z systemem Linux.</span><span class="sxs-lookup"><span data-stu-id="95388-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="95388-115">-Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="95388-115">-Workspace</span></span>
<span data-ttu-id="95388-116">Określa obszar roboczy, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="95388-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="95388-117">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="95388-117">-WorkspaceName</span></span>
<span data-ttu-id="95388-118">Określa nazwę obszaru roboczego, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="95388-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="95388-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="95388-119">-Confirm</span></span>
<span data-ttu-id="95388-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="95388-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95388-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95388-121">-WhatIf</span></span>
<span data-ttu-id="95388-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="95388-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95388-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="95388-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95388-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95388-124">CommonParameters</span></span>
<span data-ttu-id="95388-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95388-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95388-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95388-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95388-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="95388-127">INPUTS</span></span>

### <span data-ttu-id="95388-128">Microsoft. Azure. Commands. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="95388-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="95388-129">System. String</span><span class="sxs-lookup"><span data-stu-id="95388-129">System.String</span></span>

## <span data-ttu-id="95388-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="95388-130">OUTPUTS</span></span>

### <span data-ttu-id="95388-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="95388-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="95388-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="95388-132">NOTES</span></span>
* <span data-ttu-id="95388-133">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, operacyjne, Insights</span><span class="sxs-lookup"><span data-stu-id="95388-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="95388-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="95388-134">RELATED LINKS</span></span>

[<span data-ttu-id="95388-135">Enable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="95388-135">Enable-AzOperationalInsightsLinuxPerformanceCollection</span></span>](./Enable-AzOperationalInsightsLinuxPerformanceCollection.md)

[<span data-ttu-id="95388-136">Nowe — AzOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="95388-136">New-AzOperationalInsightsLinuxSyslogDataSource</span></span>](./New-AzOperationalInsightsLinuxSyslogDataSource.md)


