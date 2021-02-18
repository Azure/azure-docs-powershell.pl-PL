---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 99865242-6623-425E-92F2-0B229FC4EDAC
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/enable-azoperationalinsightslinuxcustomlogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsLinuxCustomLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsLinuxCustomLogCollection.md
ms.openlocfilehash: 0cd64af058ecf9bbc1f42178d263fcf20cabc75f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193211"
---
# <span data-ttu-id="febd8-101">Enable-AzOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="febd8-101">Enable-AzOperationalInsightsLinuxCustomLogCollection</span></span>

## <span data-ttu-id="febd8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="febd8-102">SYNOPSIS</span></span>
<span data-ttu-id="febd8-103">Uruchamia zbieranie niestandardowych dzienników z komputerów z systemem Linux.</span><span class="sxs-lookup"><span data-stu-id="febd8-103">Starts collection of custom logs from Linux computers.</span></span>

## <span data-ttu-id="febd8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="febd8-104">SYNTAX</span></span>

### <span data-ttu-id="febd8-105">ByWorkspaceName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="febd8-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzOperationalInsightsLinuxCustomLogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="febd8-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="febd8-106">ByWorkspaceObject</span></span>
```
Enable-AzOperationalInsightsLinuxCustomLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="febd8-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="febd8-107">DESCRIPTION</span></span>
<span data-ttu-id="febd8-108">Polecenie cmdlet **Enable-AzOperationalInsightsLinuxCustomLogCollection** uruchamia kolekcję niestandardowych dzienników z połączonych komputerów z systemem Linux w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="febd8-108">The **Enable-AzOperationalInsightsLinuxCustomLogCollection** cmdlet starts collection of custom logs from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="febd8-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="febd8-109">EXAMPLES</span></span>

## <span data-ttu-id="febd8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="febd8-110">PARAMETERS</span></span>

### <span data-ttu-id="febd8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="febd8-111">-DefaultProfile</span></span>
<span data-ttu-id="febd8-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="febd8-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="febd8-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="febd8-113">-ResourceGroupName</span></span>
<span data-ttu-id="febd8-114">Określa nazwę grupy zasobów zawierającej komputery z systemem Linux.</span><span class="sxs-lookup"><span data-stu-id="febd8-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="febd8-115">— Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="febd8-115">-Workspace</span></span>
<span data-ttu-id="febd8-116">Określa obszar roboczy, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="febd8-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="febd8-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="febd8-117">-WorkspaceName</span></span>
<span data-ttu-id="febd8-118">Określa nazwę obszaru roboczego, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="febd8-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="febd8-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="febd8-119">-Confirm</span></span>
<span data-ttu-id="febd8-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="febd8-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="febd8-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="febd8-121">-WhatIf</span></span>
<span data-ttu-id="febd8-122">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="febd8-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="febd8-123">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="febd8-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="febd8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="febd8-124">CommonParameters</span></span>
<span data-ttu-id="febd8-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="febd8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="febd8-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="febd8-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="febd8-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="febd8-127">INPUTS</span></span>

### <span data-ttu-id="febd8-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="febd8-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="febd8-129">System.String</span><span class="sxs-lookup"><span data-stu-id="febd8-129">System.String</span></span>

## <span data-ttu-id="febd8-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="febd8-130">OUTPUTS</span></span>

### <span data-ttu-id="febd8-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="febd8-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="febd8-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="febd8-132">NOTES</span></span>
* <span data-ttu-id="febd8-133">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, operacyjny, insights</span><span class="sxs-lookup"><span data-stu-id="febd8-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="febd8-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="febd8-134">RELATED LINKS</span></span>

[<span data-ttu-id="febd8-135">Disable-AzOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="febd8-135">Disable-AzOperationalInsightsLinuxCustomLogCollection</span></span>](./Disable-AzOperationalInsightsLinuxCustomLogCollection.md)


