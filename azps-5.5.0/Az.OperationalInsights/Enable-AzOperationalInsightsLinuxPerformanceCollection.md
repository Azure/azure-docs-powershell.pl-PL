---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 10141D75-B58D-42B0-B0A6-92FF630E534C
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/enable-azoperationalinsightslinuxperformancecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsLinuxPerformanceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsLinuxPerformanceCollection.md
ms.openlocfilehash: 3a914aa970282d5157c9c72de0e328d7b927a238
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202362"
---
# <span data-ttu-id="8058f-101">Enable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="8058f-101">Enable-AzOperationalInsightsLinuxPerformanceCollection</span></span>

## <span data-ttu-id="8058f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8058f-102">SYNOPSIS</span></span>
<span data-ttu-id="8058f-103">Uruchamia zbieranie liczników wydajności z komputerów z systemem Linux.</span><span class="sxs-lookup"><span data-stu-id="8058f-103">Starts collection of performance counters from Linux computers.</span></span>

## <span data-ttu-id="8058f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8058f-104">SYNTAX</span></span>

### <span data-ttu-id="8058f-105">ByWorkspaceName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="8058f-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzOperationalInsightsLinuxPerformanceCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8058f-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="8058f-106">ByWorkspaceObject</span></span>
```
Enable-AzOperationalInsightsLinuxPerformanceCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8058f-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="8058f-107">DESCRIPTION</span></span>
<span data-ttu-id="8058f-108">Polecenie cmdlet **Enable-AzOperationalInsightsLinuxPerformanceCollection** uruchamia kolekcję liczników wydajności z połączonych komputerów z systemem Linux w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="8058f-108">The **Enable-AzOperationalInsightsLinuxPerformanceCollection** cmdlet starts collection of performance counters from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="8058f-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8058f-109">EXAMPLES</span></span>

## <span data-ttu-id="8058f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8058f-110">PARAMETERS</span></span>

### <span data-ttu-id="8058f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8058f-111">-DefaultProfile</span></span>
<span data-ttu-id="8058f-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="8058f-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8058f-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8058f-113">-ResourceGroupName</span></span>
<span data-ttu-id="8058f-114">Określa nazwę grupy zasobów zawierającej komputery z systemem Linux.</span><span class="sxs-lookup"><span data-stu-id="8058f-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="8058f-115">— Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="8058f-115">-Workspace</span></span>
<span data-ttu-id="8058f-116">Określa obszar roboczy, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8058f-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="8058f-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="8058f-117">-WorkspaceName</span></span>
<span data-ttu-id="8058f-118">Określa nazwę obszaru roboczego, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8058f-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="8058f-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8058f-119">-Confirm</span></span>
<span data-ttu-id="8058f-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8058f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8058f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8058f-121">-WhatIf</span></span>
<span data-ttu-id="8058f-122">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8058f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8058f-123">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="8058f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8058f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8058f-124">CommonParameters</span></span>
<span data-ttu-id="8058f-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8058f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8058f-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8058f-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8058f-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8058f-127">INPUTS</span></span>

### <span data-ttu-id="8058f-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="8058f-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="8058f-129">System.String</span><span class="sxs-lookup"><span data-stu-id="8058f-129">System.String</span></span>

## <span data-ttu-id="8058f-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8058f-130">OUTPUTS</span></span>

### <span data-ttu-id="8058f-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="8058f-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="8058f-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8058f-132">NOTES</span></span>
* <span data-ttu-id="8058f-133">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, operacyjny, insights</span><span class="sxs-lookup"><span data-stu-id="8058f-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="8058f-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8058f-134">RELATED LINKS</span></span>

[<span data-ttu-id="8058f-135">Disable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="8058f-135">Disable-AzOperationalInsightsLinuxPerformanceCollection</span></span>](./Disable-AzOperationalInsightsLinuxPerformanceCollection.md)


