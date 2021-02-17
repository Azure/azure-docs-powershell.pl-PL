---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubdistributedtracing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDistributedTracing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDistributedTracing.md
ms.openlocfilehash: 364b54f9e0b7a9112c2ce46f33363a4510c7bb68
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180507"
---
# <span data-ttu-id="84e78-101">Set-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="84e78-101">Set-AzIotHubDistributedTracing</span></span>

## <span data-ttu-id="84e78-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84e78-102">SYNOPSIS</span></span>
<span data-ttu-id="84e78-103">Aktualizowanie opcji śledzenia rozłożonego dla urządzenia.</span><span class="sxs-lookup"><span data-stu-id="84e78-103">Update the distributed tracing options for a device.</span></span>

## <span data-ttu-id="84e78-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="84e78-104">SYNTAX</span></span>

### <span data-ttu-id="84e78-105">ResourceSet (Default)</span><span class="sxs-lookup"><span data-stu-id="84e78-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubDistributedTracing [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-SamplingMode] <PSDistributedTracingSamplingMode> [-SamplingRate <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84e78-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="84e78-106">InputObjectSet</span></span>
```
Set-AzIotHubDistributedTracing [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-SamplingMode] <PSDistributedTracingSamplingMode> [-SamplingRate <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84e78-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="84e78-107">ResourceIdSet</span></span>
```
Set-AzIotHubDistributedTracing [-ResourceId] <String> [-DeviceId] <String>
 [-SamplingMode] <PSDistributedTracingSamplingMode> [-SamplingRate <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84e78-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="84e78-108">DESCRIPTION</span></span>
<span data-ttu-id="84e78-109">Aktualizowanie opcji śledzenia rozłożonego dla urządzenia.</span><span class="sxs-lookup"><span data-stu-id="84e78-109">Update the distributed tracing options for a device.</span></span>

## <span data-ttu-id="84e78-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="84e78-110">EXAMPLES</span></span>

### <span data-ttu-id="84e78-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="84e78-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDistributedTracing -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -SamplingMode Enabled -SamplingRate 22

DeviceId      : mydevice1
Sampling Mode : Enabled
Sampling Rate : 22%
IsSynced      : False
```

<span data-ttu-id="84e78-112">Aktualizowanie opcji śledzenia rozłożonego dla urządzenia.</span><span class="sxs-lookup"><span data-stu-id="84e78-112">Update the distributed tracing options for a device.</span></span>

## <span data-ttu-id="84e78-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="84e78-113">PARAMETERS</span></span>

### <span data-ttu-id="84e78-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84e78-114">-DefaultProfile</span></span>
<span data-ttu-id="84e78-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="84e78-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84e78-116">— DeviceId</span><span class="sxs-lookup"><span data-stu-id="84e78-116">-DeviceId</span></span>
<span data-ttu-id="84e78-117">Identyfikator urządzenia docelowego.</span><span class="sxs-lookup"><span data-stu-id="84e78-117">Target Device Id.</span></span>

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

### <span data-ttu-id="84e78-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="84e78-118">-InputObject</span></span>
<span data-ttu-id="84e78-119">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="84e78-119">IotHub object</span></span>

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

### <span data-ttu-id="84e78-120">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="84e78-120">-IotHubName</span></span>
<span data-ttu-id="84e78-121">Nazwa Centrum Iot</span><span class="sxs-lookup"><span data-stu-id="84e78-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="84e78-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84e78-122">-ResourceGroupName</span></span>
<span data-ttu-id="84e78-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="84e78-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="84e78-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="84e78-124">-ResourceId</span></span>
<span data-ttu-id="84e78-125">Identyfikator zasobu w aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="84e78-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="84e78-126">-SamplingMode</span><span class="sxs-lookup"><span data-stu-id="84e78-126">-SamplingMode</span></span>
<span data-ttu-id="84e78-127">Umożliwia włączenie i wyłączenie próbkowania w celu śledzenia rozłożonego.</span><span class="sxs-lookup"><span data-stu-id="84e78-127">Turns sampling for distributed tracing enable and disable.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSDistributedTracingSamplingMode
Parameter Sets: (All)
Aliases: Mode
Accepted values: Disabled, Enabled

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84e78-128">-SamplingRate</span><span class="sxs-lookup"><span data-stu-id="84e78-128">-SamplingRate</span></span>
<span data-ttu-id="84e78-129">Określa ilość wiadomości do próbkowania w celu dodania kontekstu śledzenia.</span><span class="sxs-lookup"><span data-stu-id="84e78-129">Controls the amount of messages sampled for adding trace context.</span></span>
<span data-ttu-id="84e78-130">Ta wartość jest wartością procentową.</span><span class="sxs-lookup"><span data-stu-id="84e78-130">This value is a percentage.</span></span>
<span data-ttu-id="84e78-131">Dozwolone są tylko wartości od 0 do 100 (włącznie).</span><span class="sxs-lookup"><span data-stu-id="84e78-131">Only values from 0 to 100 (inclusive) are permitted.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Rate

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84e78-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="84e78-132">-Confirm</span></span>
<span data-ttu-id="84e78-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="84e78-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84e78-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84e78-134">-WhatIf</span></span>
<span data-ttu-id="84e78-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84e78-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84e78-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="84e78-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84e78-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84e78-137">CommonParameters</span></span>
<span data-ttu-id="84e78-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84e78-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84e78-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84e78-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84e78-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="84e78-140">INPUTS</span></span>

### <span data-ttu-id="84e78-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="84e78-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="84e78-142">System.String</span><span class="sxs-lookup"><span data-stu-id="84e78-142">System.String</span></span>

## <span data-ttu-id="84e78-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="84e78-143">OUTPUTS</span></span>

### <span data-ttu-id="84e78-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span><span class="sxs-lookup"><span data-stu-id="84e78-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span></span>

## <span data-ttu-id="84e78-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="84e78-145">NOTES</span></span>

## <span data-ttu-id="84e78-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="84e78-146">RELATED LINKS</span></span>
