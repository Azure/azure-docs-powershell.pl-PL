---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubQuery.md
ms.openlocfilehash: 6445e6281ff69f4eef54a5694f953beaa08ad098
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187635"
---
# <span data-ttu-id="bb42d-101">Invoke-AzIotHubQuery</span><span class="sxs-lookup"><span data-stu-id="bb42d-101">Invoke-AzIotHubQuery</span></span>

## <span data-ttu-id="bb42d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb42d-102">SYNOPSIS</span></span>
<span data-ttu-id="bb42d-103">Wykonywanie zapytań w Centrum IoT przy użyciu zaawansowanego języka SQL.</span><span class="sxs-lookup"><span data-stu-id="bb42d-103">Query an IoT Hub using a powerful SQL-like language.</span></span>

## <span data-ttu-id="bb42d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bb42d-104">SYNTAX</span></span>

### <span data-ttu-id="bb42d-105">ResourceSet (Default)</span><span class="sxs-lookup"><span data-stu-id="bb42d-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubQuery [-ResourceGroupName] <String> [-IotHubName] <String> [-Query] <String> [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb42d-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="bb42d-106">InputObjectSet</span></span>
```
Invoke-AzIotHubQuery [-InputObject] <PSIotHub> [-Query] <String> [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb42d-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="bb42d-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubQuery [-ResourceId] <String> [-Query] <String> [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb42d-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="bb42d-108">DESCRIPTION</span></span>
<span data-ttu-id="bb42d-109">Wykonywanie zapytań w Centrum IoT przy użyciu zaawansowanego języka SQL w celu pobierania informacji dotyczących urządzeń i modułów, zadań i routingu wiadomości.</span><span class="sxs-lookup"><span data-stu-id="bb42d-109">Query an IoT Hub using a powerful SQL-like language to retrieve information regarding device and module twins, jobs and message routing.</span></span>
<span data-ttu-id="bb42d-110">Aby https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-query-language uzyskać więcej informacji, zobacz.</span><span class="sxs-lookup"><span data-stu-id="bb42d-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-query-language for more information.</span></span>

## <span data-ttu-id="bb42d-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bb42d-111">EXAMPLES</span></span>

### <span data-ttu-id="bb42d-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bb42d-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Query "select * from devices"
```

<span data-ttu-id="bb42d-113">Przeszukaj wszystkie dane urządzenia w centrum Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="bb42d-113">Query all device twin data in an Azure IoT Hub.</span></span>

### <span data-ttu-id="bb42d-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="bb42d-114">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Query "select * from devices.modules where devices.deviceId = 'myDevice1'" -Top 2
```

<span data-ttu-id="bb42d-115">Zapytanie o 2 najważniejsze dane modułu na urządzeniu docelowym.</span><span class="sxs-lookup"><span data-stu-id="bb42d-115">Query top 2 module twin data on a target device.</span></span>

## <span data-ttu-id="bb42d-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bb42d-116">PARAMETERS</span></span>

### <span data-ttu-id="bb42d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb42d-117">-DefaultProfile</span></span>
<span data-ttu-id="bb42d-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="bb42d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb42d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bb42d-119">-InputObject</span></span>
<span data-ttu-id="bb42d-120">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="bb42d-120">IotHub object</span></span>

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

### <span data-ttu-id="bb42d-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="bb42d-121">-IotHubName</span></span>
<span data-ttu-id="bb42d-122">Nazwa Centrum Iot</span><span class="sxs-lookup"><span data-stu-id="bb42d-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="bb42d-123">— zapytanie</span><span class="sxs-lookup"><span data-stu-id="bb42d-123">-Query</span></span>
<span data-ttu-id="bb42d-124">Kwerenda użytkownika do wykonania.</span><span class="sxs-lookup"><span data-stu-id="bb42d-124">User query to be executed.</span></span>

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

### <span data-ttu-id="bb42d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb42d-125">-ResourceGroupName</span></span>
<span data-ttu-id="bb42d-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="bb42d-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="bb42d-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bb42d-127">-ResourceId</span></span>
<span data-ttu-id="bb42d-128">Identyfikator zasobu w aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="bb42d-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="bb42d-129">— Na górze</span><span class="sxs-lookup"><span data-stu-id="bb42d-129">-Top</span></span>
<span data-ttu-id="bb42d-130">Maksymalna liczba elementów do zwrócenia.</span><span class="sxs-lookup"><span data-stu-id="bb42d-130">Maximum number of elements to return.</span></span>
<span data-ttu-id="bb42d-131">Domyślnie zapytanie nie ma żadnych limitów.</span><span class="sxs-lookup"><span data-stu-id="bb42d-131">By default query has no cap.</span></span>

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

### <span data-ttu-id="bb42d-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bb42d-132">-Confirm</span></span>
<span data-ttu-id="bb42d-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="bb42d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb42d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb42d-134">-WhatIf</span></span>
<span data-ttu-id="bb42d-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb42d-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bb42d-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="bb42d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb42d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb42d-137">CommonParameters</span></span>
<span data-ttu-id="bb42d-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb42d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb42d-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb42d-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb42d-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bb42d-140">INPUTS</span></span>

### <span data-ttu-id="bb42d-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="bb42d-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="bb42d-142">System.String</span><span class="sxs-lookup"><span data-stu-id="bb42d-142">System.String</span></span>

## <span data-ttu-id="bb42d-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bb42d-143">OUTPUTS</span></span>

### <span data-ttu-id="bb42d-144">System.String</span><span class="sxs-lookup"><span data-stu-id="bb42d-144">System.String</span></span>

## <span data-ttu-id="bb42d-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bb42d-145">NOTES</span></span>

## <span data-ttu-id="bb42d-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bb42d-146">RELATED LINKS</span></span>
