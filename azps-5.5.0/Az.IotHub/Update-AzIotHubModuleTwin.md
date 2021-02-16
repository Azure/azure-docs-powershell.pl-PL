---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/update-aziothubmoduletwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubModuleTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubModuleTwin.md
ms.openlocfilehash: fb2b984453f87422d7a5b9ec5d5178ca6b6c55d5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200050"
---
# <span data-ttu-id="85f9e-101">Update-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="85f9e-101">Update-AzIotHubModuleTwin</span></span>

## <span data-ttu-id="85f9e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85f9e-102">SYNOPSIS</span></span>
<span data-ttu-id="85f9e-103">Aktualizuje tagi i żądane właściwości modułu urządzenia IoT.</span><span class="sxs-lookup"><span data-stu-id="85f9e-103">Updates tags and desired properties of an IoT device module twin.</span></span>

## <span data-ttu-id="85f9e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="85f9e-104">SYNTAX</span></span>

### <span data-ttu-id="85f9e-105">Zestaw zasobów (domyślny)</span><span class="sxs-lookup"><span data-stu-id="85f9e-105">ResourceSet (Default)</span></span>
```
Update-AzIotHubModuleTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 -ModuleId <String> [-Tag <Hashtable>] [-Desired <Hashtable>] [-Partial]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85f9e-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="85f9e-106">InputObjectSet</span></span>
```
Update-AzIotHubModuleTwin [-InputObject] <PSIotHub> [-DeviceId] <String> -ModuleId <String> [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="85f9e-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="85f9e-107">ResourceIdSet</span></span>
```
Update-AzIotHubModuleTwin [-ResourceId] <String> [-DeviceId] <String> -ModuleId <String> [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="85f9e-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="85f9e-108">DESCRIPTION</span></span>
<span data-ttu-id="85f9e-109">Aktualizuje lub zamienia urządzenie.</span><span class="sxs-lookup"><span data-stu-id="85f9e-109">Updates or replaces a device twin.</span></span> <span data-ttu-id="85f9e-110">Aby https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-module-twins uzyskać więcej informacji, zobacz te informacje.</span><span class="sxs-lookup"><span data-stu-id="85f9e-110">See https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-module-twins for more information.</span></span>

## <span data-ttu-id="85f9e-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="85f9e-111">EXAMPLES</span></span>

### <span data-ttu-id="85f9e-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="85f9e-112">Example 1</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Tag $updatedTag -Desired $updatedDesired -Partial
```

<span data-ttu-id="85f9e-113">Zwraca zaktualizowany obiekt modułu urządzenia.</span><span class="sxs-lookup"><span data-stu-id="85f9e-113">Returns the updated device module twin object.</span></span>

### <span data-ttu-id="85f9e-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="85f9e-114">Example 2</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Desired $updatedDesired -Partial
```

<span data-ttu-id="85f9e-115">Zwraca obiekt modułu urządzenia o zaktualizowanych właściwościach.</span><span class="sxs-lookup"><span data-stu-id="85f9e-115">Returns the device module twin object with updated desired properties.</span></span>

### <span data-ttu-id="85f9e-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="85f9e-116">Example 3</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Tag $updatedTag -Partial
```

<span data-ttu-id="85f9e-117">Zwraca obiekt module urządzenia ze zaktualizowaną właściwością tagów.</span><span class="sxs-lookup"><span data-stu-id="85f9e-117">Returns the device module twin object with updated tags property.</span></span>

### <span data-ttu-id="85f9e-118">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="85f9e-118">Example 4</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Tag $updatedTag -Desired $updatedDesired
```

<span data-ttu-id="85f9e-119">Zwraca obiekt moduł urządzenia, który został zastąpiony.</span><span class="sxs-lookup"><span data-stu-id="85f9e-119">Returns the replaced device module twin object.</span></span>

## <span data-ttu-id="85f9e-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="85f9e-120">PARAMETERS</span></span>

### <span data-ttu-id="85f9e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85f9e-121">-DefaultProfile</span></span>
<span data-ttu-id="85f9e-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="85f9e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85f9e-123">— Żądane</span><span class="sxs-lookup"><span data-stu-id="85f9e-123">-Desired</span></span>
<span data-ttu-id="85f9e-124">Dodaj lub zaktualizuj żądaną właściwość w module.</span><span class="sxs-lookup"><span data-stu-id="85f9e-124">Add or update the desired property in a module twin.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85f9e-125">— DeviceId</span><span class="sxs-lookup"><span data-stu-id="85f9e-125">-DeviceId</span></span>
<span data-ttu-id="85f9e-126">Identyfikator urządzenia docelowego.</span><span class="sxs-lookup"><span data-stu-id="85f9e-126">Target Device Id.</span></span>

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

### <span data-ttu-id="85f9e-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="85f9e-127">-InputObject</span></span>
<span data-ttu-id="85f9e-128">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="85f9e-128">IotHub object</span></span>

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

### <span data-ttu-id="85f9e-129">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="85f9e-129">-IotHubName</span></span>
<span data-ttu-id="85f9e-130">Nazwa Centrum Iot</span><span class="sxs-lookup"><span data-stu-id="85f9e-130">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="85f9e-131">- ModuleId</span><span class="sxs-lookup"><span data-stu-id="85f9e-131">-ModuleId</span></span>
<span data-ttu-id="85f9e-132">Identyfikator modułu docelowego.</span><span class="sxs-lookup"><span data-stu-id="85f9e-132">Target Module Id.</span></span>

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

### <span data-ttu-id="85f9e-133">— Częściowe</span><span class="sxs-lookup"><span data-stu-id="85f9e-133">-Partial</span></span>
<span data-ttu-id="85f9e-134">Umożliwia tylko częściową aktualizację tagów i żądanych właściwości modułu.</span><span class="sxs-lookup"><span data-stu-id="85f9e-134">Allows to only partially update the tags and desired properties of a module twin.</span></span>

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

### <span data-ttu-id="85f9e-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85f9e-135">-ResourceGroupName</span></span>
<span data-ttu-id="85f9e-136">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="85f9e-136">Name of the Resource Group</span></span>

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

### <span data-ttu-id="85f9e-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="85f9e-137">-ResourceId</span></span>
<span data-ttu-id="85f9e-138">Identyfikator zasobu w aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="85f9e-138">IotHub Resource Id</span></span>

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

### <span data-ttu-id="85f9e-139">— Tag</span><span class="sxs-lookup"><span data-stu-id="85f9e-139">-Tag</span></span>
<span data-ttu-id="85f9e-140">Dodaj lub zaktualizuj właściwość tagów w module.</span><span class="sxs-lookup"><span data-stu-id="85f9e-140">Add or update the tags property in a module twin.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85f9e-141">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="85f9e-141">-Confirm</span></span>
<span data-ttu-id="85f9e-142">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="85f9e-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85f9e-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85f9e-143">-WhatIf</span></span>
<span data-ttu-id="85f9e-144">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85f9e-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85f9e-145">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="85f9e-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85f9e-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85f9e-146">CommonParameters</span></span>
<span data-ttu-id="85f9e-147">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85f9e-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85f9e-148">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85f9e-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85f9e-149">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="85f9e-149">INPUTS</span></span>

### <span data-ttu-id="85f9e-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="85f9e-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="85f9e-151">System.String</span><span class="sxs-lookup"><span data-stu-id="85f9e-151">System.String</span></span>

## <span data-ttu-id="85f9e-152">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="85f9e-152">OUTPUTS</span></span>

### <span data-ttu-id="85f9e-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleTwin</span><span class="sxs-lookup"><span data-stu-id="85f9e-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleTwin</span></span>

## <span data-ttu-id="85f9e-154">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="85f9e-154">NOTES</span></span>

## <span data-ttu-id="85f9e-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="85f9e-155">RELATED LINKS</span></span>
