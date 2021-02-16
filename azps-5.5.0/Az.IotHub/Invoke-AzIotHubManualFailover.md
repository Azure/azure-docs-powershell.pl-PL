---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubmanualfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubManualFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubManualFailover.md
ms.openlocfilehash: d32cad2dc435c468ca785da4f81416c7c5330bd8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203895"
---
# <span data-ttu-id="bb9b3-101">Invoke-AzIotHubManualFailover</span><span class="sxs-lookup"><span data-stu-id="bb9b3-101">Invoke-AzIotHubManualFailover</span></span>

## <span data-ttu-id="bb9b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb9b3-102">SYNOPSIS</span></span>
<span data-ttu-id="bb9b3-103">Wywołaj proces trybu failover dla centrum IoT do regionu odzyskiwania po awarii sparowanego geograficznie.</span><span class="sxs-lookup"><span data-stu-id="bb9b3-103">Invoke failover process for the IoT Hub to the geo-paired disaster recovery region.</span></span>

## <span data-ttu-id="bb9b3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bb9b3-104">SYNTAX</span></span>

### <span data-ttu-id="bb9b3-105">ResourceSet (Default)</span><span class="sxs-lookup"><span data-stu-id="bb9b3-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubManualFailover [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb9b3-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="bb9b3-106">InputObjectSet</span></span>
```
Invoke-AzIotHubManualFailover [-InputObject] <PSIotHub> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb9b3-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="bb9b3-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubManualFailover [-ResourceId] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb9b3-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="bb9b3-108">DESCRIPTION</span></span>
<span data-ttu-id="bb9b3-109">Spowoduje to wyzwolenie trybu failover Twojego centrum IoT do lokalizacji pomocniczej.</span><span class="sxs-lookup"><span data-stu-id="bb9b3-109">It will trigger the failover your IoT hub to the secondary location.</span></span> <span data-ttu-id="bb9b3-110">Ta akcja spowoduje spowolnienie czasu i utraty telemetrii rozwiązania.</span><span class="sxs-lookup"><span data-stu-id="bb9b3-110">This action will cause down time and telemetry loss to your solution.</span></span> <span data-ttu-id="bb9b3-111">Jest to długo uruchomiona operacja, która może potrwać kilka minut.</span><span class="sxs-lookup"><span data-stu-id="bb9b3-111">This is a long running operation and could take several minutes to finish.</span></span> <span data-ttu-id="bb9b3-112">Podczas korzystania z urządzenia należy zachować ostrożność.</span><span class="sxs-lookup"><span data-stu-id="bb9b3-112">Please exercise with caution when using it.</span></span>

## <span data-ttu-id="bb9b3-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bb9b3-113">EXAMPLES</span></span>

### <span data-ttu-id="bb9b3-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bb9b3-114">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubManualFailover -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="bb9b3-115">Inicjowanie procesu trybu failover centrum IoT "myiothub".</span><span class="sxs-lookup"><span data-stu-id="bb9b3-115">Initiating failover process of "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="bb9b3-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="bb9b3-116">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubManualFailover -ResourceGroupName "myresourcegroup" -Name "myiothub" -AsJob
```

<span data-ttu-id="bb9b3-117">Inicjowanie procesu failover centrum IoT Hub "myiothub" w tle.</span><span class="sxs-lookup"><span data-stu-id="bb9b3-117">Initiating failover process of "myiothub" IoT Hub in the background.</span></span>

## <span data-ttu-id="bb9b3-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bb9b3-118">PARAMETERS</span></span>

### <span data-ttu-id="bb9b3-119">— AsJob</span><span class="sxs-lookup"><span data-stu-id="bb9b3-119">-AsJob</span></span>
<span data-ttu-id="bb9b3-120">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="bb9b3-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bb9b3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb9b3-121">-DefaultProfile</span></span>
<span data-ttu-id="bb9b3-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="bb9b3-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb9b3-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bb9b3-123">-InputObject</span></span>
<span data-ttu-id="bb9b3-124">Obiekt Centrum Iot</span><span class="sxs-lookup"><span data-stu-id="bb9b3-124">Iot Hub Object</span></span>

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

### <span data-ttu-id="bb9b3-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="bb9b3-125">-Name</span></span>
<span data-ttu-id="bb9b3-126">Nazwa Centrum Iot</span><span class="sxs-lookup"><span data-stu-id="bb9b3-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="bb9b3-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bb9b3-127">-PassThru</span></span>
<span data-ttu-id="bb9b3-128">Zwraca obiekt logiczny.</span><span class="sxs-lookup"><span data-stu-id="bb9b3-128">Allows to return the boolean object.</span></span> <span data-ttu-id="bb9b3-129">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="bb9b3-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="bb9b3-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb9b3-130">-ResourceGroupName</span></span>
<span data-ttu-id="bb9b3-131">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="bb9b3-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="bb9b3-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bb9b3-132">-ResourceId</span></span>
<span data-ttu-id="bb9b3-133">Identyfikator zasobu centrum Iot</span><span class="sxs-lookup"><span data-stu-id="bb9b3-133">Iot Hub Resource Id</span></span>

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

### <span data-ttu-id="bb9b3-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bb9b3-134">-Confirm</span></span>
<span data-ttu-id="bb9b3-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="bb9b3-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb9b3-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb9b3-136">-WhatIf</span></span>
<span data-ttu-id="bb9b3-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb9b3-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bb9b3-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="bb9b3-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb9b3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb9b3-139">CommonParameters</span></span>
<span data-ttu-id="bb9b3-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb9b3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb9b3-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb9b3-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb9b3-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bb9b3-142">INPUTS</span></span>

### <span data-ttu-id="bb9b3-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="bb9b3-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="bb9b3-144">System.String</span><span class="sxs-lookup"><span data-stu-id="bb9b3-144">System.String</span></span>

## <span data-ttu-id="bb9b3-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bb9b3-145">OUTPUTS</span></span>

### <span data-ttu-id="bb9b3-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bb9b3-146">System.Boolean</span></span>

## <span data-ttu-id="bb9b3-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bb9b3-147">NOTES</span></span>

## <span data-ttu-id="bb9b3-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bb9b3-148">RELATED LINKS</span></span>
