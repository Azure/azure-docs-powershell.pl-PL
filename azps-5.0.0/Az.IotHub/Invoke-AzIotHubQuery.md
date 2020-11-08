---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubQuery.md
ms.openlocfilehash: 6445e6281ff69f4eef54a5694f953beaa08ad098
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94234725"
---
# <span data-ttu-id="50006-101">Invoke-AzIotHubQuery</span><span class="sxs-lookup"><span data-stu-id="50006-101">Invoke-AzIotHubQuery</span></span>

## <span data-ttu-id="50006-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="50006-102">SYNOPSIS</span></span>
<span data-ttu-id="50006-103">Zbadaj Centrum IoT za pomocą wydajnego języka SQL.</span><span class="sxs-lookup"><span data-stu-id="50006-103">Query an IoT Hub using a powerful SQL-like language.</span></span>

## <span data-ttu-id="50006-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="50006-104">SYNTAX</span></span>

### <span data-ttu-id="50006-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="50006-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubQuery [-ResourceGroupName] <String> [-IotHubName] <String> [-Query] <String> [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50006-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="50006-106">InputObjectSet</span></span>
```
Invoke-AzIotHubQuery [-InputObject] <PSIotHub> [-Query] <String> [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50006-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="50006-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubQuery [-ResourceId] <String> [-Query] <String> [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50006-108">Opis</span><span class="sxs-lookup"><span data-stu-id="50006-108">DESCRIPTION</span></span>
<span data-ttu-id="50006-109">Zbadaj Centrum IoT za pomocą wydajnego języka SQL, aby pobrać informacje dotyczące urządzeń i modułów Twins, zadań i routingu wiadomości.</span><span class="sxs-lookup"><span data-stu-id="50006-109">Query an IoT Hub using a powerful SQL-like language to retrieve information regarding device and module twins, jobs and message routing.</span></span>
<span data-ttu-id="50006-110"> https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-query-languageAby uzyskać więcej informacji, zobacz.</span><span class="sxs-lookup"><span data-stu-id="50006-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-query-language for more information.</span></span>

## <span data-ttu-id="50006-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="50006-111">EXAMPLES</span></span>

### <span data-ttu-id="50006-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="50006-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Query "select * from devices"
```

<span data-ttu-id="50006-113">Badanie wszystkich danych dotyczących sznurka urządzenia w usłudze Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="50006-113">Query all device twin data in an Azure IoT Hub.</span></span>

### <span data-ttu-id="50006-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="50006-114">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Query "select * from devices.modules where devices.deviceId = 'myDevice1'" -Top 2
```

<span data-ttu-id="50006-115">Badanie na urządzeniu docelowym dwóch pierwszych danych dotyczących sznurów modułowych 2.</span><span class="sxs-lookup"><span data-stu-id="50006-115">Query top 2 module twin data on a target device.</span></span>

## <span data-ttu-id="50006-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="50006-116">PARAMETERS</span></span>

### <span data-ttu-id="50006-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50006-117">-DefaultProfile</span></span>
<span data-ttu-id="50006-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="50006-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50006-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="50006-119">-InputObject</span></span>
<span data-ttu-id="50006-120">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="50006-120">IotHub object</span></span>

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

### <span data-ttu-id="50006-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="50006-121">-IotHubName</span></span>
<span data-ttu-id="50006-122">Nazwa Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="50006-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="50006-123">-Query</span><span class="sxs-lookup"><span data-stu-id="50006-123">-Query</span></span>
<span data-ttu-id="50006-124">Kwerenda użytkownika do wykonania.</span><span class="sxs-lookup"><span data-stu-id="50006-124">User query to be executed.</span></span>

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

### <span data-ttu-id="50006-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50006-125">-ResourceGroupName</span></span>
<span data-ttu-id="50006-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="50006-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="50006-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="50006-127">-ResourceId</span></span>
<span data-ttu-id="50006-128">Identyfikator zasobu IotHub</span><span class="sxs-lookup"><span data-stu-id="50006-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="50006-129">-Początek</span><span class="sxs-lookup"><span data-stu-id="50006-129">-Top</span></span>
<span data-ttu-id="50006-130">Maksymalna liczba elementów do zwrócenia.</span><span class="sxs-lookup"><span data-stu-id="50006-130">Maximum number of elements to return.</span></span>
<span data-ttu-id="50006-131">Domyślnie w kwerendzie nie ma końca.</span><span class="sxs-lookup"><span data-stu-id="50006-131">By default query has no cap.</span></span>

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

### <span data-ttu-id="50006-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="50006-132">-Confirm</span></span>
<span data-ttu-id="50006-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50006-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50006-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50006-134">-WhatIf</span></span>
<span data-ttu-id="50006-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50006-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="50006-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="50006-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50006-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50006-137">CommonParameters</span></span>
<span data-ttu-id="50006-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50006-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50006-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50006-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50006-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="50006-140">INPUTS</span></span>

### <span data-ttu-id="50006-141">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="50006-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="50006-142">System. String</span><span class="sxs-lookup"><span data-stu-id="50006-142">System.String</span></span>

## <span data-ttu-id="50006-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="50006-143">OUTPUTS</span></span>

### <span data-ttu-id="50006-144">System. String</span><span class="sxs-lookup"><span data-stu-id="50006-144">System.String</span></span>

## <span data-ttu-id="50006-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="50006-145">NOTES</span></span>

## <span data-ttu-id="50006-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="50006-146">RELATED LINKS</span></span>
