---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 4A91EEDA-D8F0-4109-A32E-B83694952C06
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/disable-azoperationalinsightslinuxsyslogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsLinuxSyslogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsLinuxSyslogCollection.md
ms.openlocfilehash: 76499570abb458987b79f4cd707a6845b43cfe24
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708833"
---
# <span data-ttu-id="9db16-101">Disable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="9db16-101">Disable-AzOperationalInsightsLinuxSyslogCollection</span></span>

## <span data-ttu-id="9db16-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9db16-102">SYNOPSIS</span></span>
<span data-ttu-id="9db16-103">Zatrzymuje zbieranie danych dziennika systemu z komputerów Linux.</span><span class="sxs-lookup"><span data-stu-id="9db16-103">Stops collection of syslog data from Linux computers.</span></span>

## <span data-ttu-id="9db16-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9db16-104">SYNTAX</span></span>

### <span data-ttu-id="9db16-105">ByWorkspaceName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9db16-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzOperationalInsightsLinuxSyslogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9db16-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="9db16-106">ByWorkspaceObject</span></span>
```
Disable-AzOperationalInsightsLinuxSyslogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9db16-107">Opis</span><span class="sxs-lookup"><span data-stu-id="9db16-107">DESCRIPTION</span></span>
<span data-ttu-id="9db16-108">Polecenie cmdlet **disable-AzOperationalInsightsLinuxSyslogCollection** zatrzymuje zbieranie danych dziennika systemu z połączonych komputerów Linux w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="9db16-108">The **Disable-AzOperationalInsightsLinuxSyslogCollection** cmdlet stops collection of syslog data from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="9db16-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9db16-109">EXAMPLES</span></span>

## <span data-ttu-id="9db16-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9db16-110">PARAMETERS</span></span>

### <span data-ttu-id="9db16-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9db16-111">-DefaultProfile</span></span>
<span data-ttu-id="9db16-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="9db16-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9db16-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9db16-113">-ResourceGroupName</span></span>
<span data-ttu-id="9db16-114">Określa nazwę grupy zasobów zawierającej komputery z systemem Linux.</span><span class="sxs-lookup"><span data-stu-id="9db16-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="9db16-115">-Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="9db16-115">-Workspace</span></span>
<span data-ttu-id="9db16-116">Określa obszar roboczy, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9db16-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="9db16-117">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="9db16-117">-WorkspaceName</span></span>
<span data-ttu-id="9db16-118">Określa nazwę obszaru roboczego, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9db16-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="9db16-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9db16-119">-Confirm</span></span>
<span data-ttu-id="9db16-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9db16-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9db16-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9db16-121">-WhatIf</span></span>
<span data-ttu-id="9db16-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9db16-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9db16-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9db16-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9db16-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9db16-124">CommonParameters</span></span>
<span data-ttu-id="9db16-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9db16-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9db16-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9db16-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9db16-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9db16-127">INPUTS</span></span>

### <span data-ttu-id="9db16-128">Microsoft. Azure. Commands. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="9db16-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="9db16-129">System. String</span><span class="sxs-lookup"><span data-stu-id="9db16-129">System.String</span></span>

## <span data-ttu-id="9db16-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9db16-130">OUTPUTS</span></span>

### <span data-ttu-id="9db16-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="9db16-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="9db16-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9db16-132">NOTES</span></span>
* <span data-ttu-id="9db16-133">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, operacyjne, Insights</span><span class="sxs-lookup"><span data-stu-id="9db16-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="9db16-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9db16-134">RELATED LINKS</span></span>

[<span data-ttu-id="9db16-135">Enable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="9db16-135">Enable-AzOperationalInsightsLinuxSyslogCollection</span></span>](./Enable-AzOperationalInsightsLinuxSyslogCollection.md)

[<span data-ttu-id="9db16-136">Nowe — AzOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="9db16-136">New-AzOperationalInsightsLinuxSyslogDataSource</span></span>](./New-AzOperationalInsightsLinuxSyslogDataSource.md)

