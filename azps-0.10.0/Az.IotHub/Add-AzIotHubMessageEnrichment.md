---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Add-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Add-AzIotHubMessageEnrichment.md
ms.openlocfilehash: caae747f7accd76db1424d14274416f0de97122d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893126"
---
# <span data-ttu-id="d4d75-101">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="d4d75-101">Add-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="d4d75-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d4d75-102">SYNOPSIS</span></span>
<span data-ttu-id="d4d75-103">Tworzy wzbogacanie wiadomości dla wybranych punktów końcowych w centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="d4d75-103">Creates a message enrichment for chosen endpoints in your IoT Hub.</span></span>

## <span data-ttu-id="d4d75-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d4d75-104">SYNTAX</span></span>

### <span data-ttu-id="d4d75-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d4d75-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key] <String> -Value <String>
 -Endpoint <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4d75-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d4d75-106">InputObjectSet</span></span>
```
Add-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key] <String> -Value <String> -Endpoint <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4d75-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d4d75-107">ResourceIdSet</span></span>
```
Add-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key] <String> -Value <String> -Endpoint <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4d75-108">Opis</span><span class="sxs-lookup"><span data-stu-id="d4d75-108">DESCRIPTION</span></span>
<span data-ttu-id="d4d75-109">Dodaj maksymalnie 10 ulepszonych wiadomości dla każdego centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="d4d75-109">Add up to 10 message enrichments per IoT Hub.</span></span> <span data-ttu-id="d4d75-110">Są one dodawane jako właściwości aplikacji do wiadomości wysyłanych do wybranych punktów końcowych.</span><span class="sxs-lookup"><span data-stu-id="d4d75-110">These are added as application properties to messages sent to chosen endpoint(s).</span></span>
<span data-ttu-id="d4d75-111">Aby dowiedzieć się więcej, zobacz https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="d4d75-111">To know more, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="d4d75-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d4d75-112">EXAMPLES</span></span>

### <span data-ttu-id="d4d75-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d4d75-113">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Value "newValue" -Endpoint endpoint1,endpoint2

Key          : newKey
Value        : newValue
Endpoint(s)  : { endpoint1, endpoint2 }
```

<span data-ttu-id="d4d75-114">Dodaj nowe wzbogacanie za pomocą klucza "newKey" i wartości "newValue".</span><span class="sxs-lookup"><span data-stu-id="d4d75-114">Add a new enrichment with key "newKey" and value "newValue".</span></span> <span data-ttu-id="d4d75-115">Nowe wzbogacanie jest stosowane do punktów końcowych "endpoint1" i "endpoint2".</span><span class="sxs-lookup"><span data-stu-id="d4d75-115">This new enrichment is applied to "endpoint1" and "endpoint2" endpoints.</span></span>

## <span data-ttu-id="d4d75-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d4d75-116">PARAMETERS</span></span>

### <span data-ttu-id="d4d75-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4d75-117">-DefaultProfile</span></span>
<span data-ttu-id="d4d75-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d4d75-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4d75-119">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="d4d75-119">-Endpoint</span></span>
<span data-ttu-id="d4d75-120">Punkty końcowe, do których należy zastosować wzbogacenia.</span><span class="sxs-lookup"><span data-stu-id="d4d75-120">Endpoint(s) to apply enrichments to.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4d75-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d4d75-121">-InputObject</span></span>
<span data-ttu-id="d4d75-122">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="d4d75-122">IotHub object</span></span>

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

### <span data-ttu-id="d4d75-123">-Key</span><span class="sxs-lookup"><span data-stu-id="d4d75-123">-Key</span></span>
<span data-ttu-id="d4d75-124">Klucz wzbogacenia.</span><span class="sxs-lookup"><span data-stu-id="d4d75-124">The enrichment's key.</span></span>

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

### <span data-ttu-id="d4d75-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d4d75-125">-Name</span></span>
<span data-ttu-id="d4d75-126">Nazwa Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="d4d75-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="d4d75-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4d75-127">-ResourceGroupName</span></span>
<span data-ttu-id="d4d75-128">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="d4d75-128">Name of the Resource Group</span></span>

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

### <span data-ttu-id="d4d75-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d4d75-129">-ResourceId</span></span>
<span data-ttu-id="d4d75-130">Identyfikator zasobu IotHub</span><span class="sxs-lookup"><span data-stu-id="d4d75-130">IotHub Resource Id</span></span>

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

### <span data-ttu-id="d4d75-131">-Value</span><span class="sxs-lookup"><span data-stu-id="d4d75-131">-Value</span></span>
<span data-ttu-id="d4d75-132">Wartość wzbogacenia.</span><span class="sxs-lookup"><span data-stu-id="d4d75-132">The enrichment's value.</span></span>

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

### <span data-ttu-id="d4d75-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d4d75-133">-Confirm</span></span>
<span data-ttu-id="d4d75-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4d75-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4d75-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4d75-135">-WhatIf</span></span>
<span data-ttu-id="d4d75-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4d75-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4d75-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d4d75-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4d75-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4d75-138">CommonParameters</span></span>
<span data-ttu-id="d4d75-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4d75-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4d75-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4d75-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4d75-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d4d75-141">INPUTS</span></span>

### <span data-ttu-id="d4d75-142">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="d4d75-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="d4d75-143">System. String</span><span class="sxs-lookup"><span data-stu-id="d4d75-143">System.String</span></span>

## <span data-ttu-id="d4d75-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d4d75-144">OUTPUTS</span></span>

### <span data-ttu-id="d4d75-145">Microsoft. Azure. Commands. Management. IotHub. models. PSEnrichmentMetadata</span><span class="sxs-lookup"><span data-stu-id="d4d75-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span></span>

## <span data-ttu-id="d4d75-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d4d75-146">NOTES</span></span>

## <span data-ttu-id="d4d75-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d4d75-147">RELATED LINKS</span></span>
