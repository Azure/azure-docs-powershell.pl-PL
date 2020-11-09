---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/update-aziothubdevicetwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubDeviceTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubDeviceTwin.md
ms.openlocfilehash: 16c3ab31959268aa998d50290180d4d8b3231ccf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94304657"
---
# <span data-ttu-id="d40bb-101">Update-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="d40bb-101">Update-AzIotHubDeviceTwin</span></span>

## <span data-ttu-id="d40bb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d40bb-102">SYNOPSIS</span></span>
<span data-ttu-id="d40bb-103">Aktualizuje znaczniki i wymagane właściwości urządzenia z sznurem.</span><span class="sxs-lookup"><span data-stu-id="d40bb-103">Updates tags and desired properties of a device twin.</span></span>

## <span data-ttu-id="d40bb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d40bb-104">SYNTAX</span></span>

### <span data-ttu-id="d40bb-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d40bb-105">ResourceSet (Default)</span></span>
```
Update-AzIotHubDeviceTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Tag <Hashtable>] [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d40bb-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d40bb-106">InputObjectSet</span></span>
```
Update-AzIotHubDeviceTwin [-InputObject] <PSIotHub> [-DeviceId] <String> [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d40bb-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d40bb-107">ResourceIdSet</span></span>
```
Update-AzIotHubDeviceTwin [-ResourceId] <String> [-DeviceId] <String> [-Tag <Hashtable>] [-Desired <Hashtable>]
 [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d40bb-108">Opis</span><span class="sxs-lookup"><span data-stu-id="d40bb-108">DESCRIPTION</span></span>
<span data-ttu-id="d40bb-109">Umożliwia aktualizowanie lub zamienianie sznurka urządzenia.</span><span class="sxs-lookup"><span data-stu-id="d40bb-109">Updates or replaces a device twin.</span></span> <span data-ttu-id="d40bb-110"> https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twinsAby uzyskać więcej informacji, zobacz.</span><span class="sxs-lookup"><span data-stu-id="d40bb-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins for more information.</span></span>

## <span data-ttu-id="d40bb-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d40bb-111">EXAMPLES</span></span>

### <span data-ttu-id="d40bb-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d40bb-112">Example 1</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Tag $updatedTag -Desired $updatedDesired -Partial
```

<span data-ttu-id="d40bb-113">Zwraca zaktualizowany obiekt sznurka urządzenia.</span><span class="sxs-lookup"><span data-stu-id="d40bb-113">Returns the updated device twin object.</span></span>

### <span data-ttu-id="d40bb-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="d40bb-114">Example 2</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Desired $updatedDesired -Partial
```

<span data-ttu-id="d40bb-115">Zwraca obiekt sznurka urządzenia ze zaktualizowanymi pożądanymi właściwościami.</span><span class="sxs-lookup"><span data-stu-id="d40bb-115">Returns the device twin object with updated desired properties.</span></span>

### <span data-ttu-id="d40bb-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="d40bb-116">Example 3</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Tag $updatedTag -Partial
```

<span data-ttu-id="d40bb-117">Zwraca obiekt sznurka urządzenia z zaktualizowaną właściwością Tagi.</span><span class="sxs-lookup"><span data-stu-id="d40bb-117">Returns the device twin object with updated tags property.</span></span>

### <span data-ttu-id="d40bb-118">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="d40bb-118">Example 4</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Tag $updatedTag -Desired $updatedDesired
```

<span data-ttu-id="d40bb-119">Zwraca zamieniony obiekt sznurka na urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="d40bb-119">Returns the replaced device twin object.</span></span>

## <span data-ttu-id="d40bb-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d40bb-120">PARAMETERS</span></span>

### <span data-ttu-id="d40bb-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d40bb-121">-DefaultProfile</span></span>
<span data-ttu-id="d40bb-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d40bb-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d40bb-123">— Wymagane</span><span class="sxs-lookup"><span data-stu-id="d40bb-123">-Desired</span></span>
<span data-ttu-id="d40bb-124">Dodaj lub zaktualizuj odpowiednią właściwość w sznurze urządzenia.</span><span class="sxs-lookup"><span data-stu-id="d40bb-124">Add or update the desired property in a device twin.</span></span>

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

### <span data-ttu-id="d40bb-125">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="d40bb-125">-DeviceId</span></span>
<span data-ttu-id="d40bb-126">Identyfikator urządzenia docelowego.</span><span class="sxs-lookup"><span data-stu-id="d40bb-126">Target Device Id.</span></span>

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

### <span data-ttu-id="d40bb-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d40bb-127">-InputObject</span></span>
<span data-ttu-id="d40bb-128">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="d40bb-128">IotHub object</span></span>

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

### <span data-ttu-id="d40bb-129">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="d40bb-129">-IotHubName</span></span>
<span data-ttu-id="d40bb-130">Nazwa Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="d40bb-130">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="d40bb-131">-Częściowa</span><span class="sxs-lookup"><span data-stu-id="d40bb-131">-Partial</span></span>
<span data-ttu-id="d40bb-132">Umożliwia tylko częściowe zaktualizowanie tagów i żądanych właściwości urządzenia z sznurem.</span><span class="sxs-lookup"><span data-stu-id="d40bb-132">Allows to only partially update the tags and desired properties of a device twin.</span></span>

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

### <span data-ttu-id="d40bb-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d40bb-133">-ResourceGroupName</span></span>
<span data-ttu-id="d40bb-134">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="d40bb-134">Name of the Resource Group</span></span>

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

### <span data-ttu-id="d40bb-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d40bb-135">-ResourceId</span></span>
<span data-ttu-id="d40bb-136">Identyfikator zasobu IotHub</span><span class="sxs-lookup"><span data-stu-id="d40bb-136">IotHub Resource Id</span></span>

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

### <span data-ttu-id="d40bb-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="d40bb-137">-Tag</span></span>
<span data-ttu-id="d40bb-138">Dodaj lub zaktualizuj właściwość znaczniki w sznurze urządzenia.</span><span class="sxs-lookup"><span data-stu-id="d40bb-138">Add or update the tags property in a device twin.</span></span>

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

### <span data-ttu-id="d40bb-139">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d40bb-139">-Confirm</span></span>
<span data-ttu-id="d40bb-140">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d40bb-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d40bb-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d40bb-141">-WhatIf</span></span>
<span data-ttu-id="d40bb-142">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d40bb-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d40bb-143">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d40bb-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d40bb-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d40bb-144">CommonParameters</span></span>
<span data-ttu-id="d40bb-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d40bb-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d40bb-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d40bb-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d40bb-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d40bb-147">INPUTS</span></span>

### <span data-ttu-id="d40bb-148">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="d40bb-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="d40bb-149">System. String</span><span class="sxs-lookup"><span data-stu-id="d40bb-149">System.String</span></span>

## <span data-ttu-id="d40bb-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d40bb-150">OUTPUTS</span></span>

### <span data-ttu-id="d40bb-151">System. String</span><span class="sxs-lookup"><span data-stu-id="d40bb-151">System.String</span></span>

## <span data-ttu-id="d40bb-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d40bb-152">NOTES</span></span>

## <span data-ttu-id="d40bb-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d40bb-153">RELATED LINKS</span></span>
