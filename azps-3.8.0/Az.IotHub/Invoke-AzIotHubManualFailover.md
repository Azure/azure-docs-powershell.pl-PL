---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubmanualfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubManualFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubManualFailover.md
ms.openlocfilehash: d32cad2dc435c468ca785da4f81416c7c5330bd8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052787"
---
# <span data-ttu-id="511b6-101">Invoke-AzIotHubManualFailover</span><span class="sxs-lookup"><span data-stu-id="511b6-101">Invoke-AzIotHubManualFailover</span></span>

## <span data-ttu-id="511b6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="511b6-102">SYNOPSIS</span></span>
<span data-ttu-id="511b6-103">Wywoływanie procesu przełączania awaryjnego dla Centrum IoT w regionie odzyskiwania po awarii geograficznej.</span><span class="sxs-lookup"><span data-stu-id="511b6-103">Invoke failover process for the IoT Hub to the geo-paired disaster recovery region.</span></span>

## <span data-ttu-id="511b6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="511b6-104">SYNTAX</span></span>

### <span data-ttu-id="511b6-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="511b6-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubManualFailover [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="511b6-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="511b6-106">InputObjectSet</span></span>
```
Invoke-AzIotHubManualFailover [-InputObject] <PSIotHub> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="511b6-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="511b6-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubManualFailover [-ResourceId] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="511b6-108">Opis</span><span class="sxs-lookup"><span data-stu-id="511b6-108">DESCRIPTION</span></span>
<span data-ttu-id="511b6-109">Wyzwoli przejęcie awaryjne swojego centrum IoT w lokalizacji pomocniczej.</span><span class="sxs-lookup"><span data-stu-id="511b6-109">It will trigger the failover your IoT hub to the secondary location.</span></span> <span data-ttu-id="511b6-110">Ta czynność spowoduje powstanie czasu i utraty danych telemetrycznych w rozwiązaniu.</span><span class="sxs-lookup"><span data-stu-id="511b6-110">This action will cause down time and telemetry loss to your solution.</span></span> <span data-ttu-id="511b6-111">Jest to operacja długotrwała, która może trwać kilka minut.</span><span class="sxs-lookup"><span data-stu-id="511b6-111">This is a long running operation and could take several minutes to finish.</span></span> <span data-ttu-id="511b6-112">Podczas korzystania z tej funkcji należy zachować ostrożność.</span><span class="sxs-lookup"><span data-stu-id="511b6-112">Please exercise with caution when using it.</span></span>

## <span data-ttu-id="511b6-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="511b6-113">EXAMPLES</span></span>

### <span data-ttu-id="511b6-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="511b6-114">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubManualFailover -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="511b6-115">Inicjowanie procesu przełączania awaryjnego Centrum IoT myiothub.</span><span class="sxs-lookup"><span data-stu-id="511b6-115">Initiating failover process of "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="511b6-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="511b6-116">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubManualFailover -ResourceGroupName "myresourcegroup" -Name "myiothub" -AsJob
```

<span data-ttu-id="511b6-117">Inicjowanie procesu przełączania awaryjnego Centrum IoT "myiothub" w tle.</span><span class="sxs-lookup"><span data-stu-id="511b6-117">Initiating failover process of "myiothub" IoT Hub in the background.</span></span>

## <span data-ttu-id="511b6-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="511b6-118">PARAMETERS</span></span>

### <span data-ttu-id="511b6-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="511b6-119">-AsJob</span></span>
<span data-ttu-id="511b6-120">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="511b6-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="511b6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="511b6-121">-DefaultProfile</span></span>
<span data-ttu-id="511b6-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="511b6-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="511b6-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="511b6-123">-InputObject</span></span>
<span data-ttu-id="511b6-124">Obiekt Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="511b6-124">Iot Hub Object</span></span>

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

### <span data-ttu-id="511b6-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="511b6-125">-Name</span></span>
<span data-ttu-id="511b6-126">Nazwa Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="511b6-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="511b6-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="511b6-127">-PassThru</span></span>
<span data-ttu-id="511b6-128">Umożliwia zwrócenie obiektu logicznego.</span><span class="sxs-lookup"><span data-stu-id="511b6-128">Allows to return the boolean object.</span></span> <span data-ttu-id="511b6-129">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="511b6-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="511b6-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="511b6-130">-ResourceGroupName</span></span>
<span data-ttu-id="511b6-131">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="511b6-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="511b6-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="511b6-132">-ResourceId</span></span>
<span data-ttu-id="511b6-133">Identyfikator zasobu Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="511b6-133">Iot Hub Resource Id</span></span>

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

### <span data-ttu-id="511b6-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="511b6-134">-Confirm</span></span>
<span data-ttu-id="511b6-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="511b6-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="511b6-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="511b6-136">-WhatIf</span></span>
<span data-ttu-id="511b6-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="511b6-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="511b6-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="511b6-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="511b6-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="511b6-139">CommonParameters</span></span>
<span data-ttu-id="511b6-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="511b6-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="511b6-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="511b6-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="511b6-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="511b6-142">INPUTS</span></span>

### <span data-ttu-id="511b6-143">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="511b6-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="511b6-144">System. String</span><span class="sxs-lookup"><span data-stu-id="511b6-144">System.String</span></span>

## <span data-ttu-id="511b6-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="511b6-145">OUTPUTS</span></span>

### <span data-ttu-id="511b6-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="511b6-146">System.Boolean</span></span>

## <span data-ttu-id="511b6-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="511b6-147">NOTES</span></span>

## <span data-ttu-id="511b6-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="511b6-148">RELATED LINKS</span></span>
