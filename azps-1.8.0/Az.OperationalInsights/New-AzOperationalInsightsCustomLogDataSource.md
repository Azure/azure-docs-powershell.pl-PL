---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 6A08AF7C-1E18-40A1-B21E-12F94823D304
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightscustomlogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsCustomLogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsCustomLogDataSource.md
ms.openlocfilehash: e1b0ddc282ba72c175a13d8be18fed0bfc852b6c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708811"
---
# <span data-ttu-id="a16ad-101">New-AzOperationalInsightsCustomLogDataSource</span><span class="sxs-lookup"><span data-stu-id="a16ad-101">New-AzOperationalInsightsCustomLogDataSource</span></span>

## <span data-ttu-id="a16ad-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a16ad-102">SYNOPSIS</span></span>
<span data-ttu-id="a16ad-103">Definiuje niestandardowe zasady zbierania dziennika.</span><span class="sxs-lookup"><span data-stu-id="a16ad-103">Defines a custom log collection policy.</span></span>

## <span data-ttu-id="a16ad-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a16ad-104">SYNTAX</span></span>

### <span data-ttu-id="a16ad-105">ByWorkspaceName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a16ad-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsCustomLogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-CustomLogRawJson] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a16ad-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="a16ad-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsCustomLogDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-CustomLogRawJson] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a16ad-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a16ad-107">DESCRIPTION</span></span>
<span data-ttu-id="a16ad-108">Polecenie cmdlet **New-AzOperationalInsightsCustomLogDataSource** definiuje niestandardowe zasady zbierania dziennika.</span><span class="sxs-lookup"><span data-stu-id="a16ad-108">The **New-AzOperationalInsightsCustomLogDataSource** cmdlet defines a custom log collection policy.</span></span>

## <span data-ttu-id="a16ad-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a16ad-109">EXAMPLES</span></span>

## <span data-ttu-id="a16ad-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a16ad-110">PARAMETERS</span></span>

### <span data-ttu-id="a16ad-111">-CustomLogRawJson</span><span class="sxs-lookup"><span data-stu-id="a16ad-111">-CustomLogRawJson</span></span>
<span data-ttu-id="a16ad-112">Określa niestandardową zasadę zbierania danych w postaci nieprzetworzonego ciągu JSON (kod JSON).</span><span class="sxs-lookup"><span data-stu-id="a16ad-112">Specifies the custom collection policy as a raw JavaScript Object Notation (JSON) string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a16ad-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a16ad-113">-DefaultProfile</span></span>
<span data-ttu-id="a16ad-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="a16ad-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a16ad-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a16ad-115">-Force</span></span>
<span data-ttu-id="a16ad-116">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="a16ad-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a16ad-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a16ad-117">-Name</span></span>
<span data-ttu-id="a16ad-118">Określa nazwę źródła danych.</span><span class="sxs-lookup"><span data-stu-id="a16ad-118">Specifies a name for the data source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a16ad-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a16ad-119">-ResourceGroupName</span></span>
<span data-ttu-id="a16ad-120">Określa nazwę grupy zasobów zawierającej komputery.</span><span class="sxs-lookup"><span data-stu-id="a16ad-120">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="a16ad-121">-Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="a16ad-121">-Workspace</span></span>
<span data-ttu-id="a16ad-122">Określa obszar roboczy, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a16ad-122">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="a16ad-123">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="a16ad-123">-WorkspaceName</span></span>
<span data-ttu-id="a16ad-124">Określa nazwę obszaru roboczego, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a16ad-124">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="a16ad-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a16ad-125">-Confirm</span></span>
<span data-ttu-id="a16ad-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a16ad-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a16ad-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a16ad-127">-WhatIf</span></span>
<span data-ttu-id="a16ad-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a16ad-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a16ad-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a16ad-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a16ad-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a16ad-130">CommonParameters</span></span>
<span data-ttu-id="a16ad-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a16ad-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a16ad-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a16ad-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a16ad-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a16ad-133">INPUTS</span></span>

### <span data-ttu-id="a16ad-134">Microsoft. Azure. Commands. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="a16ad-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="a16ad-135">System. String</span><span class="sxs-lookup"><span data-stu-id="a16ad-135">System.String</span></span>

## <span data-ttu-id="a16ad-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a16ad-136">OUTPUTS</span></span>

### <span data-ttu-id="a16ad-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="a16ad-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="a16ad-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a16ad-138">NOTES</span></span>

## <span data-ttu-id="a16ad-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a16ad-139">RELATED LINKS</span></span>

[<span data-ttu-id="a16ad-140">Disable-AzOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="a16ad-140">Disable-AzOperationalInsightsLinuxCustomLogCollection</span></span>](./Disable-AzOperationalInsightsLinuxCustomLogCollection.md)

[<span data-ttu-id="a16ad-141">Enable-AzOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="a16ad-141">Enable-AzOperationalInsightsLinuxCustomLogCollection</span></span>](./Enable-AzOperationalInsightsLinuxCustomLogCollection.md)

