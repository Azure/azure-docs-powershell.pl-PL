---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubmodulemethod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubModuleMethod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubModuleMethod.md
ms.openlocfilehash: e9faa07f4addabcb556819e1d45b63a0dec0f6b3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180571"
---
# <span data-ttu-id="8d311-101">Invoke-AzIotHubModuleMethod</span><span class="sxs-lookup"><span data-stu-id="8d311-101">Invoke-AzIotHubModuleMethod</span></span>

## <span data-ttu-id="8d311-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d311-102">SYNOPSIS</span></span>
<span data-ttu-id="8d311-103">Wywoływanie metody modułu Edge.</span><span class="sxs-lookup"><span data-stu-id="8d311-103">Invoke an Edge module method.</span></span>

## <span data-ttu-id="8d311-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8d311-104">SYNTAX</span></span>

### <span data-ttu-id="8d311-105">ResourceSet (Default)</span><span class="sxs-lookup"><span data-stu-id="8d311-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubModuleMethod [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId] <String> -Name <String> [-Payload <String>] [-ResponseTimeOut <Int32>]
 [-ConnectionTimeOut <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8d311-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="8d311-106">InputObjectSet</span></span>
```
Invoke-AzIotHubModuleMethod [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId] <String> -Name <String>
 [-Payload <String>] [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d311-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="8d311-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubModuleMethod [-ResourceId] <String> [-DeviceId] <String> [-ModuleId] <String> -Name <String>
 [-Payload <String>] [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d311-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="8d311-108">DESCRIPTION</span></span>
<span data-ttu-id="8d311-109">Wywoływanie metody modułu Edge.</span><span class="sxs-lookup"><span data-stu-id="8d311-109">Invoke an Edge module method.</span></span> <span data-ttu-id="8d311-110">Aby https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods uzyskać więcej informacji, zobacz te informacje.</span><span class="sxs-lookup"><span data-stu-id="8d311-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods for more information.</span></span>

## <span data-ttu-id="8d311-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8d311-111">EXAMPLES</span></span>

### <span data-ttu-id="8d311-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8d311-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubModuleMethod -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Name "methodName" -Payload "method-input" -ResponseTimeOut 20 -ConnectionTimeOut 15
```

<span data-ttu-id="8d311-113">Wywoływanie metody modułu Edge.</span><span class="sxs-lookup"><span data-stu-id="8d311-113">Invoke an Edge module method.</span></span>

## <span data-ttu-id="8d311-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8d311-114">PARAMETERS</span></span>

### <span data-ttu-id="8d311-115">- ConnectionTimeOut</span><span class="sxs-lookup"><span data-stu-id="8d311-115">-ConnectionTimeOut</span></span>
<span data-ttu-id="8d311-116">Liczba sekund oczekiwania na pomyślne połączenie.</span><span class="sxs-lookup"><span data-stu-id="8d311-116">Number of seconds to wait until a connection is successfully made.</span></span>
<span data-ttu-id="8d311-117">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="8d311-117">Default is 10.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d311-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d311-118">-DefaultProfile</span></span>
<span data-ttu-id="8d311-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8d311-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d311-120">— DeviceId</span><span class="sxs-lookup"><span data-stu-id="8d311-120">-DeviceId</span></span>
<span data-ttu-id="8d311-121">Identyfikator urządzenia docelowego.</span><span class="sxs-lookup"><span data-stu-id="8d311-121">Target Device Id.</span></span>

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

### <span data-ttu-id="8d311-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8d311-122">-InputObject</span></span>
<span data-ttu-id="8d311-123">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="8d311-123">IotHub object</span></span>

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

### <span data-ttu-id="8d311-124">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="8d311-124">-IotHubName</span></span>
<span data-ttu-id="8d311-125">Nazwa Centrum Iot</span><span class="sxs-lookup"><span data-stu-id="8d311-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="8d311-126">- ModuleId</span><span class="sxs-lookup"><span data-stu-id="8d311-126">-ModuleId</span></span>
<span data-ttu-id="8d311-127">Identyfikator modułu urządzenia docelowego.</span><span class="sxs-lookup"><span data-stu-id="8d311-127">Target device's module id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d311-128">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8d311-128">-Name</span></span>
<span data-ttu-id="8d311-129">Nazwa metody wywoływania w tym module urządzenia.</span><span class="sxs-lookup"><span data-stu-id="8d311-129">The name of the method to invoke on this device module.</span></span>

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

### <span data-ttu-id="8d311-130">— Ładna</span><span class="sxs-lookup"><span data-stu-id="8d311-130">-Payload</span></span>
<span data-ttu-id="8d311-131">Ładowność metody wywoływania w tym module urządzenia.</span><span class="sxs-lookup"><span data-stu-id="8d311-131">The payload for the method to invoke on this device module.</span></span>

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

### <span data-ttu-id="8d311-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d311-132">-ResourceGroupName</span></span>
<span data-ttu-id="8d311-133">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="8d311-133">Name of the Resource Group</span></span>

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

### <span data-ttu-id="8d311-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8d311-134">-ResourceId</span></span>
<span data-ttu-id="8d311-135">Identyfikator zasobu w aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="8d311-135">IotHub Resource Id</span></span>

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

### <span data-ttu-id="8d311-136">- ResponseTimeOut</span><span class="sxs-lookup"><span data-stu-id="8d311-136">-ResponseTimeOut</span></span>
<span data-ttu-id="8d311-137">Liczba sekund oczekiwania na wynik z metody bezpośredniej.</span><span class="sxs-lookup"><span data-stu-id="8d311-137">Number of seconds to wait until a result is received from the direct method.</span></span>
<span data-ttu-id="8d311-138">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="8d311-138">Default is 10.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d311-139">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8d311-139">-Confirm</span></span>
<span data-ttu-id="8d311-140">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8d311-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d311-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d311-141">-WhatIf</span></span>
<span data-ttu-id="8d311-142">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d311-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d311-143">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="8d311-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d311-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d311-144">CommonParameters</span></span>
<span data-ttu-id="8d311-145">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d311-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d311-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d311-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d311-147">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8d311-147">INPUTS</span></span>

### <span data-ttu-id="8d311-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="8d311-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="8d311-149">System.String</span><span class="sxs-lookup"><span data-stu-id="8d311-149">System.String</span></span>

## <span data-ttu-id="8d311-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8d311-150">OUTPUTS</span></span>

### <span data-ttu-id="8d311-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceMethodResult</span><span class="sxs-lookup"><span data-stu-id="8d311-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceMethodResult</span></span>

## <span data-ttu-id="8d311-152">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8d311-152">NOTES</span></span>

## <span data-ttu-id="8d311-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8d311-153">RELATED LINKS</span></span>
