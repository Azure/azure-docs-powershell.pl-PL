---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/remove-azappserviceenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzAppServiceEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzAppServiceEnvironment.md
ms.openlocfilehash: 73c7a7b76f882678612eb6f2a1fb682637705858
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970081"
---
# <span data-ttu-id="6235b-101">Remove-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="6235b-101">Remove-AzAppServiceEnvironment</span></span>

## <span data-ttu-id="6235b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6235b-102">SYNOPSIS</span></span>
<span data-ttu-id="6235b-103">Usuń środowisko usługi aplikacji.</span><span class="sxs-lookup"><span data-stu-id="6235b-103">Remove App Service Environment.</span></span>

## <span data-ttu-id="6235b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6235b-104">SYNTAX</span></span>

### <span data-ttu-id="6235b-105">InputValuesParameterSet</span><span class="sxs-lookup"><span data-stu-id="6235b-105">InputValuesParameterSet</span></span>
```
Remove-AzAppServiceEnvironment [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6235b-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6235b-106">InputObjectParameterSet</span></span>
```
Remove-AzAppServiceEnvironment [-Force] [-PassThru] [-AsJob] -InputObject <PSAppServiceEnvironment>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6235b-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="6235b-107">DESCRIPTION</span></span>
<span data-ttu-id="6235b-108">Polecenie **cmdlet Remove-AzAppServiceEnvironment** usuwa środowisko usługi aplikacji.</span><span class="sxs-lookup"><span data-stu-id="6235b-108">The **Remove-AzAppServiceEnvironment** cmdlet removes an App Service Environment.</span></span> <span data-ttu-id="6235b-109">Przed usunięciem ase'a należy usunąć każdy plan usług aplikacji.</span><span class="sxs-lookup"><span data-stu-id="6235b-109">Any App Service Plan must be deleted prior to deleting the ASE.</span></span>

## <span data-ttu-id="6235b-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6235b-110">EXAMPLES</span></span>

### <span data-ttu-id="6235b-111">Przykład 1. Usuwanie środowiska usługi aplikacji</span><span class="sxs-lookup"><span data-stu-id="6235b-111">Example 1 : Delete an App Service Environment</span></span>
```powershell
PS C:\> Remove-AzAppServiceEnvironment -ResourceGroupName MyResourceGroup -Name MyAseName
```

<span data-ttu-id="6235b-112">Usuwanie środowiska usługi aplikacji</span><span class="sxs-lookup"><span data-stu-id="6235b-112">Delete an App Service Environment</span></span>

## <span data-ttu-id="6235b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6235b-113">PARAMETERS</span></span>

### <span data-ttu-id="6235b-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="6235b-114">-AsJob</span></span>
<span data-ttu-id="6235b-115">Uruchom polecenie cmdlet w tle i zwróć zadanie w celu śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="6235b-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="6235b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6235b-116">-DefaultProfile</span></span>
<span data-ttu-id="6235b-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6235b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6235b-118">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="6235b-118">-Force</span></span>
<span data-ttu-id="6235b-119">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6235b-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="6235b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6235b-120">-InputObject</span></span>
<span data-ttu-id="6235b-121">Obiekt środowiska usługi aplikacji</span><span class="sxs-lookup"><span data-stu-id="6235b-121">The app service environment object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServiceEnvironment
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6235b-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="6235b-122">-Name</span></span>
<span data-ttu-id="6235b-123">Nazwa środowiska usługi aplikacji.</span><span class="sxs-lookup"><span data-stu-id="6235b-123">The name of the app service environment.</span></span>

```yaml
Type: System.String
Parameter Sets: InputValuesParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6235b-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6235b-124">-PassThru</span></span>
<span data-ttu-id="6235b-125">Stan zwrotu.</span><span class="sxs-lookup"><span data-stu-id="6235b-125">Return status.</span></span>

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

### <span data-ttu-id="6235b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6235b-126">-ResourceGroupName</span></span>
<span data-ttu-id="6235b-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6235b-127">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: InputValuesParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6235b-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6235b-128">-Confirm</span></span>
<span data-ttu-id="6235b-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6235b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6235b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6235b-130">-WhatIf</span></span>
<span data-ttu-id="6235b-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6235b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6235b-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="6235b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6235b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6235b-133">CommonParameters</span></span>
<span data-ttu-id="6235b-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6235b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6235b-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6235b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6235b-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6235b-136">INPUTS</span></span>

### <span data-ttu-id="6235b-137">Brak</span><span class="sxs-lookup"><span data-stu-id="6235b-137">None</span></span>

## <span data-ttu-id="6235b-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6235b-138">OUTPUTS</span></span>

### <span data-ttu-id="6235b-139">System.Object</span><span class="sxs-lookup"><span data-stu-id="6235b-139">System.Object</span></span>
## <span data-ttu-id="6235b-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6235b-140">NOTES</span></span>

## <span data-ttu-id="6235b-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6235b-141">RELATED LINKS</span></span>

[<span data-ttu-id="6235b-142">New-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="6235b-142">New-AzAppServiceEnvironment</span></span>](./New-AzAppServiceEnvironment.md)

[<span data-ttu-id="6235b-143">Get-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="6235b-143">Get-AzAppServiceEnvironment</span></span>](./Get-AzAppServiceEnvironment.md)

[<span data-ttu-id="6235b-144">New-AzAppServiceEnvironmentInboundServices</span><span class="sxs-lookup"><span data-stu-id="6235b-144">New-AzAppServiceEnvironmentInboundServices</span></span>](./New-AzAppServiceEnvironmentInboundServices.md)