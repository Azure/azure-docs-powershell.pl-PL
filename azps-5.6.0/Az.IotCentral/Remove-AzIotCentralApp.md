---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/powershell/module/az.iotcentral/remove-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Remove-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Remove-AzIotCentralApp.md
ms.openlocfilehash: 29a53b49e579ab337c2345a15c86c4c27aaffe8e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997970"
---
# <span data-ttu-id="f19be-101">Remove-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="f19be-101">Remove-AzIotCentralApp</span></span>

## <span data-ttu-id="f19be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f19be-102">SYNOPSIS</span></span>
<span data-ttu-id="f19be-103">Usuwa aplikację centralną IoT.</span><span class="sxs-lookup"><span data-stu-id="f19be-103">Deletes an IoT Central Application.</span></span>

## <span data-ttu-id="f19be-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f19be-104">SYNTAX</span></span>

### <span data-ttu-id="f19be-105">ResourceIdParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="f19be-105">ResourceIdParameterSet (Default)</span></span>
```
Remove-AzIotCentralApp [-PassThru] -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f19be-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f19be-106">InputObjectParameterSet</span></span>
```
Remove-AzIotCentralApp [-PassThru] -InputObject <PSIotCentralApp> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f19be-107">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="f19be-107">InteractiveIotCentralParameterSet</span></span>
```
Remove-AzIotCentralApp [-PassThru] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f19be-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="f19be-108">DESCRIPTION</span></span>
<span data-ttu-id="f19be-109">Usuwa istniejącą aplikację centralną IoT.</span><span class="sxs-lookup"><span data-stu-id="f19be-109">Deletes an existing IoT Central Application.</span></span>

## <span data-ttu-id="f19be-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f19be-110">EXAMPLES</span></span>

### <span data-ttu-id="f19be-111">Przykład 1. Usuwanie i aplikacja centralna IoT</span><span class="sxs-lookup"><span data-stu-id="f19be-111">Example 1 Delete and IoT Central Application</span></span>
```powershell
PS C:\> Remove-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName"
```

<span data-ttu-id="f19be-112">Usuwa podaną aplikację centralną IoT.</span><span class="sxs-lookup"><span data-stu-id="f19be-112">Deletes the provided IoT Central Application.</span></span>

## <span data-ttu-id="f19be-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f19be-113">PARAMETERS</span></span>

### <span data-ttu-id="f19be-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="f19be-114">-AsJob</span></span>
<span data-ttu-id="f19be-115">Uruchom polecenie cmdlet jako zadanie w tle.</span><span class="sxs-lookup"><span data-stu-id="f19be-115">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="f19be-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f19be-116">-DefaultProfile</span></span>
<span data-ttu-id="f19be-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f19be-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f19be-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f19be-118">-InputObject</span></span>
<span data-ttu-id="f19be-119">Iot Central Application Input Object.</span><span class="sxs-lookup"><span data-stu-id="f19be-119">Iot Central Application Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f19be-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f19be-120">-Name</span></span>
<span data-ttu-id="f19be-121">Nazwa centralnego zasobu aplikacji IOT.</span><span class="sxs-lookup"><span data-stu-id="f19be-121">Name of the Iot Central Application Resource.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f19be-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f19be-122">-PassThru</span></span>
<span data-ttu-id="f19be-123">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="f19be-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="f19be-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f19be-124">-ResourceGroupName</span></span>
<span data-ttu-id="f19be-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f19be-125">Name of the Resource Group.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f19be-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f19be-126">-ResourceId</span></span>
<span data-ttu-id="f19be-127">Identyfikator zasobu aplikacji centralnej.</span><span class="sxs-lookup"><span data-stu-id="f19be-127">Iot Central Application Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f19be-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f19be-128">-Confirm</span></span>
<span data-ttu-id="f19be-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f19be-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f19be-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f19be-130">-WhatIf</span></span>
<span data-ttu-id="f19be-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f19be-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f19be-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f19be-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f19be-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f19be-133">CommonParameters</span></span>
<span data-ttu-id="f19be-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f19be-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f19be-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f19be-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f19be-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f19be-136">INPUTS</span></span>

### <span data-ttu-id="f19be-137">System.String</span><span class="sxs-lookup"><span data-stu-id="f19be-137">System.String</span></span>

### <span data-ttu-id="f19be-138">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="f19be-138">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="f19be-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f19be-139">OUTPUTS</span></span>

### <span data-ttu-id="f19be-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f19be-140">System.Boolean</span></span>

## <span data-ttu-id="f19be-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f19be-141">NOTES</span></span>

## <span data-ttu-id="f19be-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f19be-142">RELATED LINKS</span></span>
