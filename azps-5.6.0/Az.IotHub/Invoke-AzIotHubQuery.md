---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/invoke-aziothubquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubQuery.md
ms.openlocfilehash: 955e09ab17644009f281223581ae2f5f45adfb33
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952641"
---
# <span data-ttu-id="b2f5a-101">Invoke-AzIotHubQuery</span><span class="sxs-lookup"><span data-stu-id="b2f5a-101">Invoke-AzIotHubQuery</span></span>

## <span data-ttu-id="b2f5a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2f5a-102">SYNOPSIS</span></span>
<span data-ttu-id="b2f5a-103">Wykonywanie zapytań w Centrum IoT przy użyciu zaawansowanego języka SQL.</span><span class="sxs-lookup"><span data-stu-id="b2f5a-103">Query an IoT Hub using a powerful SQL-like language.</span></span>

## <span data-ttu-id="b2f5a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b2f5a-104">SYNTAX</span></span>

### <span data-ttu-id="b2f5a-105">Zestaw zasobów (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b2f5a-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubQuery [-ResourceGroupName] <String> [-IotHubName] <String> [-Query] <String> [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2f5a-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b2f5a-106">InputObjectSet</span></span>
```
Invoke-AzIotHubQuery [-InputObject] <PSIotHub> [-Query] <String> [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2f5a-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b2f5a-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubQuery [-ResourceId] <String> [-Query] <String> [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2f5a-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="b2f5a-108">DESCRIPTION</span></span>
<span data-ttu-id="b2f5a-109">Wykonywanie zapytań w Centrum IoT przy użyciu zaawansowanego języka SQL w celu pobierania informacji dotyczących urządzeń i modułów, zadań i routingu wiadomości.</span><span class="sxs-lookup"><span data-stu-id="b2f5a-109">Query an IoT Hub using a powerful SQL-like language to retrieve information regarding device and module twins, jobs and message routing.</span></span>
<span data-ttu-id="b2f5a-110">Aby https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-query-language uzyskać więcej informacji, zobacz te informacje.</span><span class="sxs-lookup"><span data-stu-id="b2f5a-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-query-language for more information.</span></span>

## <span data-ttu-id="b2f5a-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b2f5a-111">EXAMPLES</span></span>

### <span data-ttu-id="b2f5a-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b2f5a-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Query "select * from devices"
```

<span data-ttu-id="b2f5a-113">Wykonywanie zapytań dotyczących wszystkich danych urządzenia w centrum Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="b2f5a-113">Query all device twin data in an Azure IoT Hub.</span></span>

### <span data-ttu-id="b2f5a-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="b2f5a-114">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Query "select * from devices.modules where devices.deviceId = 'myDevice1'" -Top 2
```

<span data-ttu-id="b2f5a-115">Zapytanie o 2 najważniejsze dane modułu na urządzeniu docelowym.</span><span class="sxs-lookup"><span data-stu-id="b2f5a-115">Query top 2 module twin data on a target device.</span></span>

## <span data-ttu-id="b2f5a-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b2f5a-116">PARAMETERS</span></span>

### <span data-ttu-id="b2f5a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2f5a-117">-DefaultProfile</span></span>
<span data-ttu-id="b2f5a-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b2f5a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2f5a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b2f5a-119">-InputObject</span></span>
<span data-ttu-id="b2f5a-120">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="b2f5a-120">IotHub object</span></span>

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

### <span data-ttu-id="b2f5a-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="b2f5a-121">-IotHubName</span></span>
<span data-ttu-id="b2f5a-122">Nazwa Centrum Iot</span><span class="sxs-lookup"><span data-stu-id="b2f5a-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="b2f5a-123">— zapytanie</span><span class="sxs-lookup"><span data-stu-id="b2f5a-123">-Query</span></span>
<span data-ttu-id="b2f5a-124">Kwerenda użytkownika do wykonania.</span><span class="sxs-lookup"><span data-stu-id="b2f5a-124">User query to be executed.</span></span>

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

### <span data-ttu-id="b2f5a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2f5a-125">-ResourceGroupName</span></span>
<span data-ttu-id="b2f5a-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="b2f5a-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="b2f5a-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b2f5a-127">-ResourceId</span></span>
<span data-ttu-id="b2f5a-128">Identyfikator zasobu w aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="b2f5a-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="b2f5a-129">— Na górze</span><span class="sxs-lookup"><span data-stu-id="b2f5a-129">-Top</span></span>
<span data-ttu-id="b2f5a-130">Maksymalna liczba elementów do zwrócenia.</span><span class="sxs-lookup"><span data-stu-id="b2f5a-130">Maximum number of elements to return.</span></span>
<span data-ttu-id="b2f5a-131">Domyślnie zapytanie nie ma żadnych limitów.</span><span class="sxs-lookup"><span data-stu-id="b2f5a-131">By default query has no cap.</span></span>

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

### <span data-ttu-id="b2f5a-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b2f5a-132">-Confirm</span></span>
<span data-ttu-id="b2f5a-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b2f5a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2f5a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2f5a-134">-WhatIf</span></span>
<span data-ttu-id="b2f5a-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2f5a-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b2f5a-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b2f5a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2f5a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2f5a-137">CommonParameters</span></span>
<span data-ttu-id="b2f5a-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2f5a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2f5a-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2f5a-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2f5a-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b2f5a-140">INPUTS</span></span>

### <span data-ttu-id="b2f5a-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="b2f5a-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="b2f5a-142">System.String</span><span class="sxs-lookup"><span data-stu-id="b2f5a-142">System.String</span></span>

## <span data-ttu-id="b2f5a-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b2f5a-143">OUTPUTS</span></span>

### <span data-ttu-id="b2f5a-144">System.String</span><span class="sxs-lookup"><span data-stu-id="b2f5a-144">System.String</span></span>

## <span data-ttu-id="b2f5a-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b2f5a-145">NOTES</span></span>

## <span data-ttu-id="b2f5a-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b2f5a-146">RELATED LINKS</span></span>
