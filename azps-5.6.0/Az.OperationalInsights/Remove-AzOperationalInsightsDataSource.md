---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 5C1C51FE-747F-4176-84ED-A28AA3475581
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/remove-azoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsDataSource.md
ms.openlocfilehash: 1a99f06fac37c0d96a159b0c17afc606d850ee65
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989864"
---
# <span data-ttu-id="88cb0-101">Remove-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="88cb0-101">Remove-AzOperationalInsightsDataSource</span></span>

## <span data-ttu-id="88cb0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88cb0-102">SYNOPSIS</span></span>
<span data-ttu-id="88cb0-103">Usuwa źródło danych.</span><span class="sxs-lookup"><span data-stu-id="88cb0-103">Deletes a data source.</span></span>

## <span data-ttu-id="88cb0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="88cb0-104">SYNTAX</span></span>

### <span data-ttu-id="88cb0-105">ByWorkspaceName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="88cb0-105">ByWorkspaceName (Default)</span></span>
```
Remove-AzOperationalInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String> [-Name] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88cb0-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="88cb0-106">ByWorkspaceObject</span></span>
```
Remove-AzOperationalInsightsDataSource [-Workspace] <PSWorkspace> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88cb0-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="88cb0-107">DESCRIPTION</span></span>
<span data-ttu-id="88cb0-108">Polecenie **cmdlet Remove-AzOperationalInsightsDataSource** usuwa źródło danych.</span><span class="sxs-lookup"><span data-stu-id="88cb0-108">The **Remove-AzOperationalInsightsDataSource** cmdlet deletes a data source.</span></span>

## <span data-ttu-id="88cb0-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="88cb0-109">EXAMPLES</span></span>

## <span data-ttu-id="88cb0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="88cb0-110">PARAMETERS</span></span>

### <span data-ttu-id="88cb0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88cb0-111">-DefaultProfile</span></span>
<span data-ttu-id="88cb0-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="88cb0-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="88cb0-113">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="88cb0-113">-Force</span></span>
<span data-ttu-id="88cb0-114">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="88cb0-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="88cb0-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="88cb0-115">-Name</span></span>
<span data-ttu-id="88cb0-116">Określa nazwę źródła danych do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="88cb0-116">Specifies the name of a data source to delete.</span></span>

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

### <span data-ttu-id="88cb0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88cb0-117">-ResourceGroupName</span></span>
<span data-ttu-id="88cb0-118">Określa nazwę grupy zasobów zawierającej komputery.</span><span class="sxs-lookup"><span data-stu-id="88cb0-118">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="88cb0-119">— Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="88cb0-119">-Workspace</span></span>
<span data-ttu-id="88cb0-120">Określa obszar roboczy, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88cb0-120">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="88cb0-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="88cb0-121">-WorkspaceName</span></span>
<span data-ttu-id="88cb0-122">Określa nazwę obszaru roboczego, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88cb0-122">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="88cb0-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="88cb0-123">-Confirm</span></span>
<span data-ttu-id="88cb0-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="88cb0-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88cb0-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88cb0-125">-WhatIf</span></span>
<span data-ttu-id="88cb0-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88cb0-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88cb0-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="88cb0-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88cb0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88cb0-128">CommonParameters</span></span>
<span data-ttu-id="88cb0-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88cb0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88cb0-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88cb0-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88cb0-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="88cb0-131">INPUTS</span></span>

### <span data-ttu-id="88cb0-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="88cb0-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="88cb0-133">System.String</span><span class="sxs-lookup"><span data-stu-id="88cb0-133">System.String</span></span>

## <span data-ttu-id="88cb0-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="88cb0-134">OUTPUTS</span></span>

### <span data-ttu-id="88cb0-135">System.Void</span><span class="sxs-lookup"><span data-stu-id="88cb0-135">System.Void</span></span>

## <span data-ttu-id="88cb0-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="88cb0-136">NOTES</span></span>
* <span data-ttu-id="88cb0-137">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, operacyjny, insights</span><span class="sxs-lookup"><span data-stu-id="88cb0-137">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="88cb0-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="88cb0-138">RELATED LINKS</span></span>

[<span data-ttu-id="88cb0-139">Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="88cb0-139">Get-AzOperationalInsightsDataSource</span></span>](./Get-AzOperationalInsightsDataSource.md)

[<span data-ttu-id="88cb0-140">Set-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="88cb0-140">Set-AzOperationalInsightsDataSource</span></span>](./Set-AzOperationalInsightsDataSource.md)


