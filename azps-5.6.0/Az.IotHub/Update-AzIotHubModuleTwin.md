---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/update-aziothubmoduletwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubModuleTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubModuleTwin.md
ms.openlocfilehash: 72e9b809ac2b2894b34aefeddd17473cc29d9f35
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983114"
---
# <span data-ttu-id="a9cc7-101">Update-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="a9cc7-101">Update-AzIotHubModuleTwin</span></span>

## <span data-ttu-id="a9cc7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9cc7-102">SYNOPSIS</span></span>
<span data-ttu-id="a9cc7-103">Aktualizuje tagi i żądane właściwości modułu urządzenia IoT.</span><span class="sxs-lookup"><span data-stu-id="a9cc7-103">Updates tags and desired properties of an IoT device module twin.</span></span>

## <span data-ttu-id="a9cc7-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a9cc7-104">SYNTAX</span></span>

### <span data-ttu-id="a9cc7-105">Zestaw zasobów (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a9cc7-105">ResourceSet (Default)</span></span>
```
Update-AzIotHubModuleTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 -ModuleId <String> [-Tag <Hashtable>] [-Desired <Hashtable>] [-Partial]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9cc7-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a9cc7-106">InputObjectSet</span></span>
```
Update-AzIotHubModuleTwin [-InputObject] <PSIotHub> [-DeviceId] <String> -ModuleId <String> [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a9cc7-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a9cc7-107">ResourceIdSet</span></span>
```
Update-AzIotHubModuleTwin [-ResourceId] <String> [-DeviceId] <String> -ModuleId <String> [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a9cc7-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="a9cc7-108">DESCRIPTION</span></span>
<span data-ttu-id="a9cc7-109">Aktualizuje lub zamienia urządzenie.</span><span class="sxs-lookup"><span data-stu-id="a9cc7-109">Updates or replaces a device twin.</span></span> <span data-ttu-id="a9cc7-110">Aby https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-module-twins uzyskać więcej informacji, zobacz te informacje.</span><span class="sxs-lookup"><span data-stu-id="a9cc7-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-module-twins for more information.</span></span>

## <span data-ttu-id="a9cc7-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a9cc7-111">EXAMPLES</span></span>

### <span data-ttu-id="a9cc7-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a9cc7-112">Example 1</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Tag $updatedTag -Desired $updatedDesired -Partial
```

<span data-ttu-id="a9cc7-113">Zwraca zaktualizowany obiekt modułu urządzenia.</span><span class="sxs-lookup"><span data-stu-id="a9cc7-113">Returns the updated device module twin object.</span></span>

### <span data-ttu-id="a9cc7-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="a9cc7-114">Example 2</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Desired $updatedDesired -Partial
```

<span data-ttu-id="a9cc7-115">Zwraca obiekt modułu urządzenia o zaktualizowanych właściwościach.</span><span class="sxs-lookup"><span data-stu-id="a9cc7-115">Returns the device module twin object with updated desired properties.</span></span>

### <span data-ttu-id="a9cc7-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="a9cc7-116">Example 3</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Tag $updatedTag -Partial
```

<span data-ttu-id="a9cc7-117">Zwraca obiekt module urządzenia ze zaktualizowaną właściwością tagów.</span><span class="sxs-lookup"><span data-stu-id="a9cc7-117">Returns the device module twin object with updated tags property.</span></span>

### <span data-ttu-id="a9cc7-118">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="a9cc7-118">Example 4</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Tag $updatedTag -Desired $updatedDesired
```

<span data-ttu-id="a9cc7-119">Zwraca obiekt moduł urządzenia, który został zastąpiony.</span><span class="sxs-lookup"><span data-stu-id="a9cc7-119">Returns the replaced device module twin object.</span></span>

## <span data-ttu-id="a9cc7-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a9cc7-120">PARAMETERS</span></span>

### <span data-ttu-id="a9cc7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9cc7-121">-DefaultProfile</span></span>
<span data-ttu-id="a9cc7-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a9cc7-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9cc7-123">— Żądane</span><span class="sxs-lookup"><span data-stu-id="a9cc7-123">-Desired</span></span>
<span data-ttu-id="a9cc7-124">Dodaj lub zaktualizuj żądaną właściwość w module.</span><span class="sxs-lookup"><span data-stu-id="a9cc7-124">Add or update the desired property in a module twin.</span></span>

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

### <span data-ttu-id="a9cc7-125">— DeviceId</span><span class="sxs-lookup"><span data-stu-id="a9cc7-125">-DeviceId</span></span>
<span data-ttu-id="a9cc7-126">Identyfikator urządzenia docelowego.</span><span class="sxs-lookup"><span data-stu-id="a9cc7-126">Target Device Id.</span></span>

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

### <span data-ttu-id="a9cc7-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a9cc7-127">-InputObject</span></span>
<span data-ttu-id="a9cc7-128">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="a9cc7-128">IotHub object</span></span>

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

### <span data-ttu-id="a9cc7-129">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="a9cc7-129">-IotHubName</span></span>
<span data-ttu-id="a9cc7-130">Nazwa Centrum Iot</span><span class="sxs-lookup"><span data-stu-id="a9cc7-130">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="a9cc7-131">- ModuleId</span><span class="sxs-lookup"><span data-stu-id="a9cc7-131">-ModuleId</span></span>
<span data-ttu-id="a9cc7-132">Identyfikator modułu docelowego.</span><span class="sxs-lookup"><span data-stu-id="a9cc7-132">Target Module Id.</span></span>

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

### <span data-ttu-id="a9cc7-133">— Częściowe</span><span class="sxs-lookup"><span data-stu-id="a9cc7-133">-Partial</span></span>
<span data-ttu-id="a9cc7-134">Umożliwia tylko częściową aktualizację tagów i żądanych właściwości modułu.</span><span class="sxs-lookup"><span data-stu-id="a9cc7-134">Allows to only partially update the tags and desired properties of a module twin.</span></span>

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

### <span data-ttu-id="a9cc7-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9cc7-135">-ResourceGroupName</span></span>
<span data-ttu-id="a9cc7-136">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="a9cc7-136">Name of the Resource Group</span></span>

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

### <span data-ttu-id="a9cc7-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a9cc7-137">-ResourceId</span></span>
<span data-ttu-id="a9cc7-138">Identyfikator zasobu w aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="a9cc7-138">IotHub Resource Id</span></span>

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

### <span data-ttu-id="a9cc7-139">— Tag</span><span class="sxs-lookup"><span data-stu-id="a9cc7-139">-Tag</span></span>
<span data-ttu-id="a9cc7-140">Dodaj lub zaktualizuj właściwość tagów w module.</span><span class="sxs-lookup"><span data-stu-id="a9cc7-140">Add or update the tags property in a module twin.</span></span>

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

### <span data-ttu-id="a9cc7-141">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a9cc7-141">-Confirm</span></span>
<span data-ttu-id="a9cc7-142">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a9cc7-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9cc7-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9cc7-143">-WhatIf</span></span>
<span data-ttu-id="a9cc7-144">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9cc7-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9cc7-145">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a9cc7-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9cc7-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9cc7-146">CommonParameters</span></span>
<span data-ttu-id="a9cc7-147">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9cc7-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9cc7-148">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9cc7-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9cc7-149">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a9cc7-149">INPUTS</span></span>

### <span data-ttu-id="a9cc7-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="a9cc7-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="a9cc7-151">System.String</span><span class="sxs-lookup"><span data-stu-id="a9cc7-151">System.String</span></span>

## <span data-ttu-id="a9cc7-152">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a9cc7-152">OUTPUTS</span></span>

### <span data-ttu-id="a9cc7-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleTwin</span><span class="sxs-lookup"><span data-stu-id="a9cc7-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleTwin</span></span>

## <span data-ttu-id="a9cc7-154">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a9cc7-154">NOTES</span></span>

## <span data-ttu-id="a9cc7-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a9cc7-155">RELATED LINKS</span></span>
