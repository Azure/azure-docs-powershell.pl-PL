---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 47AFBAC7-8818-4788-B685-7AB4DCD6C2DE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/disable-azurermoperationalinsightslinuxperformancecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Disable-AzureRmOperationalInsightsLinuxPerformanceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Disable-AzureRmOperationalInsightsLinuxPerformanceCollection.md
ms.openlocfilehash: eb83881b2875005504626224b1fa3f1673ed4b7d
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/21/2020
ms.locfileid: "93554420"
---
# <span data-ttu-id="8cc49-101">Disable-AzureRmOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="8cc49-101">Disable-AzureRmOperationalInsightsLinuxPerformanceCollection</span></span>

## <span data-ttu-id="8cc49-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8cc49-102">SYNOPSIS</span></span>
<span data-ttu-id="8cc49-103">Zatrzymuje zbieranie liczników wydajności z komputerów z systemem Linux.</span><span class="sxs-lookup"><span data-stu-id="8cc49-103">Stops collection of performance counters from Linux computers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8cc49-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8cc49-104">SYNTAX</span></span>

### <span data-ttu-id="8cc49-105">ByWorkspaceName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8cc49-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzureRmOperationalInsightsLinuxPerformanceCollection [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cc49-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="8cc49-106">ByWorkspaceObject</span></span>
```
Disable-AzureRmOperationalInsightsLinuxPerformanceCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8cc49-107">Opis</span><span class="sxs-lookup"><span data-stu-id="8cc49-107">DESCRIPTION</span></span>
<span data-ttu-id="8cc49-108">Polecenie cmdlet **disable-AzureRmOperationalInsightsLinuxPerformanceCollection** zatrzymuje zbieranie liczników wydajności z połączonych komputerów z systemem Linux w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="8cc49-108">The **Disable-AzureRmOperationalInsightsLinuxPerformanceCollection** cmdlet stops collection of performance counters from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="8cc49-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8cc49-109">EXAMPLES</span></span>

## <span data-ttu-id="8cc49-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8cc49-110">PARAMETERS</span></span>

### <span data-ttu-id="8cc49-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cc49-111">-DefaultProfile</span></span>
<span data-ttu-id="8cc49-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="8cc49-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cc49-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cc49-113">-ResourceGroupName</span></span>
<span data-ttu-id="8cc49-114">Określa nazwę grupy zasobów zawierającej komputery z systemem Linux.</span><span class="sxs-lookup"><span data-stu-id="8cc49-114">Specifies the name of a resource group that contains Linux computers.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cc49-115">-Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="8cc49-115">-Workspace</span></span>
<span data-ttu-id="8cc49-116">Określa obszar roboczy, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8cc49-116">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8cc49-117">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="8cc49-117">-WorkspaceName</span></span>
<span data-ttu-id="8cc49-118">Określa nazwę obszaru roboczego, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8cc49-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cc49-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8cc49-119">-Confirm</span></span>
<span data-ttu-id="8cc49-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8cc49-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cc49-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8cc49-121">-WhatIf</span></span>
<span data-ttu-id="8cc49-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8cc49-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8cc49-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8cc49-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cc49-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cc49-124">CommonParameters</span></span>
<span data-ttu-id="8cc49-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cc49-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cc49-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8cc49-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cc49-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8cc49-127">INPUTS</span></span>

### <span data-ttu-id="8cc49-128">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="8cc49-128">PSWorkspace</span></span>
<span data-ttu-id="8cc49-129">Parametr "obszar roboczy" akceptuje wartość typu "PSWorkspace" z potoku</span><span class="sxs-lookup"><span data-stu-id="8cc49-129">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="8cc49-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8cc49-130">OUTPUTS</span></span>

### <span data-ttu-id="8cc49-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="8cc49-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="8cc49-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8cc49-132">NOTES</span></span>
* <span data-ttu-id="8cc49-133">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, operacyjne, Insights</span><span class="sxs-lookup"><span data-stu-id="8cc49-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="8cc49-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8cc49-134">RELATED LINKS</span></span>

[<span data-ttu-id="8cc49-135">Enable-AzureRmOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="8cc49-135">Enable-AzureRmOperationalInsightsLinuxPerformanceCollection</span></span>](./Enable-AzureRmOperationalInsightsLinuxPerformanceCollection.md)

[<span data-ttu-id="8cc49-136">Nowe — AzureRmOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="8cc49-136">New-AzureRmOperationalInsightsLinuxSyslogDataSource</span></span>](./New-AzureRmOperationalInsightsLinuxSyslogDataSource.md)


