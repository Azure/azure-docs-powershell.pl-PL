---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/update-aziothubdevicetwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubDeviceTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubDeviceTwin.md
ms.openlocfilehash: 84f1485f84996c1c0e98768914afffd501722ab7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978481"
---
# <span data-ttu-id="67a3f-101">Update-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="67a3f-101">Update-AzIotHubDeviceTwin</span></span>

## <span data-ttu-id="67a3f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67a3f-102">SYNOPSIS</span></span>
<span data-ttu-id="67a3f-103">Aktualizuje tagi i żądane właściwości urządzenia.</span><span class="sxs-lookup"><span data-stu-id="67a3f-103">Updates tags and desired properties of a device twin.</span></span>

## <span data-ttu-id="67a3f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="67a3f-104">SYNTAX</span></span>

### <span data-ttu-id="67a3f-105">Zestaw zasobów (domyślny)</span><span class="sxs-lookup"><span data-stu-id="67a3f-105">ResourceSet (Default)</span></span>
```
Update-AzIotHubDeviceTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Tag <Hashtable>] [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67a3f-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="67a3f-106">InputObjectSet</span></span>
```
Update-AzIotHubDeviceTwin [-InputObject] <PSIotHub> [-DeviceId] <String> [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="67a3f-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="67a3f-107">ResourceIdSet</span></span>
```
Update-AzIotHubDeviceTwin [-ResourceId] <String> [-DeviceId] <String> [-Tag <Hashtable>] [-Desired <Hashtable>]
 [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67a3f-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="67a3f-108">DESCRIPTION</span></span>
<span data-ttu-id="67a3f-109">Aktualizuje lub zamienia urządzenie.</span><span class="sxs-lookup"><span data-stu-id="67a3f-109">Updates or replaces a device twin.</span></span> <span data-ttu-id="67a3f-110">Aby https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins uzyskać więcej informacji, zobacz te informacje.</span><span class="sxs-lookup"><span data-stu-id="67a3f-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins for more information.</span></span>

## <span data-ttu-id="67a3f-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="67a3f-111">EXAMPLES</span></span>

### <span data-ttu-id="67a3f-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="67a3f-112">Example 1</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Tag $updatedTag -Desired $updatedDesired -Partial
```

<span data-ttu-id="67a3f-113">Zwraca zaktualizowany obiekt urządzenia.</span><span class="sxs-lookup"><span data-stu-id="67a3f-113">Returns the updated device twin object.</span></span>

### <span data-ttu-id="67a3f-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="67a3f-114">Example 2</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Desired $updatedDesired -Partial
```

<span data-ttu-id="67a3f-115">Zwraca obiekt urządzenia o zaktualizowanych właściwościach.</span><span class="sxs-lookup"><span data-stu-id="67a3f-115">Returns the device twin object with updated desired properties.</span></span>

### <span data-ttu-id="67a3f-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="67a3f-116">Example 3</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Tag $updatedTag -Partial
```

<span data-ttu-id="67a3f-117">Zwraca obiekt urządzenia ze zaktualizowaną właściwością tagów.</span><span class="sxs-lookup"><span data-stu-id="67a3f-117">Returns the device twin object with updated tags property.</span></span>

### <span data-ttu-id="67a3f-118">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="67a3f-118">Example 4</span></span>
```powershell
PS C:\> $updatedTag = @{}
PS C:\> $updatedTag.add("key0","value0")
PS C:\> $updatedDesired =@{}
PS C:\> $updatedDesired.add("desiredkey","desiredvalue")
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Tag $updatedTag -Desired $updatedDesired
```

<span data-ttu-id="67a3f-119">Zwraca zastąpiony obiekt urządzenia.</span><span class="sxs-lookup"><span data-stu-id="67a3f-119">Returns the replaced device twin object.</span></span>

## <span data-ttu-id="67a3f-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="67a3f-120">PARAMETERS</span></span>

### <span data-ttu-id="67a3f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67a3f-121">-DefaultProfile</span></span>
<span data-ttu-id="67a3f-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="67a3f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67a3f-123">— Żądane</span><span class="sxs-lookup"><span data-stu-id="67a3f-123">-Desired</span></span>
<span data-ttu-id="67a3f-124">Dodaj lub zaktualizuj żądaną właściwość w urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="67a3f-124">Add or update the desired property in a device twin.</span></span>

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

### <span data-ttu-id="67a3f-125">— DeviceId</span><span class="sxs-lookup"><span data-stu-id="67a3f-125">-DeviceId</span></span>
<span data-ttu-id="67a3f-126">Identyfikator urządzenia docelowego.</span><span class="sxs-lookup"><span data-stu-id="67a3f-126">Target Device Id.</span></span>

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

### <span data-ttu-id="67a3f-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="67a3f-127">-InputObject</span></span>
<span data-ttu-id="67a3f-128">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="67a3f-128">IotHub object</span></span>

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

### <span data-ttu-id="67a3f-129">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="67a3f-129">-IotHubName</span></span>
<span data-ttu-id="67a3f-130">Nazwa Centrum Iot</span><span class="sxs-lookup"><span data-stu-id="67a3f-130">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="67a3f-131">— Częściowe</span><span class="sxs-lookup"><span data-stu-id="67a3f-131">-Partial</span></span>
<span data-ttu-id="67a3f-132">Umożliwia tylko częściową aktualizację tagów i żądanych właściwości urządzenia.</span><span class="sxs-lookup"><span data-stu-id="67a3f-132">Allows to only partially update the tags and desired properties of a device twin.</span></span>

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

### <span data-ttu-id="67a3f-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67a3f-133">-ResourceGroupName</span></span>
<span data-ttu-id="67a3f-134">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="67a3f-134">Name of the Resource Group</span></span>

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

### <span data-ttu-id="67a3f-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="67a3f-135">-ResourceId</span></span>
<span data-ttu-id="67a3f-136">Identyfikator zasobu w aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="67a3f-136">IotHub Resource Id</span></span>

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

### <span data-ttu-id="67a3f-137">— Tag</span><span class="sxs-lookup"><span data-stu-id="67a3f-137">-Tag</span></span>
<span data-ttu-id="67a3f-138">Dodaj lub zaktualizuj właściwość tagów w urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="67a3f-138">Add or update the tags property in a device twin.</span></span>

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

### <span data-ttu-id="67a3f-139">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="67a3f-139">-Confirm</span></span>
<span data-ttu-id="67a3f-140">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="67a3f-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67a3f-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67a3f-141">-WhatIf</span></span>
<span data-ttu-id="67a3f-142">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67a3f-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67a3f-143">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="67a3f-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67a3f-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67a3f-144">CommonParameters</span></span>
<span data-ttu-id="67a3f-145">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67a3f-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67a3f-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67a3f-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67a3f-147">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="67a3f-147">INPUTS</span></span>

### <span data-ttu-id="67a3f-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="67a3f-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="67a3f-149">System.String</span><span class="sxs-lookup"><span data-stu-id="67a3f-149">System.String</span></span>

## <span data-ttu-id="67a3f-150">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="67a3f-150">OUTPUTS</span></span>

### <span data-ttu-id="67a3f-151">System.String</span><span class="sxs-lookup"><span data-stu-id="67a3f-151">System.String</span></span>

## <span data-ttu-id="67a3f-152">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="67a3f-152">NOTES</span></span>

## <span data-ttu-id="67a3f-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="67a3f-153">RELATED LINKS</span></span>
