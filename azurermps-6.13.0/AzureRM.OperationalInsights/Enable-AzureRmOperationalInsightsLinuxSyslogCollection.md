---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 66DD5919-B6B7-4FE5-B45B-937013549882
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/enable-azurermoperationalinsightslinuxsyslogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Enable-AzureRmOperationalInsightsLinuxSyslogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Enable-AzureRmOperationalInsightsLinuxSyslogCollection.md
ms.openlocfilehash: 015dbc617d0c4e3f8d61530eec3abe0167802931
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93541635"
---
# <span data-ttu-id="63e63-101">Enable-AzureRmOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="63e63-101">Enable-AzureRmOperationalInsightsLinuxSyslogCollection</span></span>

## <span data-ttu-id="63e63-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="63e63-102">SYNOPSIS</span></span>
<span data-ttu-id="63e63-103">Rozpoczyna zbieranie danych dziennika systemu z komputerów Linux.</span><span class="sxs-lookup"><span data-stu-id="63e63-103">Starts collection of syslog data from Linux computers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="63e63-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="63e63-104">SYNTAX</span></span>

### <span data-ttu-id="63e63-105">ByWorkspaceName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="63e63-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzureRmOperationalInsightsLinuxSyslogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63e63-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="63e63-106">ByWorkspaceObject</span></span>
```
Enable-AzureRmOperationalInsightsLinuxSyslogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63e63-107">Opis</span><span class="sxs-lookup"><span data-stu-id="63e63-107">DESCRIPTION</span></span>
<span data-ttu-id="63e63-108">Polecenie cmdlet **enable-AzureRmOperationalInsightsLinuxSyslogCollection** rozpoczyna zbieranie danych dziennika systemu z podłączonych komputerów Linux w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="63e63-108">The **Enable-AzureRmOperationalInsightsLinuxSyslogCollection** cmdlet starts collection of syslog data from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="63e63-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="63e63-109">EXAMPLES</span></span>

## <span data-ttu-id="63e63-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="63e63-110">PARAMETERS</span></span>

### <span data-ttu-id="63e63-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63e63-111">-DefaultProfile</span></span>
<span data-ttu-id="63e63-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="63e63-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63e63-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63e63-113">-ResourceGroupName</span></span>
<span data-ttu-id="63e63-114">Określa nazwę grupy zasobów zawierającej komputery z systemem Linux.</span><span class="sxs-lookup"><span data-stu-id="63e63-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="63e63-115">-Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="63e63-115">-Workspace</span></span>
<span data-ttu-id="63e63-116">Określa obszar roboczy, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63e63-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="63e63-117">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="63e63-117">-WorkspaceName</span></span>
<span data-ttu-id="63e63-118">Określa nazwę obszaru roboczego, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63e63-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="63e63-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="63e63-119">-Confirm</span></span>
<span data-ttu-id="63e63-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63e63-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63e63-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63e63-121">-WhatIf</span></span>
<span data-ttu-id="63e63-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63e63-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63e63-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="63e63-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63e63-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63e63-124">CommonParameters</span></span>
<span data-ttu-id="63e63-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63e63-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63e63-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63e63-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63e63-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="63e63-127">INPUTS</span></span>

### <span data-ttu-id="63e63-128">Microsoft. Azure. Commands. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="63e63-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="63e63-129">Parametry: przestrzeń robocza (ByValue)</span><span class="sxs-lookup"><span data-stu-id="63e63-129">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="63e63-130">System. String</span><span class="sxs-lookup"><span data-stu-id="63e63-130">System.String</span></span>

## <span data-ttu-id="63e63-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="63e63-131">OUTPUTS</span></span>

### <span data-ttu-id="63e63-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="63e63-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="63e63-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="63e63-133">NOTES</span></span>
* <span data-ttu-id="63e63-134">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, operacyjne, Insights</span><span class="sxs-lookup"><span data-stu-id="63e63-134">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="63e63-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="63e63-135">RELATED LINKS</span></span>

[<span data-ttu-id="63e63-136">Disable-AzureRmOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="63e63-136">Disable-AzureRmOperationalInsightsLinuxSyslogCollection</span></span>](./Disable-AzureRmOperationalInsightsLinuxSyslogCollection.md)

[<span data-ttu-id="63e63-137">Nowe — AzureRmOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="63e63-137">New-AzureRmOperationalInsightsLinuxSyslogDataSource</span></span>](./New-AzureRmOperationalInsightsLinuxSyslogDataSource.md)


