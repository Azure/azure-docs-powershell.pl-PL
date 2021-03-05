---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/remove-aziothubmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubModule.md
ms.openlocfilehash: 6e03e6dcf5cce193452fd03cee1f48bc387335c6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970753"
---
# <span data-ttu-id="770bf-101">Remove-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="770bf-101">Remove-AzIotHubModule</span></span>

## <span data-ttu-id="770bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="770bf-102">SYNOPSIS</span></span>
<span data-ttu-id="770bf-103">Usuń moduły na docelowym urządzeniu IoT w Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="770bf-103">Delete module(s) on a target IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="770bf-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="770bf-104">SYNTAX</span></span>

### <span data-ttu-id="770bf-105">Zestaw zasobów (domyślny)</span><span class="sxs-lookup"><span data-stu-id="770bf-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubModule [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="770bf-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="770bf-106">InputObjectSet</span></span>
```
Remove-AzIotHubModule [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="770bf-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="770bf-107">ResourceIdSet</span></span>
```
Remove-AzIotHubModule [-ResourceId] <String> [-DeviceId] <String> [-ModuleId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="770bf-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="770bf-108">DESCRIPTION</span></span>
<span data-ttu-id="770bf-109">Usuń moduły na docelowym urządzeniu IoT w Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="770bf-109">Delete module(s) on a target IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="770bf-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="770bf-110">EXAMPLES</span></span>

### <span data-ttu-id="770bf-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="770bf-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -PassThru

True
```

<span data-ttu-id="770bf-112">Usuń moduł urządzenia Iot.</span><span class="sxs-lookup"><span data-stu-id="770bf-112">Delete an Iot device module.</span></span>

### <span data-ttu-id="770bf-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="770bf-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIotHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -PassThru

True
```

<span data-ttu-id="770bf-114">Usuń wszystkie moduły urządzeń Iot.</span><span class="sxs-lookup"><span data-stu-id="770bf-114">Delete all Iot device modules.</span></span>

## <span data-ttu-id="770bf-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="770bf-115">PARAMETERS</span></span>

### <span data-ttu-id="770bf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="770bf-116">-DefaultProfile</span></span>
<span data-ttu-id="770bf-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="770bf-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="770bf-118">— DeviceId</span><span class="sxs-lookup"><span data-stu-id="770bf-118">-DeviceId</span></span>
<span data-ttu-id="770bf-119">Identyfikator urządzenia docelowego.</span><span class="sxs-lookup"><span data-stu-id="770bf-119">Target Device Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="770bf-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="770bf-120">-InputObject</span></span>
<span data-ttu-id="770bf-121">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="770bf-121">IotHub object</span></span>

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

### <span data-ttu-id="770bf-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="770bf-122">-IotHubName</span></span>
<span data-ttu-id="770bf-123">Nazwa Centrum Iot</span><span class="sxs-lookup"><span data-stu-id="770bf-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="770bf-124">- ModuleId</span><span class="sxs-lookup"><span data-stu-id="770bf-124">-ModuleId</span></span>
<span data-ttu-id="770bf-125">Identyfikator modułu docelowego.</span><span class="sxs-lookup"><span data-stu-id="770bf-125">Target Module Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="770bf-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="770bf-126">-PassThru</span></span>
<span data-ttu-id="770bf-127">Zwraca obiekt logiczny.</span><span class="sxs-lookup"><span data-stu-id="770bf-127">Allows to return the boolean object.</span></span>
<span data-ttu-id="770bf-128">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="770bf-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="770bf-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="770bf-129">-ResourceGroupName</span></span>
<span data-ttu-id="770bf-130">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="770bf-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="770bf-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="770bf-131">-ResourceId</span></span>
<span data-ttu-id="770bf-132">Identyfikator zasobu w aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="770bf-132">IotHub Resource Id</span></span>

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

### <span data-ttu-id="770bf-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="770bf-133">-Confirm</span></span>
<span data-ttu-id="770bf-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="770bf-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="770bf-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="770bf-135">-WhatIf</span></span>
<span data-ttu-id="770bf-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="770bf-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="770bf-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="770bf-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="770bf-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="770bf-138">CommonParameters</span></span>
<span data-ttu-id="770bf-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="770bf-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="770bf-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="770bf-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="770bf-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="770bf-141">INPUTS</span></span>

### <span data-ttu-id="770bf-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="770bf-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="770bf-143">System.String</span><span class="sxs-lookup"><span data-stu-id="770bf-143">System.String</span></span>

## <span data-ttu-id="770bf-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="770bf-144">OUTPUTS</span></span>

### <span data-ttu-id="770bf-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="770bf-145">System.Boolean</span></span>

## <span data-ttu-id="770bf-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="770bf-146">NOTES</span></span>

## <span data-ttu-id="770bf-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="770bf-147">RELATED LINKS</span></span>
