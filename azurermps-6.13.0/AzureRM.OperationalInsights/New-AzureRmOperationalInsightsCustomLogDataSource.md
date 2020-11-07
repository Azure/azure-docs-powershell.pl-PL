---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 6A08AF7C-1E18-40A1-B21E-12F94823D304
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightscustomlogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsCustomLogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsCustomLogDataSource.md
ms.openlocfilehash: b364833be9219d778bc9d204f7e1a61a1667fe1a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718294"
---
# <span data-ttu-id="d896c-101">New-AzureRmOperationalInsightsCustomLogDataSource</span><span class="sxs-lookup"><span data-stu-id="d896c-101">New-AzureRmOperationalInsightsCustomLogDataSource</span></span>

## <span data-ttu-id="d896c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d896c-102">SYNOPSIS</span></span>
<span data-ttu-id="d896c-103">Definiuje niestandardowe zasady zbierania dziennika.</span><span class="sxs-lookup"><span data-stu-id="d896c-103">Defines a custom log collection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d896c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d896c-104">SYNTAX</span></span>

### <span data-ttu-id="d896c-105">ByWorkspaceName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d896c-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsCustomLogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-CustomLogRawJson] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d896c-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d896c-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsCustomLogDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-CustomLogRawJson] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d896c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d896c-107">DESCRIPTION</span></span>
<span data-ttu-id="d896c-108">Polecenie cmdlet **New-AzureRmOperationalInsightsCustomLogDataSource** definiuje niestandardowe zasady zbierania dziennika.</span><span class="sxs-lookup"><span data-stu-id="d896c-108">The **New-AzureRmOperationalInsightsCustomLogDataSource** cmdlet defines a custom log collection policy.</span></span>

## <span data-ttu-id="d896c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d896c-109">EXAMPLES</span></span>

## <span data-ttu-id="d896c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d896c-110">PARAMETERS</span></span>

### <span data-ttu-id="d896c-111">-CustomLogRawJson</span><span class="sxs-lookup"><span data-stu-id="d896c-111">-CustomLogRawJson</span></span>
<span data-ttu-id="d896c-112">Określa niestandardową zasadę zbierania danych w postaci nieprzetworzonego ciągu JSON (kod JSON).</span><span class="sxs-lookup"><span data-stu-id="d896c-112">Specifies the custom collection policy as a raw JavaScript Object Notation (JSON) string.</span></span>

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

### <span data-ttu-id="d896c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d896c-113">-DefaultProfile</span></span>
<span data-ttu-id="d896c-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="d896c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d896c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="d896c-115">-Force</span></span>
<span data-ttu-id="d896c-116">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="d896c-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d896c-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d896c-117">-Name</span></span>
<span data-ttu-id="d896c-118">Określa nazwę źródła danych.</span><span class="sxs-lookup"><span data-stu-id="d896c-118">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="d896c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d896c-119">-ResourceGroupName</span></span>
<span data-ttu-id="d896c-120">Określa nazwę grupy zasobów zawierającej komputery.</span><span class="sxs-lookup"><span data-stu-id="d896c-120">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="d896c-121">-Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="d896c-121">-Workspace</span></span>
<span data-ttu-id="d896c-122">Określa obszar roboczy, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d896c-122">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="d896c-123">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="d896c-123">-WorkspaceName</span></span>
<span data-ttu-id="d896c-124">Określa nazwę obszaru roboczego, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d896c-124">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="d896c-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d896c-125">-Confirm</span></span>
<span data-ttu-id="d896c-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d896c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d896c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d896c-127">-WhatIf</span></span>
<span data-ttu-id="d896c-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d896c-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d896c-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d896c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d896c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d896c-130">CommonParameters</span></span>
<span data-ttu-id="d896c-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d896c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d896c-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d896c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d896c-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d896c-133">INPUTS</span></span>

### <span data-ttu-id="d896c-134">Microsoft. Azure. Commands. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="d896c-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="d896c-135">Parametry: przestrzeń robocza (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d896c-135">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="d896c-136">System. String</span><span class="sxs-lookup"><span data-stu-id="d896c-136">System.String</span></span>

## <span data-ttu-id="d896c-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d896c-137">OUTPUTS</span></span>

### <span data-ttu-id="d896c-138">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="d896c-138">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="d896c-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d896c-139">NOTES</span></span>

## <span data-ttu-id="d896c-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d896c-140">RELATED LINKS</span></span>

[<span data-ttu-id="d896c-141">Disable-AzureRmOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="d896c-141">Disable-AzureRmOperationalInsightsLinuxCustomLogCollection</span></span>](./Disable-AzureRmOperationalInsightsLinuxCustomLogCollection.md)

[<span data-ttu-id="d896c-142">Enable-AzureRmOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="d896c-142">Enable-AzureRmOperationalInsightsLinuxCustomLogCollection</span></span>](./Enable-AzureRmOperationalInsightsLinuxCustomLogCollection.md)


