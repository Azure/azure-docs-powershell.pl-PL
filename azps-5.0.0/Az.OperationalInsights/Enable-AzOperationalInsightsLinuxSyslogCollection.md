---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 66DD5919-B6B7-4FE5-B45B-937013549882
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/enable-azoperationalinsightslinuxsyslogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsLinuxSyslogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsLinuxSyslogCollection.md
ms.openlocfilehash: d609ee8910a1dc016365d126b61bc1f4820e977c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94318979"
---
# <span data-ttu-id="bcf34-101">Enable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="bcf34-101">Enable-AzOperationalInsightsLinuxSyslogCollection</span></span>

## <span data-ttu-id="bcf34-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bcf34-102">SYNOPSIS</span></span>
<span data-ttu-id="bcf34-103">Rozpoczyna zbieranie danych dziennika systemu z komputerów Linux.</span><span class="sxs-lookup"><span data-stu-id="bcf34-103">Starts collection of syslog data from Linux computers.</span></span>

## <span data-ttu-id="bcf34-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bcf34-104">SYNTAX</span></span>

### <span data-ttu-id="bcf34-105">ByWorkspaceName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="bcf34-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzOperationalInsightsLinuxSyslogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bcf34-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="bcf34-106">ByWorkspaceObject</span></span>
```
Enable-AzOperationalInsightsLinuxSyslogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bcf34-107">Opis</span><span class="sxs-lookup"><span data-stu-id="bcf34-107">DESCRIPTION</span></span>
<span data-ttu-id="bcf34-108">Polecenie cmdlet **enable-AzOperationalInsightsLinuxSyslogCollection** rozpoczyna zbieranie danych dziennika systemu z podłączonych komputerów Linux w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="bcf34-108">The **Enable-AzOperationalInsightsLinuxSyslogCollection** cmdlet starts collection of syslog data from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="bcf34-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bcf34-109">EXAMPLES</span></span>

## <span data-ttu-id="bcf34-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bcf34-110">PARAMETERS</span></span>

### <span data-ttu-id="bcf34-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcf34-111">-DefaultProfile</span></span>
<span data-ttu-id="bcf34-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="bcf34-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bcf34-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcf34-113">-ResourceGroupName</span></span>
<span data-ttu-id="bcf34-114">Określa nazwę grupy zasobów zawierającej komputery z systemem Linux.</span><span class="sxs-lookup"><span data-stu-id="bcf34-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="bcf34-115">-Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="bcf34-115">-Workspace</span></span>
<span data-ttu-id="bcf34-116">Określa obszar roboczy, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bcf34-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="bcf34-117">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="bcf34-117">-WorkspaceName</span></span>
<span data-ttu-id="bcf34-118">Określa nazwę obszaru roboczego, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bcf34-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="bcf34-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bcf34-119">-Confirm</span></span>
<span data-ttu-id="bcf34-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bcf34-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bcf34-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bcf34-121">-WhatIf</span></span>
<span data-ttu-id="bcf34-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bcf34-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bcf34-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bcf34-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bcf34-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcf34-124">CommonParameters</span></span>
<span data-ttu-id="bcf34-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcf34-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcf34-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bcf34-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcf34-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bcf34-127">INPUTS</span></span>

### <span data-ttu-id="bcf34-128">Microsoft. Azure. Commands. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="bcf34-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="bcf34-129">System. String</span><span class="sxs-lookup"><span data-stu-id="bcf34-129">System.String</span></span>

## <span data-ttu-id="bcf34-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bcf34-130">OUTPUTS</span></span>

### <span data-ttu-id="bcf34-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="bcf34-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="bcf34-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bcf34-132">NOTES</span></span>
* <span data-ttu-id="bcf34-133">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, operacyjne, Insights</span><span class="sxs-lookup"><span data-stu-id="bcf34-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="bcf34-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bcf34-134">RELATED LINKS</span></span>

[<span data-ttu-id="bcf34-135">Disable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="bcf34-135">Disable-AzOperationalInsightsLinuxSyslogCollection</span></span>](./Disable-AzOperationalInsightsLinuxSyslogCollection.md)

[<span data-ttu-id="bcf34-136">Nowe — AzOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="bcf34-136">New-AzOperationalInsightsLinuxSyslogDataSource</span></span>](./New-AzOperationalInsightsLinuxSyslogDataSource.md)


