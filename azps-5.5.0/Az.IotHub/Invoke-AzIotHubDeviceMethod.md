---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubdevicemethod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubDeviceMethod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubDeviceMethod.md
ms.openlocfilehash: 78247b26d2f8e6618d3999389efa509e3f8854b9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192419"
---
# <span data-ttu-id="fb7d4-101">Invoke-AzIotHubDeviceMethod</span><span class="sxs-lookup"><span data-stu-id="fb7d4-101">Invoke-AzIotHubDeviceMethod</span></span>

## <span data-ttu-id="fb7d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb7d4-102">SYNOPSIS</span></span>
<span data-ttu-id="fb7d4-103">Wywoływanie metody bezpośredniej na urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="fb7d4-103">Invoke a direct method on a device.</span></span>

## <span data-ttu-id="fb7d4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fb7d4-104">SYNTAX</span></span>

### <span data-ttu-id="fb7d4-105">ResourceSet (Default)</span><span class="sxs-lookup"><span data-stu-id="fb7d4-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubDeviceMethod [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 -Name <String> [-Payload <String>] [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb7d4-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="fb7d4-106">InputObjectSet</span></span>
```
Invoke-AzIotHubDeviceMethod [-InputObject] <PSIotHub> [-DeviceId] <String> -Name <String> [-Payload <String>]
 [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb7d4-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="fb7d4-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubDeviceMethod [-ResourceId] <String> [-DeviceId] <String> -Name <String> [-Payload <String>]
 [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb7d4-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="fb7d4-108">DESCRIPTION</span></span>
<span data-ttu-id="fb7d4-109">Wywoływanie metody bezpośredniej na urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="fb7d4-109">Invoke a direct method on a device.</span></span> <span data-ttu-id="fb7d4-110">Aby https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods uzyskać więcej informacji, zobacz te informacje.</span><span class="sxs-lookup"><span data-stu-id="fb7d4-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods for more information.</span></span>

## <span data-ttu-id="fb7d4-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fb7d4-111">EXAMPLES</span></span>

### <span data-ttu-id="fb7d4-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fb7d4-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubDeviceMethod -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Name "methodName" -ResponseTimeOut 20 -ConnectionTimeOut 15
```

<span data-ttu-id="fb7d4-113">Wywoływanie metody urządzenia.</span><span class="sxs-lookup"><span data-stu-id="fb7d4-113">Invoke a device method.</span></span>

## <span data-ttu-id="fb7d4-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fb7d4-114">PARAMETERS</span></span>

### <span data-ttu-id="fb7d4-115">- ConnectionTimeOut</span><span class="sxs-lookup"><span data-stu-id="fb7d4-115">-ConnectionTimeOut</span></span>
<span data-ttu-id="fb7d4-116">Liczba sekund oczekiwania na pomyślne połączenie.</span><span class="sxs-lookup"><span data-stu-id="fb7d4-116">Number of seconds to wait until a connection is successfully made.</span></span>
<span data-ttu-id="fb7d4-117">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="fb7d4-117">Default is 10.</span></span>

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

### <span data-ttu-id="fb7d4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb7d4-118">-DefaultProfile</span></span>
<span data-ttu-id="fb7d4-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="fb7d4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb7d4-120">— DeviceId</span><span class="sxs-lookup"><span data-stu-id="fb7d4-120">-DeviceId</span></span>
<span data-ttu-id="fb7d4-121">Identyfikator urządzenia docelowego.</span><span class="sxs-lookup"><span data-stu-id="fb7d4-121">Target Device Id.</span></span>

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

### <span data-ttu-id="fb7d4-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fb7d4-122">-InputObject</span></span>
<span data-ttu-id="fb7d4-123">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="fb7d4-123">IotHub object</span></span>

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

### <span data-ttu-id="fb7d4-124">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="fb7d4-124">-IotHubName</span></span>
<span data-ttu-id="fb7d4-125">Nazwa Centrum Iot</span><span class="sxs-lookup"><span data-stu-id="fb7d4-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="fb7d4-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="fb7d4-126">-Name</span></span>
<span data-ttu-id="fb7d4-127">Nazwa metody wywoływania na tym urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="fb7d4-127">The name of the method to invoke on this device.</span></span>

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

### <span data-ttu-id="fb7d4-128">— Ładna</span><span class="sxs-lookup"><span data-stu-id="fb7d4-128">-Payload</span></span>
<span data-ttu-id="fb7d4-129">Ładowność metody wywoływania na tym urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="fb7d4-129">The payload for the method to invoke on this device.</span></span>

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

### <span data-ttu-id="fb7d4-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb7d4-130">-ResourceGroupName</span></span>
<span data-ttu-id="fb7d4-131">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="fb7d4-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="fb7d4-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fb7d4-132">-ResourceId</span></span>
<span data-ttu-id="fb7d4-133">Identyfikator zasobu w aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="fb7d4-133">IotHub Resource Id</span></span>

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

### <span data-ttu-id="fb7d4-134">- ResponseTimeOut</span><span class="sxs-lookup"><span data-stu-id="fb7d4-134">-ResponseTimeOut</span></span>
<span data-ttu-id="fb7d4-135">Liczba sekund oczekiwania na wynik z metody bezpośredniej.</span><span class="sxs-lookup"><span data-stu-id="fb7d4-135">Number of seconds to wait until a result is received from the direct method.</span></span>
<span data-ttu-id="fb7d4-136">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="fb7d4-136">Default is 10.</span></span>

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

### <span data-ttu-id="fb7d4-137">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fb7d4-137">-Confirm</span></span>
<span data-ttu-id="fb7d4-138">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="fb7d4-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb7d4-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb7d4-139">-WhatIf</span></span>
<span data-ttu-id="fb7d4-140">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb7d4-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb7d4-141">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="fb7d4-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb7d4-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb7d4-142">CommonParameters</span></span>
<span data-ttu-id="fb7d4-143">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb7d4-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb7d4-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb7d4-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb7d4-145">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fb7d4-145">INPUTS</span></span>

### <span data-ttu-id="fb7d4-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="fb7d4-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="fb7d4-147">System.String</span><span class="sxs-lookup"><span data-stu-id="fb7d4-147">System.String</span></span>

## <span data-ttu-id="fb7d4-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fb7d4-148">OUTPUTS</span></span>

### <span data-ttu-id="fb7d4-149">Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceMethodResult</span><span class="sxs-lookup"><span data-stu-id="fb7d4-149">Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceMethodResult</span></span>

## <span data-ttu-id="fb7d4-150">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fb7d4-150">NOTES</span></span>

## <span data-ttu-id="fb7d4-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fb7d4-151">RELATED LINKS</span></span>
