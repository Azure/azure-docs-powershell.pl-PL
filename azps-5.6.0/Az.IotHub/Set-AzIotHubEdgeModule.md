---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/set-aziothubedgemodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubEdgeModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubEdgeModule.md
ms.openlocfilehash: f3bc819c7050300c82f039981b1df34010771eb7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952625"
---
# <span data-ttu-id="a742a-101">Set-AzIotHubEdgeModule</span><span class="sxs-lookup"><span data-stu-id="a742a-101">Set-AzIotHubEdgeModule</span></span>

## <span data-ttu-id="a742a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a742a-102">SYNOPSIS</span></span>
<span data-ttu-id="a742a-103">Ustaw moduły brzegowe na jednym urządzeniu brzegowym.</span><span class="sxs-lookup"><span data-stu-id="a742a-103">Set edge modules on a single edge device.</span></span>

## <span data-ttu-id="a742a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a742a-104">SYNTAX</span></span>

### <span data-ttu-id="a742a-105">Zestaw zasobów (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a742a-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubEdgeModule [-ResourceGroupName] <String> [-IotHubName] <String> -DeviceId <String>
 -ModulesContent <Hashtable> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a742a-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a742a-106">InputObjectSet</span></span>
```
Set-AzIotHubEdgeModule [-InputObject] <PSIotHub> -DeviceId <String> -ModulesContent <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a742a-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a742a-107">ResourceIdSet</span></span>
```
Set-AzIotHubEdgeModule [-ResourceId] <String> -DeviceId <String> -ModulesContent <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a742a-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="a742a-108">DESCRIPTION</span></span>
<span data-ttu-id="a742a-109">Powoduje zastosowanie zawartości konfiguracji podanych modułów do określonego urządzenia brzegowego.</span><span class="sxs-lookup"><span data-stu-id="a742a-109">Applies the provided modules configuration content to the specified edge device.</span></span>
<span data-ttu-id="a742a-110">Uwaga: Po wykonaniu polecenie wyprowadzi kolekcję modułów zastosowanych do urządzenia.</span><span class="sxs-lookup"><span data-stu-id="a742a-110">Note: Upon execution the command will output the collection of modules applied to the device.</span></span>

## <span data-ttu-id="a742a-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a742a-111">EXAMPLES</span></span>

### <span data-ttu-id="a742a-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a742a-112">Example 1</span></span>
```powershell
PS C:\> $content = Get-Content "C:/Edge/modules.json" | ConvertFrom-Json -AsHashtable
PS C:\> Set-AzIotHubEdgeModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myEdgeDevice1" -ModulesContent $content
```

<span data-ttu-id="a742a-113">Testowanie modułów brzegowych podczas opracowywania przez ustawienie modułów na urządzeniu docelowym.</span><span class="sxs-lookup"><span data-stu-id="a742a-113">Test edge modules while in development by setting modules on a target device.</span></span>

## <span data-ttu-id="a742a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a742a-114">PARAMETERS</span></span>

### <span data-ttu-id="a742a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a742a-115">-DefaultProfile</span></span>
<span data-ttu-id="a742a-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a742a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a742a-117">— DeviceId</span><span class="sxs-lookup"><span data-stu-id="a742a-117">-DeviceId</span></span>
<span data-ttu-id="a742a-118">Identyfikator urządzenia target Edge.</span><span class="sxs-lookup"><span data-stu-id="a742a-118">Target Edge Device Id.</span></span>

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

### <span data-ttu-id="a742a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a742a-119">-InputObject</span></span>
<span data-ttu-id="a742a-120">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="a742a-120">IotHub object</span></span>

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

### <span data-ttu-id="a742a-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="a742a-121">-IotHubName</span></span>
<span data-ttu-id="a742a-122">Nazwa Centrum Iot</span><span class="sxs-lookup"><span data-stu-id="a742a-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="a742a-123">-ModulesContent</span><span class="sxs-lookup"><span data-stu-id="a742a-123">-ModulesContent</span></span>
<span data-ttu-id="a742a-124">Zawartość konfiguracji modułów dla urządzeń przeglądarki IoT Edge.</span><span class="sxs-lookup"><span data-stu-id="a742a-124">Configuration content of modules for IoT Edge devices.</span></span>

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

### <span data-ttu-id="a742a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a742a-125">-ResourceGroupName</span></span>
<span data-ttu-id="a742a-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="a742a-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="a742a-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a742a-127">-ResourceId</span></span>
<span data-ttu-id="a742a-128">Identyfikator zasobu w aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="a742a-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="a742a-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a742a-129">-Confirm</span></span>
<span data-ttu-id="a742a-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a742a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a742a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a742a-131">-WhatIf</span></span>
<span data-ttu-id="a742a-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a742a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a742a-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a742a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a742a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a742a-134">CommonParameters</span></span>
<span data-ttu-id="a742a-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a742a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a742a-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a742a-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a742a-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a742a-137">INPUTS</span></span>

### <span data-ttu-id="a742a-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="a742a-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="a742a-139">System.String</span><span class="sxs-lookup"><span data-stu-id="a742a-139">System.String</span></span>

## <span data-ttu-id="a742a-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a742a-140">OUTPUTS</span></span>

### <span data-ttu-id="a742a-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSModules[]</span><span class="sxs-lookup"><span data-stu-id="a742a-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSModules[]</span></span>

## <span data-ttu-id="a742a-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a742a-142">NOTES</span></span>

## <span data-ttu-id="a742a-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a742a-143">RELATED LINKS</span></span>
