---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 26B1921E-6052-471B-B5B6-F2853536A425
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/enable-azoperationalinsightsiislogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsIISLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsIISLogCollection.md
ms.openlocfilehash: f48007be3e1209cff65e46c669bce46298182247
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98384923"
---
# <span data-ttu-id="c2e50-101">Enable-AzOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="c2e50-101">Enable-AzOperationalInsightsIISLogCollection</span></span>

## <span data-ttu-id="c2e50-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c2e50-102">SYNOPSIS</span></span>
<span data-ttu-id="c2e50-103">Rozpoczyna zbieranie dzienników programu IIS z komputerów w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="c2e50-103">Starts collection of IIS logs from computers in a workspace.</span></span>

## <span data-ttu-id="c2e50-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c2e50-104">SYNTAX</span></span>

### <span data-ttu-id="c2e50-105">ByWorkspaceName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c2e50-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzOperationalInsightsIISLogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2e50-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="c2e50-106">ByWorkspaceObject</span></span>
```
Enable-AzOperationalInsightsIISLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2e50-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c2e50-107">DESCRIPTION</span></span>
<span data-ttu-id="c2e50-108">Polecenie cmdlet **enable-AzOperationalInsightsIISLogCollection** rozpoczyna zbieranie dzienników internetowych usług informacyjnych (IIS) z połączonych komputerów w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="c2e50-108">The **Enable-AzOperationalInsightsIISLogCollection** cmdlet starts collection of Internet Information Services (IIS) logs from connected computers in a workspace.</span></span>

## <span data-ttu-id="c2e50-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c2e50-109">EXAMPLES</span></span>

## <span data-ttu-id="c2e50-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c2e50-110">PARAMETERS</span></span>

### <span data-ttu-id="c2e50-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2e50-111">-DefaultProfile</span></span>
<span data-ttu-id="c2e50-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="c2e50-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c2e50-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2e50-113">-ResourceGroupName</span></span>
<span data-ttu-id="c2e50-114">Określa nazwę grupy zasobów zawierającej komputery.</span><span class="sxs-lookup"><span data-stu-id="c2e50-114">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="c2e50-115">-Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="c2e50-115">-Workspace</span></span>
<span data-ttu-id="c2e50-116">Określa obszar roboczy, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2e50-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="c2e50-117">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="c2e50-117">-WorkspaceName</span></span>
<span data-ttu-id="c2e50-118">Określa nazwę obszaru roboczego, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2e50-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="c2e50-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c2e50-119">-Confirm</span></span>
<span data-ttu-id="c2e50-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2e50-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2e50-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2e50-121">-WhatIf</span></span>
<span data-ttu-id="c2e50-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2e50-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2e50-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c2e50-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2e50-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2e50-124">CommonParameters</span></span>
<span data-ttu-id="c2e50-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2e50-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2e50-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2e50-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2e50-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c2e50-127">INPUTS</span></span>

### <span data-ttu-id="c2e50-128">Microsoft. Azure. Commands. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="c2e50-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="c2e50-129">System. String</span><span class="sxs-lookup"><span data-stu-id="c2e50-129">System.String</span></span>

## <span data-ttu-id="c2e50-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c2e50-130">OUTPUTS</span></span>

### <span data-ttu-id="c2e50-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="c2e50-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="c2e50-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c2e50-132">NOTES</span></span>

## <span data-ttu-id="c2e50-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c2e50-133">RELATED LINKS</span></span>

[<span data-ttu-id="c2e50-134">Disable-AzOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="c2e50-134">Disable-AzOperationalInsightsIISLogCollection</span></span>](./Disable-AzOperationalInsightsIISLogCollection.md)


