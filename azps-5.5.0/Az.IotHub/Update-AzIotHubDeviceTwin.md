---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/update-aziothubdevicetwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubDeviceTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubDeviceTwin.md
ms.openlocfilehash: 451f809687ea768800f0e9e33ef4c5af9c425150
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185587"
---
# <span data-ttu-id="7ce7b-101">Update-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="7ce7b-101">Update-AzIotHubDeviceTwin</span></span>

## <span data-ttu-id="7ce7b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ce7b-102">SYNOPSIS</span></span>
<span data-ttu-id="7ce7b-103">Aktualizuje tagi i żądane właściwości urządzenia.</span><span class="sxs-lookup"><span data-stu-id="7ce7b-103">Updates tags and desired properties of a device twin.</span></span>

## <span data-ttu-id="7ce7b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7ce7b-104">SYNTAX</span></span>

### <span data-ttu-id="7ce7b-105">ResourceSet (Default)</span><span class="sxs-lookup"><span data-stu-id="7ce7b-105">ResourceSet (Default)</span></span>
```
Update-AzIotHubDeviceTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Tag <Hashtable>] [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ce7b-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7ce7b-106">InputObjectSet</span></span>
```
Update-AzIotHubDeviceTwin [-InputObject] <PSIotHub> [-DeviceId] <String> [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7ce7b-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="7ce7b-107">ResourceIdSet</span></span>
```
Update-AzIotHubDeviceTwin [-ResourceId] <String> [-DeviceId] <String> [-Tag <Hashtable>] [-Desired <Hashtable>]
 [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ce7b-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="7ce7b-108">DESCRIPTION</span></span>
<span data-ttu-id="7ce7b-109">Aktualizuje lub zamienia urządzenie.</span><span class="sxs-lookup"><span data-stu-id="7ce7b-109">Updates or replaces a device twin.</span></span> <span data-ttu-id="7ce7b-110">Aby https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins uzyskać więcej informacji, zobacz.</span><span class="sxs-lookup"><span data-stu-id="7ce7b-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins for more information.</span></span>

## <span data-ttu-id="7ce7b-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7ce7b-111">EXAMPLES</span></span>

### <span data-ttu-id="7ce7b-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7ce7b-112">Example 1</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Tag $updatedTag -Desired $updatedDesired -Partial
```

<span data-ttu-id="7ce7b-113">Zwraca zaktualizowany obiekt urządzenia.</span><span class="sxs-lookup"><span data-stu-id="7ce7b-113">Returns the updated device twin object.</span></span>

### <span data-ttu-id="7ce7b-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="7ce7b-114">Example 2</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Desired $updatedDesired -Partial
```

<span data-ttu-id="7ce7b-115">Zwraca obiekt urządzenia o zaktualizowanych właściwościach.</span><span class="sxs-lookup"><span data-stu-id="7ce7b-115">Returns the device twin object with updated desired properties.</span></span>

### <span data-ttu-id="7ce7b-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="7ce7b-116">Example 3</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Tag $updatedTag -Partial
```

<span data-ttu-id="7ce7b-117">Zwraca obiekt urządzenia ze zaktualizowaną właściwością tagów.</span><span class="sxs-lookup"><span data-stu-id="7ce7b-117">Returns the device twin object with updated tags property.</span></span>

### <span data-ttu-id="7ce7b-118">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="7ce7b-118">Example 4</span></span>
```powershell
PS C:\> $updatedTag = @{}
PS C:\> $updatedTag.add("key0","value0")
PS C:\> $updatedDesired =@{}
PS C:\> $updatedDesired.add("desiredkey","desiredvalue")
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Tag $updatedTag -Desired $updatedDesired
```

<span data-ttu-id="7ce7b-119">Zwraca zastąpiony obiekt urządzenia.</span><span class="sxs-lookup"><span data-stu-id="7ce7b-119">Returns the replaced device twin object.</span></span>

## <span data-ttu-id="7ce7b-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7ce7b-120">PARAMETERS</span></span>

### <span data-ttu-id="7ce7b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ce7b-121">-DefaultProfile</span></span>
<span data-ttu-id="7ce7b-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7ce7b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ce7b-123">— Żądane</span><span class="sxs-lookup"><span data-stu-id="7ce7b-123">-Desired</span></span>
<span data-ttu-id="7ce7b-124">Dodaj lub zaktualizuj żądaną właściwość w urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="7ce7b-124">Add or update the desired property in a device twin.</span></span>

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

### <span data-ttu-id="7ce7b-125">— DeviceId</span><span class="sxs-lookup"><span data-stu-id="7ce7b-125">-DeviceId</span></span>
<span data-ttu-id="7ce7b-126">Identyfikator urządzenia docelowego.</span><span class="sxs-lookup"><span data-stu-id="7ce7b-126">Target Device Id.</span></span>

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

### <span data-ttu-id="7ce7b-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7ce7b-127">-InputObject</span></span>
<span data-ttu-id="7ce7b-128">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="7ce7b-128">IotHub object</span></span>

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

### <span data-ttu-id="7ce7b-129">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="7ce7b-129">-IotHubName</span></span>
<span data-ttu-id="7ce7b-130">Nazwa Centrum Iot</span><span class="sxs-lookup"><span data-stu-id="7ce7b-130">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="7ce7b-131">— Częściowe</span><span class="sxs-lookup"><span data-stu-id="7ce7b-131">-Partial</span></span>
<span data-ttu-id="7ce7b-132">Umożliwia tylko częściową aktualizację tagów i żądanych właściwości urządzenia.</span><span class="sxs-lookup"><span data-stu-id="7ce7b-132">Allows to only partially update the tags and desired properties of a device twin.</span></span>

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

### <span data-ttu-id="7ce7b-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ce7b-133">-ResourceGroupName</span></span>
<span data-ttu-id="7ce7b-134">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="7ce7b-134">Name of the Resource Group</span></span>

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

### <span data-ttu-id="7ce7b-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7ce7b-135">-ResourceId</span></span>
<span data-ttu-id="7ce7b-136">Identyfikator zasobu w aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="7ce7b-136">IotHub Resource Id</span></span>

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

### <span data-ttu-id="7ce7b-137">— Tag</span><span class="sxs-lookup"><span data-stu-id="7ce7b-137">-Tag</span></span>
<span data-ttu-id="7ce7b-138">Dodaj lub zaktualizuj właściwość tagów w urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="7ce7b-138">Add or update the tags property in a device twin.</span></span>

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

### <span data-ttu-id="7ce7b-139">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7ce7b-139">-Confirm</span></span>
<span data-ttu-id="7ce7b-140">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7ce7b-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ce7b-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ce7b-141">-WhatIf</span></span>
<span data-ttu-id="7ce7b-142">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ce7b-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ce7b-143">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="7ce7b-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ce7b-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ce7b-144">CommonParameters</span></span>
<span data-ttu-id="7ce7b-145">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ce7b-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ce7b-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ce7b-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ce7b-147">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7ce7b-147">INPUTS</span></span>

### <span data-ttu-id="7ce7b-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="7ce7b-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="7ce7b-149">System.String</span><span class="sxs-lookup"><span data-stu-id="7ce7b-149">System.String</span></span>

## <span data-ttu-id="7ce7b-150">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7ce7b-150">OUTPUTS</span></span>

### <span data-ttu-id="7ce7b-151">System.String</span><span class="sxs-lookup"><span data-stu-id="7ce7b-151">System.String</span></span>

## <span data-ttu-id="7ce7b-152">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7ce7b-152">NOTES</span></span>

## <span data-ttu-id="7ce7b-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7ce7b-153">RELATED LINKS</span></span>
