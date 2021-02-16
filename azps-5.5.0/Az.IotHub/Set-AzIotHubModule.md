---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubModule.md
ms.openlocfilehash: c88ee9af5d03b50ed80bf677ccff6e7236668756
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185618"
---
# <span data-ttu-id="463dd-101">Set-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="463dd-101">Set-AzIotHubModule</span></span>

## <span data-ttu-id="463dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="463dd-102">SYNOPSIS</span></span>
<span data-ttu-id="463dd-103">Aktualizowanie modułu na urządzeniu docelowym IoT w centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="463dd-103">Update a module on a target IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="463dd-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="463dd-104">SYNTAX</span></span>

### <span data-ttu-id="463dd-105">Zestaw zasobów (domyślny)</span><span class="sxs-lookup"><span data-stu-id="463dd-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubModule [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String> [-ModuleId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="463dd-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="463dd-106">InputObjectSet</span></span>
```
Set-AzIotHubModule [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="463dd-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="463dd-107">ResourceIdSet</span></span>
```
Set-AzIotHubModule [-ResourceId] <String> [-DeviceId] <String> [-ModuleId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="463dd-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="463dd-108">DESCRIPTION</span></span>
<span data-ttu-id="463dd-109">Aktualizowanie modułu na urządzeniu docelowym IoT w Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="463dd-109">Update a module on a target IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="463dd-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="463dd-110">EXAMPLES</span></span>

### <span data-ttu-id="463dd-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="463dd-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -AuthMethod "shared_private_key"

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

<span data-ttu-id="463dd-112">Aktualizowanie typu autoryzacji modułu urządzenia Iot.</span><span class="sxs-lookup"><span data-stu-id="463dd-112">Update authorization type of an Iot device module.</span></span>

## <span data-ttu-id="463dd-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="463dd-113">PARAMETERS</span></span>

### <span data-ttu-id="463dd-114">-AuthMethod</span><span class="sxs-lookup"><span data-stu-id="463dd-114">-AuthMethod</span></span>
<span data-ttu-id="463dd-115">Typ podmiotu autoryzacji, za pomocą który ma zostać utworzony.</span><span class="sxs-lookup"><span data-stu-id="463dd-115">The authorization type an entity is to be created with.</span></span>

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

### <span data-ttu-id="463dd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="463dd-116">-DefaultProfile</span></span>
<span data-ttu-id="463dd-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="463dd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="463dd-118">— DeviceId</span><span class="sxs-lookup"><span data-stu-id="463dd-118">-DeviceId</span></span>
<span data-ttu-id="463dd-119">Identyfikator urządzenia docelowego.</span><span class="sxs-lookup"><span data-stu-id="463dd-119">Target Device Id.</span></span>

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

### <span data-ttu-id="463dd-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="463dd-120">-InputObject</span></span>
<span data-ttu-id="463dd-121">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="463dd-121">IotHub object</span></span>

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

### <span data-ttu-id="463dd-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="463dd-122">-IotHubName</span></span>
<span data-ttu-id="463dd-123">Nazwa Centrum Iot</span><span class="sxs-lookup"><span data-stu-id="463dd-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="463dd-124">- ModuleId</span><span class="sxs-lookup"><span data-stu-id="463dd-124">-ModuleId</span></span>
<span data-ttu-id="463dd-125">Identyfikator modułu docelowego.</span><span class="sxs-lookup"><span data-stu-id="463dd-125">Target Module Id.</span></span>

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

### <span data-ttu-id="463dd-126">-PrimaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="463dd-126">-PrimaryThumbprint</span></span>
<span data-ttu-id="463dd-127">Jawny własny podpis usb certyfikatu do użycia jako klucz podstawowy.</span><span class="sxs-lookup"><span data-stu-id="463dd-127">Explicit self-signed certificate thumbprint to use for primary key.</span></span>

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

### <span data-ttu-id="463dd-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="463dd-128">-ResourceGroupName</span></span>
<span data-ttu-id="463dd-129">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="463dd-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="463dd-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="463dd-130">-ResourceId</span></span>
<span data-ttu-id="463dd-131">Identyfikator zasobu w aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="463dd-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="463dd-132">- SecondaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="463dd-132">-SecondaryThumbprint</span></span>
<span data-ttu-id="463dd-133">Jawne samopodpisywane wydrukowanie certyfikatu do użycia na kluczu pomocniczym.</span><span class="sxs-lookup"><span data-stu-id="463dd-133">Explicit self-signed certificate thumbprint to use for secondary key.</span></span>

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

### <span data-ttu-id="463dd-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="463dd-134">-Confirm</span></span>
<span data-ttu-id="463dd-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="463dd-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="463dd-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="463dd-136">-WhatIf</span></span>
<span data-ttu-id="463dd-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="463dd-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="463dd-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="463dd-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="463dd-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="463dd-139">CommonParameters</span></span>
<span data-ttu-id="463dd-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="463dd-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="463dd-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="463dd-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="463dd-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="463dd-142">INPUTS</span></span>

### <span data-ttu-id="463dd-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="463dd-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="463dd-144">System.String</span><span class="sxs-lookup"><span data-stu-id="463dd-144">System.String</span></span>

## <span data-ttu-id="463dd-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="463dd-145">OUTPUTS</span></span>

### <span data-ttu-id="463dd-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSModule</span><span class="sxs-lookup"><span data-stu-id="463dd-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSModule</span></span>

## <span data-ttu-id="463dd-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="463dd-147">NOTES</span></span>

## <span data-ttu-id="463dd-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="463dd-148">RELATED LINKS</span></span>