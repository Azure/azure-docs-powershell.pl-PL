---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 6A08AF7C-1E18-40A1-B21E-12F94823D304
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightscustomlogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsCustomLogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsCustomLogDataSource.md
ms.openlocfilehash: ba33d02ec8c47c91865cc2d0f5549e5f446ca2c6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98322742"
---
# <span data-ttu-id="73cb0-101">New-AzOperationalInsightsCustomLogDataSource</span><span class="sxs-lookup"><span data-stu-id="73cb0-101">New-AzOperationalInsightsCustomLogDataSource</span></span>

## <span data-ttu-id="73cb0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="73cb0-102">SYNOPSIS</span></span>
<span data-ttu-id="73cb0-103">Definiuje niestandardowe zasady zbierania dziennika.</span><span class="sxs-lookup"><span data-stu-id="73cb0-103">Defines a custom log collection policy.</span></span>

## <span data-ttu-id="73cb0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="73cb0-104">SYNTAX</span></span>

### <span data-ttu-id="73cb0-105">ByWorkspaceName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="73cb0-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsCustomLogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-CustomLogRawJson] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73cb0-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="73cb0-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsCustomLogDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-CustomLogRawJson] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="73cb0-107">Opis</span><span class="sxs-lookup"><span data-stu-id="73cb0-107">DESCRIPTION</span></span>
<span data-ttu-id="73cb0-108">Polecenie cmdlet **New-AzOperationalInsightsCustomLogDataSource** definiuje niestandardowe zasady zbierania dziennika.</span><span class="sxs-lookup"><span data-stu-id="73cb0-108">The **New-AzOperationalInsightsCustomLogDataSource** cmdlet defines a custom log collection policy.</span></span>

## <span data-ttu-id="73cb0-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="73cb0-109">EXAMPLES</span></span>

## <span data-ttu-id="73cb0-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="73cb0-110">PARAMETERS</span></span>

### <span data-ttu-id="73cb0-111">-CustomLogRawJson</span><span class="sxs-lookup"><span data-stu-id="73cb0-111">-CustomLogRawJson</span></span>
<span data-ttu-id="73cb0-112">Określa niestandardową zasadę zbierania danych w postaci nieprzetworzonego ciągu JSON (kod JSON).</span><span class="sxs-lookup"><span data-stu-id="73cb0-112">Specifies the custom collection policy as a raw JavaScript Object Notation (JSON) string.</span></span>

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

### <span data-ttu-id="73cb0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73cb0-113">-DefaultProfile</span></span>
<span data-ttu-id="73cb0-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="73cb0-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="73cb0-115">-Force</span><span class="sxs-lookup"><span data-stu-id="73cb0-115">-Force</span></span>
<span data-ttu-id="73cb0-116">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="73cb0-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="73cb0-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="73cb0-117">-Name</span></span>
<span data-ttu-id="73cb0-118">Określa nazwę źródła danych.</span><span class="sxs-lookup"><span data-stu-id="73cb0-118">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="73cb0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73cb0-119">-ResourceGroupName</span></span>
<span data-ttu-id="73cb0-120">Określa nazwę grupy zasobów zawierającej komputery.</span><span class="sxs-lookup"><span data-stu-id="73cb0-120">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="73cb0-121">-Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="73cb0-121">-Workspace</span></span>
<span data-ttu-id="73cb0-122">Określa obszar roboczy, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73cb0-122">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="73cb0-123">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="73cb0-123">-WorkspaceName</span></span>
<span data-ttu-id="73cb0-124">Określa nazwę obszaru roboczego, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73cb0-124">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="73cb0-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="73cb0-125">-Confirm</span></span>
<span data-ttu-id="73cb0-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73cb0-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73cb0-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73cb0-127">-WhatIf</span></span>
<span data-ttu-id="73cb0-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73cb0-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73cb0-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="73cb0-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73cb0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73cb0-130">CommonParameters</span></span>
<span data-ttu-id="73cb0-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73cb0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73cb0-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73cb0-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73cb0-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="73cb0-133">INPUTS</span></span>

### <span data-ttu-id="73cb0-134">Microsoft. Azure. Commands. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="73cb0-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="73cb0-135">System. String</span><span class="sxs-lookup"><span data-stu-id="73cb0-135">System.String</span></span>

## <span data-ttu-id="73cb0-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="73cb0-136">OUTPUTS</span></span>

### <span data-ttu-id="73cb0-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="73cb0-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="73cb0-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="73cb0-138">NOTES</span></span>

## <span data-ttu-id="73cb0-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="73cb0-139">RELATED LINKS</span></span>

[<span data-ttu-id="73cb0-140">Disable-AzOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="73cb0-140">Disable-AzOperationalInsightsLinuxCustomLogCollection</span></span>](./Disable-AzOperationalInsightsLinuxCustomLogCollection.md)

[<span data-ttu-id="73cb0-141">Enable-AzOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="73cb0-141">Enable-AzOperationalInsightsLinuxCustomLogCollection</span></span>](./Enable-AzOperationalInsightsLinuxCustomLogCollection.md)


