---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 95B54065-B6CC-4D10-A747-28CE3F412ABF
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/disable-azoperationalinsightsiislogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsIISLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsIISLogCollection.md
ms.openlocfilehash: 71a0089b4f593032404b71f17ba432486f5498d7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223007"
---
# <span data-ttu-id="5ead4-101">Disable-AzOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="5ead4-101">Disable-AzOperationalInsightsIISLogCollection</span></span>

## <span data-ttu-id="5ead4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5ead4-102">SYNOPSIS</span></span>
<span data-ttu-id="5ead4-103">Zatrzymuje zbieranie dzienników programu IIS na komputerach.</span><span class="sxs-lookup"><span data-stu-id="5ead4-103">Stops collection of IIS logs from computers.</span></span>

## <span data-ttu-id="5ead4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5ead4-104">SYNTAX</span></span>

### <span data-ttu-id="5ead4-105">ByWorkspaceName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5ead4-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzOperationalInsightsIISLogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ead4-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="5ead4-106">ByWorkspaceObject</span></span>
```
Disable-AzOperationalInsightsIISLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ead4-107">Opis</span><span class="sxs-lookup"><span data-stu-id="5ead4-107">DESCRIPTION</span></span>
<span data-ttu-id="5ead4-108">Polecenie cmdlet **disable-AzOperationalInsightsIISLogCollection** zatrzymuje zbieranie dzienników internetowych usług informacyjnych (IIS) z połączonych komputerów w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="5ead4-108">The **Disable-AzOperationalInsightsIISLogCollection** cmdlet stops collection of Internet Information Services (IIS) logs from connected computers in a workspace.</span></span>

## <span data-ttu-id="5ead4-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5ead4-109">EXAMPLES</span></span>

## <span data-ttu-id="5ead4-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5ead4-110">PARAMETERS</span></span>

### <span data-ttu-id="5ead4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ead4-111">-DefaultProfile</span></span>
<span data-ttu-id="5ead4-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="5ead4-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5ead4-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ead4-113">-ResourceGroupName</span></span>
<span data-ttu-id="5ead4-114">Określa nazwę grupy zasobów zawierającej komputery.</span><span class="sxs-lookup"><span data-stu-id="5ead4-114">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="5ead4-115">-Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="5ead4-115">-Workspace</span></span>
<span data-ttu-id="5ead4-116">Określa obszar roboczy, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ead4-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="5ead4-117">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="5ead4-117">-WorkspaceName</span></span>
<span data-ttu-id="5ead4-118">Określa nazwę obszaru roboczego, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ead4-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="5ead4-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5ead4-119">-Confirm</span></span>
<span data-ttu-id="5ead4-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ead4-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ead4-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ead4-121">-WhatIf</span></span>
<span data-ttu-id="5ead4-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ead4-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ead4-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5ead4-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ead4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ead4-124">CommonParameters</span></span>
<span data-ttu-id="5ead4-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ead4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ead4-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ead4-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ead4-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5ead4-127">INPUTS</span></span>

### <span data-ttu-id="5ead4-128">Microsoft. Azure. Commands. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="5ead4-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="5ead4-129">System. String</span><span class="sxs-lookup"><span data-stu-id="5ead4-129">System.String</span></span>

## <span data-ttu-id="5ead4-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5ead4-130">OUTPUTS</span></span>

### <span data-ttu-id="5ead4-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="5ead4-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="5ead4-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5ead4-132">NOTES</span></span>
* <span data-ttu-id="5ead4-133">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, operacyjne, Insights</span><span class="sxs-lookup"><span data-stu-id="5ead4-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="5ead4-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5ead4-134">RELATED LINKS</span></span>

[<span data-ttu-id="5ead4-135">Enable-AzOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="5ead4-135">Enable-AzOperationalInsightsIISLogCollection</span></span>](./Enable-AzOperationalInsightsIISLogCollection.md)


