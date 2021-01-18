---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubQuery.md
ms.openlocfilehash: 6445e6281ff69f4eef54a5694f953beaa08ad098
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503484"
---
# <span data-ttu-id="c2b67-101">Invoke-AzIotHubQuery</span><span class="sxs-lookup"><span data-stu-id="c2b67-101">Invoke-AzIotHubQuery</span></span>

## <span data-ttu-id="c2b67-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c2b67-102">SYNOPSIS</span></span>
<span data-ttu-id="c2b67-103">Zbadaj Centrum IoT za pomocą wydajnego języka SQL.</span><span class="sxs-lookup"><span data-stu-id="c2b67-103">Query an IoT Hub using a powerful SQL-like language.</span></span>

## <span data-ttu-id="c2b67-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c2b67-104">SYNTAX</span></span>

### <span data-ttu-id="c2b67-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c2b67-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubQuery [-ResourceGroupName] <String> [-IotHubName] <String> [-Query] <String> [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2b67-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c2b67-106">InputObjectSet</span></span>
```
Invoke-AzIotHubQuery [-InputObject] <PSIotHub> [-Query] <String> [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2b67-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c2b67-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubQuery [-ResourceId] <String> [-Query] <String> [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2b67-108">Opis</span><span class="sxs-lookup"><span data-stu-id="c2b67-108">DESCRIPTION</span></span>
<span data-ttu-id="c2b67-109">Zbadaj Centrum IoT za pomocą wydajnego języka SQL, aby pobrać informacje dotyczące urządzeń i modułów Twins, zadań i routingu wiadomości.</span><span class="sxs-lookup"><span data-stu-id="c2b67-109">Query an IoT Hub using a powerful SQL-like language to retrieve information regarding device and module twins, jobs and message routing.</span></span>
<span data-ttu-id="c2b67-110"> https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-query-languageAby uzyskać więcej informacji, zobacz.</span><span class="sxs-lookup"><span data-stu-id="c2b67-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-query-language for more information.</span></span>

## <span data-ttu-id="c2b67-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c2b67-111">EXAMPLES</span></span>

### <span data-ttu-id="c2b67-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c2b67-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Query "select * from devices"
```

<span data-ttu-id="c2b67-113">Badanie wszystkich danych dotyczących sznurka urządzenia w usłudze Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="c2b67-113">Query all device twin data in an Azure IoT Hub.</span></span>

### <span data-ttu-id="c2b67-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="c2b67-114">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Query "select * from devices.modules where devices.deviceId = 'myDevice1'" -Top 2
```

<span data-ttu-id="c2b67-115">Badanie na urządzeniu docelowym dwóch pierwszych danych dotyczących sznurów modułowych 2.</span><span class="sxs-lookup"><span data-stu-id="c2b67-115">Query top 2 module twin data on a target device.</span></span>

## <span data-ttu-id="c2b67-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c2b67-116">PARAMETERS</span></span>

### <span data-ttu-id="c2b67-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2b67-117">-DefaultProfile</span></span>
<span data-ttu-id="c2b67-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c2b67-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2b67-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c2b67-119">-InputObject</span></span>
<span data-ttu-id="c2b67-120">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="c2b67-120">IotHub object</span></span>

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

### <span data-ttu-id="c2b67-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="c2b67-121">-IotHubName</span></span>
<span data-ttu-id="c2b67-122">Nazwa Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="c2b67-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="c2b67-123">-Query</span><span class="sxs-lookup"><span data-stu-id="c2b67-123">-Query</span></span>
<span data-ttu-id="c2b67-124">Kwerenda użytkownika do wykonania.</span><span class="sxs-lookup"><span data-stu-id="c2b67-124">User query to be executed.</span></span>

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

### <span data-ttu-id="c2b67-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2b67-125">-ResourceGroupName</span></span>
<span data-ttu-id="c2b67-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="c2b67-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="c2b67-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c2b67-127">-ResourceId</span></span>
<span data-ttu-id="c2b67-128">Identyfikator zasobu IotHub</span><span class="sxs-lookup"><span data-stu-id="c2b67-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="c2b67-129">-Początek</span><span class="sxs-lookup"><span data-stu-id="c2b67-129">-Top</span></span>
<span data-ttu-id="c2b67-130">Maksymalna liczba elementów do zwrócenia.</span><span class="sxs-lookup"><span data-stu-id="c2b67-130">Maximum number of elements to return.</span></span>
<span data-ttu-id="c2b67-131">Domyślnie w kwerendzie nie ma końca.</span><span class="sxs-lookup"><span data-stu-id="c2b67-131">By default query has no cap.</span></span>

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

### <span data-ttu-id="c2b67-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c2b67-132">-Confirm</span></span>
<span data-ttu-id="c2b67-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2b67-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2b67-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2b67-134">-WhatIf</span></span>
<span data-ttu-id="c2b67-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2b67-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c2b67-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c2b67-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2b67-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2b67-137">CommonParameters</span></span>
<span data-ttu-id="c2b67-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2b67-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2b67-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2b67-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2b67-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c2b67-140">INPUTS</span></span>

### <span data-ttu-id="c2b67-141">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="c2b67-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="c2b67-142">System. String</span><span class="sxs-lookup"><span data-stu-id="c2b67-142">System.String</span></span>

## <span data-ttu-id="c2b67-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c2b67-143">OUTPUTS</span></span>

### <span data-ttu-id="c2b67-144">System. String</span><span class="sxs-lookup"><span data-stu-id="c2b67-144">System.String</span></span>

## <span data-ttu-id="c2b67-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c2b67-145">NOTES</span></span>

## <span data-ttu-id="c2b67-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c2b67-146">RELATED LINKS</span></span>
