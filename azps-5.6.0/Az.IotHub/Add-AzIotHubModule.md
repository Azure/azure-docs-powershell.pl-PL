---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/add-aziothubmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubModule.md
ms.openlocfilehash: 09a4201d8add325c068358615a48a86c5e60911a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997823"
---
# <span data-ttu-id="cd382-101">Add-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="cd382-101">Add-AzIotHubModule</span></span>

## <span data-ttu-id="cd382-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd382-102">SYNOPSIS</span></span>
<span data-ttu-id="cd382-103">Utwórz moduł na urządzeniu docelowym IoT w Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="cd382-103">Create a module on a target IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="cd382-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="cd382-104">SYNTAX</span></span>

### <span data-ttu-id="cd382-105">Zestaw zasobów (domyślny)</span><span class="sxs-lookup"><span data-stu-id="cd382-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubModule [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String> [-ModuleId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cd382-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="cd382-106">InputObjectSet</span></span>
```
Add-AzIotHubModule [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cd382-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="cd382-107">ResourceIdSet</span></span>
```
Add-AzIotHubModule [-ResourceId] <String> [-DeviceId] <String> [-ModuleId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cd382-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="cd382-108">DESCRIPTION</span></span>
<span data-ttu-id="cd382-109">Utwórz moduł na urządzeniu docelowym IoT o innym typie autoryzacji w Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="cd382-109">Create a module on a target IoT device with different authorization type in an IoT Hub.</span></span>

## <span data-ttu-id="cd382-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="cd382-110">EXAMPLES</span></span>

### <span data-ttu-id="cd382-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cd382-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIoTHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -AuthMethod shared_private_key

ModuleId                   : myModule1
DeviceId                   : myDevice1
GenerationId               : 637148941292917073
ETag                       : "NzIyMDI4MTk3"
LastActivityTime           : 1/1/0001 12:00:00 AM
ConnectionState            : Disconnected
ConnectionStateUpdatedTime : 1/1/0001 12:00:00 AM
CloudToDeviceMessageCount  : 0
Authentication             : Sas
ManagedBy                  : 
```

<span data-ttu-id="cd382-112">Utwórz moduł na urządzeniu docelowym IoT z domyślną autoryzacją (udostępniony klucz prywatny).</span><span class="sxs-lookup"><span data-stu-id="cd382-112">Create a module on a target IoT device with default authorization (shared private key).</span></span>

## <span data-ttu-id="cd382-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cd382-113">PARAMETERS</span></span>

### <span data-ttu-id="cd382-114">-AuthMethod</span><span class="sxs-lookup"><span data-stu-id="cd382-114">-AuthMethod</span></span>
<span data-ttu-id="cd382-115">Typ podmiotu autoryzacji, za pomocą który ma zostać utworzony.</span><span class="sxs-lookup"><span data-stu-id="cd382-115">The authorization type an entity is to be created with.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceAuthType
Parameter Sets: (All)
Aliases:
Accepted values: shared_private_key, x509_thumbprint, x509_ca

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd382-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd382-116">-DefaultProfile</span></span>
<span data-ttu-id="cd382-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="cd382-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd382-118">— DeviceId</span><span class="sxs-lookup"><span data-stu-id="cd382-118">-DeviceId</span></span>
<span data-ttu-id="cd382-119">Identyfikator urządzenia docelowego.</span><span class="sxs-lookup"><span data-stu-id="cd382-119">Target Device Id.</span></span>

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

### <span data-ttu-id="cd382-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cd382-120">-InputObject</span></span>
<span data-ttu-id="cd382-121">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="cd382-121">IotHub object</span></span>

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

### <span data-ttu-id="cd382-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="cd382-122">-IotHubName</span></span>
<span data-ttu-id="cd382-123">Nazwa Centrum Iot</span><span class="sxs-lookup"><span data-stu-id="cd382-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="cd382-124">- ModuleId</span><span class="sxs-lookup"><span data-stu-id="cd382-124">-ModuleId</span></span>
<span data-ttu-id="cd382-125">Identyfikator modułu docelowego.</span><span class="sxs-lookup"><span data-stu-id="cd382-125">Target Module Id.</span></span>

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

### <span data-ttu-id="cd382-126">-PrimaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="cd382-126">-PrimaryThumbprint</span></span>
<span data-ttu-id="cd382-127">Jawny własny podpis usb certyfikatu do użycia jako klucz podstawowy.</span><span class="sxs-lookup"><span data-stu-id="cd382-127">Explicit self-signed certificate thumbprint to use for primary key.</span></span>

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

### <span data-ttu-id="cd382-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd382-128">-ResourceGroupName</span></span>
<span data-ttu-id="cd382-129">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="cd382-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="cd382-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd382-130">-ResourceId</span></span>
<span data-ttu-id="cd382-131">Identyfikator zasobu w aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="cd382-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="cd382-132">-SecondaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="cd382-132">-SecondaryThumbprint</span></span>
<span data-ttu-id="cd382-133">Jawny samopodpisywanego certyfikatu thumbprint do użycia w przypadku klucza pomocniczego.</span><span class="sxs-lookup"><span data-stu-id="cd382-133">Explicit self-signed certificate thumbprint to use for secondary key.</span></span>

```yaml
Type:System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd382-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cd382-134">-Confirm</span></span>
<span data-ttu-id="cd382-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="cd382-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd382-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd382-136">-WhatIf</span></span>
<span data-ttu-id="cd382-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd382-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd382-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="cd382-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd382-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd382-139">CommonParameters</span></span>
<span data-ttu-id="cd382-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd382-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd382-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd382-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd382-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cd382-142">INPUTS</span></span>

### <span data-ttu-id="cd382-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="cd382-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="cd382-144">System.String</span><span class="sxs-lookup"><span data-stu-id="cd382-144">System.String</span></span>

## <span data-ttu-id="cd382-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cd382-145">OUTPUTS</span></span>

### <span data-ttu-id="cd382-146">Microsoft.Azure.Commands.Management.iotHub.Models.PSModule</span><span class="sxs-lookup"><span data-stu-id="cd382-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSModule</span></span>

## <span data-ttu-id="cd382-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="cd382-147">NOTES</span></span>

## <span data-ttu-id="cd382-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cd382-148">RELATED LINKS</span></span>