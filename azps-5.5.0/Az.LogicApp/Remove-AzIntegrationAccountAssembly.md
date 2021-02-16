---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAssembly.md
ms.openlocfilehash: 4dceb934f5cf746908c289c7662de0dc3dae09a5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187587"
---
# <span data-ttu-id="42cc3-101">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="42cc3-101">Remove-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="42cc3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42cc3-102">SYNOPSIS</span></span>
<span data-ttu-id="42cc3-103">Usuwa zestaw konta integracji.</span><span class="sxs-lookup"><span data-stu-id="42cc3-103">Removes an integration account assembly.</span></span>

## <span data-ttu-id="42cc3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="42cc3-104">SYNTAX</span></span>

### <span data-ttu-id="42cc3-105">ByIntegrationAccount (domyślne)</span><span class="sxs-lookup"><span data-stu-id="42cc3-105">ByIntegrationAccount (Default)</span></span>
```
Remove-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42cc3-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="42cc3-106">ByInputObject</span></span>
```
Remove-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42cc3-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="42cc3-107">ByResourceId</span></span>
```
Remove-AzIntegrationAccountAssembly -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42cc3-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="42cc3-108">DESCRIPTION</span></span>
<span data-ttu-id="42cc3-109">Polecenie **cmdlet Remove-AzIntegrationAccountAssembly** usuwa zestaw z konta integracji.</span><span class="sxs-lookup"><span data-stu-id="42cc3-109">The **Remove-AzIntegrationAccountAssembly** cmdlet removes an assembly from an integration account.</span></span>

## <span data-ttu-id="42cc3-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="42cc3-110">EXAMPLES</span></span>

### <span data-ttu-id="42cc3-111">Przykład 1. Usuwanie zestawu według parametrów</span><span class="sxs-lookup"><span data-stu-id="42cc3-111">Example 1: Remove an assembly by parameters</span></span>
```powershell
PS C:\> Remove-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly"
```

<span data-ttu-id="42cc3-112">Usuwa zestaw o nazwie "sampleAssembly" znajdujący się na koncie integracji "sampleIntegrationAccount".</span><span class="sxs-lookup"><span data-stu-id="42cc3-112">Removes the assembly named "sampleAssembly" located in the integration account "sampleIntegrationAccount".</span></span>

## <span data-ttu-id="42cc3-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="42cc3-113">PARAMETERS</span></span>

### <span data-ttu-id="42cc3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42cc3-114">-DefaultProfile</span></span>
<span data-ttu-id="42cc3-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="42cc3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42cc3-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="42cc3-116">-InputObject</span></span>
<span data-ttu-id="42cc3-117">Zestaw konta integracji.</span><span class="sxs-lookup"><span data-stu-id="42cc3-117">An integration account assembly.</span></span>

```yaml
Type: Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="42cc3-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="42cc3-118">-Name</span></span>
<span data-ttu-id="42cc3-119">Nazwa zestawu konta integracji.</span><span class="sxs-lookup"><span data-stu-id="42cc3-119">The integration account assembly name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases: AssemblyName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42cc3-120">-ParentName</span><span class="sxs-lookup"><span data-stu-id="42cc3-120">-ParentName</span></span>
<span data-ttu-id="42cc3-121">Nazwa konta integracji.</span><span class="sxs-lookup"><span data-stu-id="42cc3-121">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases: IntegrationAccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42cc3-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="42cc3-122">-PassThru</span></span>
<span data-ttu-id="42cc3-123">Zwracanie, czy polecenie zostało pomyślnie lub nie.</span><span class="sxs-lookup"><span data-stu-id="42cc3-123">Return whether the command was successful or not.</span></span>

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

### <span data-ttu-id="42cc3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42cc3-124">-ResourceGroupName</span></span>
<span data-ttu-id="42cc3-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="42cc3-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42cc3-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="42cc3-126">-ResourceId</span></span>
<span data-ttu-id="42cc3-127">Identyfikator zasobu zestawu konta integracji.</span><span class="sxs-lookup"><span data-stu-id="42cc3-127">The integration account assembly resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42cc3-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="42cc3-128">-Confirm</span></span>
<span data-ttu-id="42cc3-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="42cc3-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42cc3-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42cc3-130">-WhatIf</span></span>
<span data-ttu-id="42cc3-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42cc3-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="42cc3-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="42cc3-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42cc3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42cc3-133">CommonParameters</span></span>
<span data-ttu-id="42cc3-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42cc3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42cc3-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42cc3-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42cc3-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="42cc3-136">INPUTS</span></span>

### <span data-ttu-id="42cc3-137">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="42cc3-137">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

### <span data-ttu-id="42cc3-138">System.String</span><span class="sxs-lookup"><span data-stu-id="42cc3-138">System.String</span></span>

## <span data-ttu-id="42cc3-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="42cc3-139">OUTPUTS</span></span>

### <span data-ttu-id="42cc3-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="42cc3-140">System.Boolean</span></span>

## <span data-ttu-id="42cc3-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="42cc3-141">NOTES</span></span>

## <span data-ttu-id="42cc3-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="42cc3-142">RELATED LINKS</span></span>
