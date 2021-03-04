---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 10141D75-B58D-42B0-B0A6-92FF630E534C
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/enable-azoperationalinsightslinuxperformancecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsLinuxPerformanceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsLinuxPerformanceCollection.md
ms.openlocfilehash: 85ff01bdbdf454f498366b33d4684532f8382c7d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997550"
---
# <span data-ttu-id="41487-101">Enable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="41487-101">Enable-AzOperationalInsightsLinuxPerformanceCollection</span></span>

## <span data-ttu-id="41487-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41487-102">SYNOPSIS</span></span>
<span data-ttu-id="41487-103">Uruchamia zbieranie liczników wydajności z komputerów z systemem Linux.</span><span class="sxs-lookup"><span data-stu-id="41487-103">Starts collection of performance counters from Linux computers.</span></span>

## <span data-ttu-id="41487-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="41487-104">SYNTAX</span></span>

### <span data-ttu-id="41487-105">ByWorkspaceName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="41487-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzOperationalInsightsLinuxPerformanceCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41487-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="41487-106">ByWorkspaceObject</span></span>
```
Enable-AzOperationalInsightsLinuxPerformanceCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41487-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="41487-107">DESCRIPTION</span></span>
<span data-ttu-id="41487-108">Polecenie cmdlet **Enable-AzOperationalInsightsLinuxPerformanceCollection** uruchamia kolekcję liczników wydajności z połączonych komputerów z systemem Linux w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="41487-108">The **Enable-AzOperationalInsightsLinuxPerformanceCollection** cmdlet starts collection of performance counters from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="41487-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="41487-109">EXAMPLES</span></span>

## <span data-ttu-id="41487-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="41487-110">PARAMETERS</span></span>

### <span data-ttu-id="41487-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41487-111">-DefaultProfile</span></span>
<span data-ttu-id="41487-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="41487-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="41487-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41487-113">-ResourceGroupName</span></span>
<span data-ttu-id="41487-114">Określa nazwę grupy zasobów zawierającej komputery z systemem Linux.</span><span class="sxs-lookup"><span data-stu-id="41487-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="41487-115">— Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="41487-115">-Workspace</span></span>
<span data-ttu-id="41487-116">Określa obszar roboczy, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41487-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="41487-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="41487-117">-WorkspaceName</span></span>
<span data-ttu-id="41487-118">Określa nazwę obszaru roboczego, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41487-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="41487-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="41487-119">-Confirm</span></span>
<span data-ttu-id="41487-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="41487-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41487-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41487-121">-WhatIf</span></span>
<span data-ttu-id="41487-122">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41487-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41487-123">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="41487-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41487-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41487-124">CommonParameters</span></span>
<span data-ttu-id="41487-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41487-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41487-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41487-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41487-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="41487-127">INPUTS</span></span>

### <span data-ttu-id="41487-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="41487-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="41487-129">System.String</span><span class="sxs-lookup"><span data-stu-id="41487-129">System.String</span></span>

## <span data-ttu-id="41487-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="41487-130">OUTPUTS</span></span>

### <span data-ttu-id="41487-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="41487-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="41487-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="41487-132">NOTES</span></span>
* <span data-ttu-id="41487-133">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, operacyjny, insights</span><span class="sxs-lookup"><span data-stu-id="41487-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="41487-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="41487-134">RELATED LINKS</span></span>

[<span data-ttu-id="41487-135">Disable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="41487-135">Disable-AzOperationalInsightsLinuxPerformanceCollection</span></span>](./Disable-AzOperationalInsightsLinuxPerformanceCollection.md)


