---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 95B54065-B6CC-4D10-A747-28CE3F412ABF
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/disable-azoperationalinsightsiislogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsIISLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsIISLogCollection.md
ms.openlocfilehash: 71a0089b4f593032404b71f17ba432486f5498d7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193226"
---
# <span data-ttu-id="2af35-101">Disable-AzOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="2af35-101">Disable-AzOperationalInsightsIISLogCollection</span></span>

## <span data-ttu-id="2af35-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2af35-102">SYNOPSIS</span></span>
<span data-ttu-id="2af35-103">Zatrzymuje zbieranie dzienników usług IIS z komputerów.</span><span class="sxs-lookup"><span data-stu-id="2af35-103">Stops collection of IIS logs from computers.</span></span>

## <span data-ttu-id="2af35-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2af35-104">SYNTAX</span></span>

### <span data-ttu-id="2af35-105">ByWorkspaceName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="2af35-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzOperationalInsightsIISLogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2af35-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="2af35-106">ByWorkspaceObject</span></span>
```
Disable-AzOperationalInsightsIISLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2af35-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="2af35-107">DESCRIPTION</span></span>
<span data-ttu-id="2af35-108">Polecenie cmdlet **Disable-AzOperationalInsightsIISLogCollection** zatrzymuje kolekcję dzienników programu Internet Information Services (IIS) z połączonych komputerów w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="2af35-108">The **Disable-AzOperationalInsightsIISLogCollection** cmdlet stops collection of Internet Information Services (IIS) logs from connected computers in a workspace.</span></span>

## <span data-ttu-id="2af35-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2af35-109">EXAMPLES</span></span>

## <span data-ttu-id="2af35-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2af35-110">PARAMETERS</span></span>

### <span data-ttu-id="2af35-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2af35-111">-DefaultProfile</span></span>
<span data-ttu-id="2af35-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="2af35-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2af35-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2af35-113">-ResourceGroupName</span></span>
<span data-ttu-id="2af35-114">Określa nazwę grupy zasobów zawierającej komputery.</span><span class="sxs-lookup"><span data-stu-id="2af35-114">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="2af35-115">— Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="2af35-115">-Workspace</span></span>
<span data-ttu-id="2af35-116">Określa obszar roboczy, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2af35-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="2af35-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2af35-117">-WorkspaceName</span></span>
<span data-ttu-id="2af35-118">Określa nazwę obszaru roboczego, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2af35-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="2af35-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2af35-119">-Confirm</span></span>
<span data-ttu-id="2af35-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2af35-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2af35-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2af35-121">-WhatIf</span></span>
<span data-ttu-id="2af35-122">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2af35-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2af35-123">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="2af35-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2af35-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2af35-124">CommonParameters</span></span>
<span data-ttu-id="2af35-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2af35-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2af35-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2af35-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2af35-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2af35-127">INPUTS</span></span>

### <span data-ttu-id="2af35-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="2af35-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="2af35-129">System.String</span><span class="sxs-lookup"><span data-stu-id="2af35-129">System.String</span></span>

## <span data-ttu-id="2af35-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2af35-130">OUTPUTS</span></span>

### <span data-ttu-id="2af35-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="2af35-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="2af35-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2af35-132">NOTES</span></span>
* <span data-ttu-id="2af35-133">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, operacyjny, insights</span><span class="sxs-lookup"><span data-stu-id="2af35-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="2af35-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2af35-134">RELATED LINKS</span></span>

[<span data-ttu-id="2af35-135">Enable-AzOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="2af35-135">Enable-AzOperationalInsightsIISLogCollection</span></span>](./Enable-AzOperationalInsightsIISLogCollection.md)


