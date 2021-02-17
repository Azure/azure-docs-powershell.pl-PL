---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubedgemodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubEdgeModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubEdgeModule.md
ms.openlocfilehash: 5316b6bae6bfc64f791959bb6e236c861833ed4c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180506"
---
# <span data-ttu-id="67735-101">Set-AzIotHubEdgeModule</span><span class="sxs-lookup"><span data-stu-id="67735-101">Set-AzIotHubEdgeModule</span></span>

## <span data-ttu-id="67735-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67735-102">SYNOPSIS</span></span>
<span data-ttu-id="67735-103">Ustaw moduły brzegowe na jednym urządzeniu brzegowym.</span><span class="sxs-lookup"><span data-stu-id="67735-103">Set edge modules on a single edge device.</span></span>

## <span data-ttu-id="67735-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="67735-104">SYNTAX</span></span>

### <span data-ttu-id="67735-105">Zestaw zasobów (domyślny)</span><span class="sxs-lookup"><span data-stu-id="67735-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubEdgeModule [-ResourceGroupName] <String> [-IotHubName] <String> -DeviceId <String>
 -ModulesContent <Hashtable> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="67735-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="67735-106">InputObjectSet</span></span>
```
Set-AzIotHubEdgeModule [-InputObject] <PSIotHub> -DeviceId <String> -ModulesContent <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67735-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="67735-107">ResourceIdSet</span></span>
```
Set-AzIotHubEdgeModule [-ResourceId] <String> -DeviceId <String> -ModulesContent <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67735-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="67735-108">DESCRIPTION</span></span>
<span data-ttu-id="67735-109">Powoduje zastosowanie zawartości konfiguracji podanych modułów do określonego urządzenia brzegowego.</span><span class="sxs-lookup"><span data-stu-id="67735-109">Applies the provided modules configuration content to the specified edge device.</span></span>
<span data-ttu-id="67735-110">Uwaga: Po wykonaniu polecenie wyprowadzi kolekcję modułów zastosowanych do urządzenia.</span><span class="sxs-lookup"><span data-stu-id="67735-110">Note: Upon execution the command will output the collection of modules applied to the device.</span></span>

## <span data-ttu-id="67735-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="67735-111">EXAMPLES</span></span>

### <span data-ttu-id="67735-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="67735-112">Example 1</span></span>
```powershell
PS C:\> $content = Get-Content "C:/Edge/modules.json" | ConvertFrom-Json -AsHashtable
PS C:\> Set-AzIotHubEdgeModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myEdgeDevice1" -ModulesContent $content
```

<span data-ttu-id="67735-113">Testowanie modułów brzegowych podczas opracowywania przez ustawienie modułów na urządzeniu docelowym.</span><span class="sxs-lookup"><span data-stu-id="67735-113">Test edge modules while in development by setting modules on a target device.</span></span>

## <span data-ttu-id="67735-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="67735-114">PARAMETERS</span></span>

### <span data-ttu-id="67735-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67735-115">-DefaultProfile</span></span>
<span data-ttu-id="67735-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="67735-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67735-117">— DeviceId</span><span class="sxs-lookup"><span data-stu-id="67735-117">-DeviceId</span></span>
<span data-ttu-id="67735-118">Identyfikator urządzenia target Edge.</span><span class="sxs-lookup"><span data-stu-id="67735-118">Target Edge Device Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67735-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="67735-119">-InputObject</span></span>
<span data-ttu-id="67735-120">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="67735-120">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="67735-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="67735-121">-IotHubName</span></span>
<span data-ttu-id="67735-122">Nazwa Centrum Iot</span><span class="sxs-lookup"><span data-stu-id="67735-122">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67735-123">-ModulesContent</span><span class="sxs-lookup"><span data-stu-id="67735-123">-ModulesContent</span></span>
<span data-ttu-id="67735-124">Zawartość konfiguracji modułów dla urządzeń przeglądarki IoT Edge.</span><span class="sxs-lookup"><span data-stu-id="67735-124">Configuration content of modules for IoT Edge devices.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67735-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67735-125">-ResourceGroupName</span></span>
<span data-ttu-id="67735-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="67735-126">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67735-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="67735-127">-ResourceId</span></span>
<span data-ttu-id="67735-128">Identyfikator zasobu w aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="67735-128">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67735-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="67735-129">-Confirm</span></span>
<span data-ttu-id="67735-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="67735-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67735-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67735-131">-WhatIf</span></span>
<span data-ttu-id="67735-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67735-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67735-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="67735-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67735-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67735-134">CommonParameters</span></span>
<span data-ttu-id="67735-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67735-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67735-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67735-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67735-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="67735-137">INPUTS</span></span>

### <span data-ttu-id="67735-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="67735-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="67735-139">System.String</span><span class="sxs-lookup"><span data-stu-id="67735-139">System.String</span></span>

## <span data-ttu-id="67735-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="67735-140">OUTPUTS</span></span>

### <span data-ttu-id="67735-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSModules[]</span><span class="sxs-lookup"><span data-stu-id="67735-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSModules[]</span></span>

## <span data-ttu-id="67735-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="67735-142">NOTES</span></span>

## <span data-ttu-id="67735-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="67735-143">RELATED LINKS</span></span>
