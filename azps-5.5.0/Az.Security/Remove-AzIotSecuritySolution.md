---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzIotSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzIotSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzIotSecuritySolution.md
ms.openlocfilehash: 42e483a9783a919dfe45425357052df2389cc8b0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242371"
---
# <span data-ttu-id="f1912-101">Remove-AzIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="f1912-101">Remove-AzIotSecuritySolution</span></span>

## <span data-ttu-id="f1912-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1912-102">SYNOPSIS</span></span>
<span data-ttu-id="f1912-103">Usuwanie rozwiązania zabezpieczającego IoT</span><span class="sxs-lookup"><span data-stu-id="f1912-103">Delete IoT security solution</span></span>

## <span data-ttu-id="f1912-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f1912-104">SYNTAX</span></span>

### <span data-ttu-id="f1912-105">ResourceGroupLevelResource (Default)</span><span class="sxs-lookup"><span data-stu-id="f1912-105">ResourceGroupLevelResource (Default)</span></span>
```
Remove-AzIotSecuritySolution -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1912-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="f1912-106">ResourceId</span></span>
```
Remove-AzIotSecuritySolution -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1912-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="f1912-107">InputObject</span></span>
```
Remove-AzIotSecuritySolution -InputObject <PSIotSecuritySolution> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1912-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="f1912-108">DESCRIPTION</span></span>
<span data-ttu-id="f1912-109">Polecenie Remove-AzIotSecuritySolution cmdlet usuwa określone rozwiązanie zabezpieczeń iot.</span><span class="sxs-lookup"><span data-stu-id="f1912-109">The Remove-AzIotSecuritySolution cmdlet deletes a specific iot security solution.</span></span> <span data-ttu-id="f1912-110">Rozwiązanie zabezpieczeń IoT zbiera dane zabezpieczeń i zdarzenia z urządzeń iot i centrum iot, aby chronić zagrożenia i je wykrywać.</span><span class="sxs-lookup"><span data-stu-id="f1912-110">The IoT security solution collects security data and events from iot devices and iot hub to help prevent and detect threats.</span></span>

## <span data-ttu-id="f1912-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f1912-111">EXAMPLES</span></span>

### <span data-ttu-id="f1912-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f1912-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotSecuritySolution -Name "MySample" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="f1912-113">Usuwanie rozwiązania zabezpieczeń IoT "MySample" za pomocą grupy zasobów "MyResourceGroup"</span><span class="sxs-lookup"><span data-stu-id="f1912-113">Delete IoT security solution "MySample" with resource group "MyResourceGroup"</span></span>

## <span data-ttu-id="f1912-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f1912-114">PARAMETERS</span></span>

### <span data-ttu-id="f1912-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1912-115">-DefaultProfile</span></span>
<span data-ttu-id="f1912-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f1912-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1912-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f1912-117">-InputObject</span></span>
<span data-ttu-id="f1912-118">Obiekt Input.</span><span class="sxs-lookup"><span data-stu-id="f1912-118">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f1912-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f1912-119">-Name</span></span>
<span data-ttu-id="f1912-120">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="f1912-120">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1912-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f1912-121">-PassThru</span></span>
<span data-ttu-id="f1912-122">Sprawdź, czy operacja się powiedzie.</span><span class="sxs-lookup"><span data-stu-id="f1912-122">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="f1912-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1912-123">-ResourceGroupName</span></span>
<span data-ttu-id="f1912-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f1912-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1912-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f1912-125">-ResourceId</span></span>
<span data-ttu-id="f1912-126">Identyfikator zasobu zabezpieczeń, dla którego chcesz wywołać polecenie.</span><span class="sxs-lookup"><span data-stu-id="f1912-126">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1912-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f1912-127">-Confirm</span></span>
<span data-ttu-id="f1912-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f1912-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1912-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1912-129">-WhatIf</span></span>
<span data-ttu-id="f1912-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1912-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1912-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f1912-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1912-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1912-132">CommonParameters</span></span>
<span data-ttu-id="f1912-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1912-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1912-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f1912-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1912-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f1912-135">INPUTS</span></span>

### <span data-ttu-id="f1912-136">System.String</span><span class="sxs-lookup"><span data-stu-id="f1912-136">System.String</span></span>

### <span data-ttu-id="f1912-137">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="f1912-137">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

## <span data-ttu-id="f1912-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f1912-138">OUTPUTS</span></span>

### <span data-ttu-id="f1912-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f1912-139">System.Boolean</span></span>

## <span data-ttu-id="f1912-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f1912-140">NOTES</span></span>

## <span data-ttu-id="f1912-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f1912-141">RELATED LINKS</span></span>
