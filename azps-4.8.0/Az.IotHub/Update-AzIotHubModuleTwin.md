---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/update-aziothubmoduletwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubModuleTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubModuleTwin.md
ms.openlocfilehash: fb2b984453f87422d7a5b9ec5d5178ca6b6c55d5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062703"
---
# <span data-ttu-id="dc79e-101">Update-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="dc79e-101">Update-AzIotHubModuleTwin</span></span>

## <span data-ttu-id="dc79e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dc79e-102">SYNOPSIS</span></span>
<span data-ttu-id="dc79e-103">Aktualizuje znaczniki i odpowiednie właściwości modułu urządzenia IoT — sznurek.</span><span class="sxs-lookup"><span data-stu-id="dc79e-103">Updates tags and desired properties of an IoT device module twin.</span></span>

## <span data-ttu-id="dc79e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dc79e-104">SYNTAX</span></span>

### <span data-ttu-id="dc79e-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="dc79e-105">ResourceSet (Default)</span></span>
```
Update-AzIotHubModuleTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 -ModuleId <String> [-Tag <Hashtable>] [-Desired <Hashtable>] [-Partial]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc79e-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="dc79e-106">InputObjectSet</span></span>
```
Update-AzIotHubModuleTwin [-InputObject] <PSIotHub> [-DeviceId] <String> -ModuleId <String> [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dc79e-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="dc79e-107">ResourceIdSet</span></span>
```
Update-AzIotHubModuleTwin [-ResourceId] <String> [-DeviceId] <String> -ModuleId <String> [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dc79e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="dc79e-108">DESCRIPTION</span></span>
<span data-ttu-id="dc79e-109">Umożliwia aktualizowanie lub zamienianie sznurka urządzenia.</span><span class="sxs-lookup"><span data-stu-id="dc79e-109">Updates or replaces a device twin.</span></span> <span data-ttu-id="dc79e-110"> https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-module-twinsAby uzyskać więcej informacji, zobacz.</span><span class="sxs-lookup"><span data-stu-id="dc79e-110">See https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-module-twins for more information.</span></span>

## <span data-ttu-id="dc79e-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dc79e-111">EXAMPLES</span></span>

### <span data-ttu-id="dc79e-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="dc79e-112">Example 1</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Tag $updatedTag -Desired $updatedDesired -Partial
```

<span data-ttu-id="dc79e-113">Zwraca obiekt z zaktualizowanym modułem sznurka urządzenia.</span><span class="sxs-lookup"><span data-stu-id="dc79e-113">Returns the updated device module twin object.</span></span>

### <span data-ttu-id="dc79e-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="dc79e-114">Example 2</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Desired $updatedDesired -Partial
```

<span data-ttu-id="dc79e-115">Zwraca obiekt sznura modułowego urządzenia ze zaktualizowanymi pożądanymi właściwościami.</span><span class="sxs-lookup"><span data-stu-id="dc79e-115">Returns the device module twin object with updated desired properties.</span></span>

### <span data-ttu-id="dc79e-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="dc79e-116">Example 3</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Tag $updatedTag -Partial
```

<span data-ttu-id="dc79e-117">Zwraca obiekt typu sznurek modułu urządzenia z zaktualizowaną właściwością Tagi.</span><span class="sxs-lookup"><span data-stu-id="dc79e-117">Returns the device module twin object with updated tags property.</span></span>

### <span data-ttu-id="dc79e-118">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="dc79e-118">Example 4</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Tag $updatedTag -Desired $updatedDesired
```

<span data-ttu-id="dc79e-119">Zwraca obiekt z zamienionym modułem sznurka urządzenia.</span><span class="sxs-lookup"><span data-stu-id="dc79e-119">Returns the replaced device module twin object.</span></span>

## <span data-ttu-id="dc79e-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dc79e-120">PARAMETERS</span></span>

### <span data-ttu-id="dc79e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc79e-121">-DefaultProfile</span></span>
<span data-ttu-id="dc79e-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="dc79e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc79e-123">— Wymagane</span><span class="sxs-lookup"><span data-stu-id="dc79e-123">-Desired</span></span>
<span data-ttu-id="dc79e-124">Dodaj lub zaktualizuj odpowiednią właściwość w module sznurek.</span><span class="sxs-lookup"><span data-stu-id="dc79e-124">Add or update the desired property in a module twin.</span></span>

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

### <span data-ttu-id="dc79e-125">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="dc79e-125">-DeviceId</span></span>
<span data-ttu-id="dc79e-126">Identyfikator urządzenia docelowego.</span><span class="sxs-lookup"><span data-stu-id="dc79e-126">Target Device Id.</span></span>

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

### <span data-ttu-id="dc79e-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="dc79e-127">-InputObject</span></span>
<span data-ttu-id="dc79e-128">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="dc79e-128">IotHub object</span></span>

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

### <span data-ttu-id="dc79e-129">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="dc79e-129">-IotHubName</span></span>
<span data-ttu-id="dc79e-130">Nazwa Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="dc79e-130">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="dc79e-131">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="dc79e-131">-ModuleId</span></span>
<span data-ttu-id="dc79e-132">Identyfikator modułu docelowego.</span><span class="sxs-lookup"><span data-stu-id="dc79e-132">Target Module Id.</span></span>

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

### <span data-ttu-id="dc79e-133">-Częściowa</span><span class="sxs-lookup"><span data-stu-id="dc79e-133">-Partial</span></span>
<span data-ttu-id="dc79e-134">Umożliwia tylko częściowe zaktualizowanie znaczników i pożądanych właściwości modułu sznurek.</span><span class="sxs-lookup"><span data-stu-id="dc79e-134">Allows to only partially update the tags and desired properties of a module twin.</span></span>

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

### <span data-ttu-id="dc79e-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc79e-135">-ResourceGroupName</span></span>
<span data-ttu-id="dc79e-136">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="dc79e-136">Name of the Resource Group</span></span>

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

### <span data-ttu-id="dc79e-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dc79e-137">-ResourceId</span></span>
<span data-ttu-id="dc79e-138">Identyfikator zasobu IotHub</span><span class="sxs-lookup"><span data-stu-id="dc79e-138">IotHub Resource Id</span></span>

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

### <span data-ttu-id="dc79e-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="dc79e-139">-Tag</span></span>
<span data-ttu-id="dc79e-140">Dodaj lub zaktualizuj właściwość znaczniki w module sznurek.</span><span class="sxs-lookup"><span data-stu-id="dc79e-140">Add or update the tags property in a module twin.</span></span>

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

### <span data-ttu-id="dc79e-141">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dc79e-141">-Confirm</span></span>
<span data-ttu-id="dc79e-142">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc79e-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc79e-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc79e-143">-WhatIf</span></span>
<span data-ttu-id="dc79e-144">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc79e-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc79e-145">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="dc79e-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc79e-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc79e-146">CommonParameters</span></span>
<span data-ttu-id="dc79e-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc79e-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc79e-148">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc79e-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc79e-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dc79e-149">INPUTS</span></span>

### <span data-ttu-id="dc79e-150">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="dc79e-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="dc79e-151">System. String</span><span class="sxs-lookup"><span data-stu-id="dc79e-151">System.String</span></span>

## <span data-ttu-id="dc79e-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dc79e-152">OUTPUTS</span></span>

### <span data-ttu-id="dc79e-153">Microsoft. Azure. Commands. Management. IotHub. models. PSModuleTwin</span><span class="sxs-lookup"><span data-stu-id="dc79e-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleTwin</span></span>

## <span data-ttu-id="dc79e-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dc79e-154">NOTES</span></span>

## <span data-ttu-id="dc79e-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dc79e-155">RELATED LINKS</span></span>
