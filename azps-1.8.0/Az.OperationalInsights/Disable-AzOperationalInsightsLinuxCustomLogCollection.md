---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: EF3FE3F1-1C8F-41EB-990E-F2B30BD9D082
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/disable-azoperationalinsightslinuxcustomlogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsLinuxCustomLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsLinuxCustomLogCollection.md
ms.openlocfilehash: f36c6b87ed6e1fc916df228448426a441bc855ae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708835"
---
# <span data-ttu-id="cac4f-101">Disable-AzOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="cac4f-101">Disable-AzOperationalInsightsLinuxCustomLogCollection</span></span>

## <span data-ttu-id="cac4f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cac4f-102">SYNOPSIS</span></span>
<span data-ttu-id="cac4f-103">Zatrzymuje zbieranie niestandardowych dzienników z komputerów z systemem Linux.</span><span class="sxs-lookup"><span data-stu-id="cac4f-103">Stops collection of custom logs from Linux computers.</span></span>

## <span data-ttu-id="cac4f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cac4f-104">SYNTAX</span></span>

### <span data-ttu-id="cac4f-105">ByWorkspaceName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="cac4f-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzOperationalInsightsLinuxCustomLogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cac4f-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="cac4f-106">ByWorkspaceObject</span></span>
```
Disable-AzOperationalInsightsLinuxCustomLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cac4f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="cac4f-107">DESCRIPTION</span></span>
<span data-ttu-id="cac4f-108">Polecenie cmdlet **disable-AzOperationalInsightsLinuxCustomLogCollection** zatrzymuje zbieranie niestandardowych dzienników z połączonych komputerów z systemem Linux w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="cac4f-108">The **Disable-AzOperationalInsightsLinuxCustomLogCollection** cmdlet stops collection of custom logs from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="cac4f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cac4f-109">EXAMPLES</span></span>

## <span data-ttu-id="cac4f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cac4f-110">PARAMETERS</span></span>

### <span data-ttu-id="cac4f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cac4f-111">-DefaultProfile</span></span>
<span data-ttu-id="cac4f-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="cac4f-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cac4f-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cac4f-113">-ResourceGroupName</span></span>
<span data-ttu-id="cac4f-114">Określa nazwę grupy zasobów zawierającej komputery z systemem Linux.</span><span class="sxs-lookup"><span data-stu-id="cac4f-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="cac4f-115">-Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="cac4f-115">-Workspace</span></span>
<span data-ttu-id="cac4f-116">Określa obszar roboczy, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cac4f-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="cac4f-117">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="cac4f-117">-WorkspaceName</span></span>
<span data-ttu-id="cac4f-118">Określa nazwę obszaru roboczego, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cac4f-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="cac4f-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cac4f-119">-Confirm</span></span>
<span data-ttu-id="cac4f-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cac4f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cac4f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cac4f-121">-WhatIf</span></span>
<span data-ttu-id="cac4f-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cac4f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cac4f-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="cac4f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cac4f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cac4f-124">CommonParameters</span></span>
<span data-ttu-id="cac4f-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cac4f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cac4f-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cac4f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cac4f-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cac4f-127">INPUTS</span></span>

### <span data-ttu-id="cac4f-128">Microsoft. Azure. Commands. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="cac4f-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="cac4f-129">System. String</span><span class="sxs-lookup"><span data-stu-id="cac4f-129">System.String</span></span>

## <span data-ttu-id="cac4f-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cac4f-130">OUTPUTS</span></span>

### <span data-ttu-id="cac4f-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="cac4f-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="cac4f-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cac4f-132">NOTES</span></span>
* <span data-ttu-id="cac4f-133">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, operacyjne, Insights</span><span class="sxs-lookup"><span data-stu-id="cac4f-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="cac4f-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cac4f-134">RELATED LINKS</span></span>

[<span data-ttu-id="cac4f-135">Enable-AzOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="cac4f-135">Enable-AzOperationalInsightsLinuxCustomLogCollection</span></span>](./Enable-AzOperationalInsightsLinuxCustomLogCollection.md)


