---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/set-aziothubdistributedtracing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDistributedTracing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDistributedTracing.md
ms.openlocfilehash: b1bdc6b5910f47fdca8e8b66ab99939945547a08
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004138"
---
# <span data-ttu-id="684d5-101">Set-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="684d5-101">Set-AzIotHubDistributedTracing</span></span>

## <span data-ttu-id="684d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="684d5-102">SYNOPSIS</span></span>
<span data-ttu-id="684d5-103">Aktualizowanie opcji śledzenia rozłożonego dla urządzenia.</span><span class="sxs-lookup"><span data-stu-id="684d5-103">Update the distributed tracing options for a device.</span></span>

## <span data-ttu-id="684d5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="684d5-104">SYNTAX</span></span>

### <span data-ttu-id="684d5-105">Zestaw zasobów (domyślny)</span><span class="sxs-lookup"><span data-stu-id="684d5-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubDistributedTracing [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-SamplingMode] <PSDistributedTracingSamplingMode> [-SamplingRate <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="684d5-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="684d5-106">InputObjectSet</span></span>
```
Set-AzIotHubDistributedTracing [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-SamplingMode] <PSDistributedTracingSamplingMode> [-SamplingRate <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="684d5-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="684d5-107">ResourceIdSet</span></span>
```
Set-AzIotHubDistributedTracing [-ResourceId] <String> [-DeviceId] <String>
 [-SamplingMode] <PSDistributedTracingSamplingMode> [-SamplingRate <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="684d5-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="684d5-108">DESCRIPTION</span></span>
<span data-ttu-id="684d5-109">Aktualizowanie opcji śledzenia rozłożonego dla urządzenia.</span><span class="sxs-lookup"><span data-stu-id="684d5-109">Update the distributed tracing options for a device.</span></span>

## <span data-ttu-id="684d5-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="684d5-110">EXAMPLES</span></span>

### <span data-ttu-id="684d5-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="684d5-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDistributedTracing -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -SamplingMode Enabled -SamplingRate 22

DeviceId      : mydevice1
Sampling Mode : Enabled
Sampling Rate : 22%
IsSynced      : False
```

<span data-ttu-id="684d5-112">Aktualizowanie opcji śledzenia rozłożonego dla urządzenia.</span><span class="sxs-lookup"><span data-stu-id="684d5-112">Update the distributed tracing options for a device.</span></span>

## <span data-ttu-id="684d5-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="684d5-113">PARAMETERS</span></span>

### <span data-ttu-id="684d5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="684d5-114">-DefaultProfile</span></span>
<span data-ttu-id="684d5-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="684d5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="684d5-116">— DeviceId</span><span class="sxs-lookup"><span data-stu-id="684d5-116">-DeviceId</span></span>
<span data-ttu-id="684d5-117">Identyfikator urządzenia docelowego.</span><span class="sxs-lookup"><span data-stu-id="684d5-117">Target Device Id.</span></span>

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

### <span data-ttu-id="684d5-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="684d5-118">-InputObject</span></span>
<span data-ttu-id="684d5-119">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="684d5-119">IotHub object</span></span>

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

### <span data-ttu-id="684d5-120">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="684d5-120">-IotHubName</span></span>
<span data-ttu-id="684d5-121">Nazwa Centrum Iot</span><span class="sxs-lookup"><span data-stu-id="684d5-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="684d5-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="684d5-122">-ResourceGroupName</span></span>
<span data-ttu-id="684d5-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="684d5-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="684d5-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="684d5-124">-ResourceId</span></span>
<span data-ttu-id="684d5-125">Identyfikator zasobu w aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="684d5-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="684d5-126">-SamplingMode</span><span class="sxs-lookup"><span data-stu-id="684d5-126">-SamplingMode</span></span>
<span data-ttu-id="684d5-127">Umożliwia włączenie i wyłączenie próbkowania w celu śledzenia rozłożonego.</span><span class="sxs-lookup"><span data-stu-id="684d5-127">Turns sampling for distributed tracing enable and disable.</span></span>

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

### <span data-ttu-id="684d5-128">-SamplingRate</span><span class="sxs-lookup"><span data-stu-id="684d5-128">-SamplingRate</span></span>
<span data-ttu-id="684d5-129">Określa ilość wiadomości, do których pobrano próbkę, aby dodać kontekst śledzenia.</span><span class="sxs-lookup"><span data-stu-id="684d5-129">Controls the amount of messages sampled for adding trace context.</span></span>
<span data-ttu-id="684d5-130">Ta wartość jest wartością procentową.</span><span class="sxs-lookup"><span data-stu-id="684d5-130">This value is a percentage.</span></span>
<span data-ttu-id="684d5-131">Dozwolone są tylko wartości od 0 do 100 (włącznie).</span><span class="sxs-lookup"><span data-stu-id="684d5-131">Only values from 0 to 100 (inclusive) are permitted.</span></span>

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

### <span data-ttu-id="684d5-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="684d5-132">-Confirm</span></span>
<span data-ttu-id="684d5-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="684d5-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="684d5-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="684d5-134">-WhatIf</span></span>
<span data-ttu-id="684d5-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="684d5-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="684d5-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="684d5-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="684d5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="684d5-137">CommonParameters</span></span>
<span data-ttu-id="684d5-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="684d5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="684d5-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="684d5-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="684d5-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="684d5-140">INPUTS</span></span>

### <span data-ttu-id="684d5-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="684d5-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="684d5-142">System.String</span><span class="sxs-lookup"><span data-stu-id="684d5-142">System.String</span></span>

## <span data-ttu-id="684d5-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="684d5-143">OUTPUTS</span></span>

### <span data-ttu-id="684d5-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span><span class="sxs-lookup"><span data-stu-id="684d5-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span></span>

## <span data-ttu-id="684d5-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="684d5-145">NOTES</span></span>

## <span data-ttu-id="684d5-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="684d5-146">RELATED LINKS</span></span>
