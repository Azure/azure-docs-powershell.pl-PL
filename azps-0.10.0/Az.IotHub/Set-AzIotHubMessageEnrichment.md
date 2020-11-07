---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Set-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Set-AzIotHubMessageEnrichment.md
ms.openlocfilehash: 4ecbbe9f37e4a2adf8d5ae5a06ef631d7a3b34cc
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891333"
---
# <span data-ttu-id="6739f-101">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="6739f-101">Set-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="6739f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6739f-102">SYNOPSIS</span></span>
<span data-ttu-id="6739f-103">Aktualizowanie wzbogacania wiadomości w centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="6739f-103">Update a message enrichment in your IoT hub.</span></span>

## <span data-ttu-id="6739f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6739f-104">SYNTAX</span></span>

### <span data-ttu-id="6739f-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6739f-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key] <String> [-Value <String>]
 [-Endpoint <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6739f-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="6739f-106">InputObjectSet</span></span>
```
Set-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key] <String> [-Value <String>]
 [-Endpoint <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6739f-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="6739f-107">ResourceIdSet</span></span>
```
Set-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key] <String> [-Value <String>] [-Endpoint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6739f-108">Opis</span><span class="sxs-lookup"><span data-stu-id="6739f-108">DESCRIPTION</span></span>
<span data-ttu-id="6739f-109">Aby uzyskać szczegółowe wyjaśnienie dotyczące wzbogacenia wiadomości w centrum usługi Azure IoT, zobacz https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="6739f-109">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="6739f-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6739f-110">EXAMPLES</span></span>

### <span data-ttu-id="6739f-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6739f-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Value "updatedValue"

Key         : newKey
Value       : updatedValue
Endpoint(s) : {endpoint1, endpoint2}
```

<span data-ttu-id="6739f-112">Aktualizuje wartość wzbogacenia do "updatedValue" dla klucza "newKey".</span><span class="sxs-lookup"><span data-stu-id="6739f-112">Updates enrichment's value to "updatedValue" for the key "newKey".</span></span>
<span data-ttu-id="6739f-113">Aby uzyskać szczegółowe wyjaśnienie dotyczące wzbogacenia wiadomości w centrum usługi Azure IoT, zobacz https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="6739f-113">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

### <span data-ttu-id="6739f-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="6739f-114">Example 2</span></span>
```powershell
PS C:\> Set-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Endpoint endpoint1,endpoint2,endpoint3

Key         : newKey
Value       : value1
Endpoint(s) : {endpoint1, endpoint2, endpoint3}
```

<span data-ttu-id="6739f-115">Aktualizuje punkt końcowy wzbogacenia do "endpoint1, endpoint2, endpoint3" dla klucza "newKey".</span><span class="sxs-lookup"><span data-stu-id="6739f-115">Updates enrichment's endpoint to "endpoint1, endpoint2, endpoint3" for the key "newKey".</span></span>
<span data-ttu-id="6739f-116">Aby uzyskać szczegółowe wyjaśnienie dotyczące wzbogacenia wiadomości w centrum usługi Azure IoT, zobacz https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="6739f-116">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="6739f-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6739f-117">PARAMETERS</span></span>

### <span data-ttu-id="6739f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6739f-118">-DefaultProfile</span></span>
<span data-ttu-id="6739f-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6739f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6739f-120">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="6739f-120">-Endpoint</span></span>
<span data-ttu-id="6739f-121">Punkty końcowe, do których należy zastosować wzbogacenia.</span><span class="sxs-lookup"><span data-stu-id="6739f-121">Endpoint(s) to apply enrichments to.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6739f-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6739f-122">-InputObject</span></span>
<span data-ttu-id="6739f-123">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="6739f-123">IotHub Object</span></span>

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

### <span data-ttu-id="6739f-124">-Key</span><span class="sxs-lookup"><span data-stu-id="6739f-124">-Key</span></span>
<span data-ttu-id="6739f-125">Klucz wzbogacenia.</span><span class="sxs-lookup"><span data-stu-id="6739f-125">The enrichment's key.</span></span>

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

### <span data-ttu-id="6739f-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6739f-126">-Name</span></span>
<span data-ttu-id="6739f-127">Nazwa Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="6739f-127">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="6739f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6739f-128">-ResourceGroupName</span></span>
<span data-ttu-id="6739f-129">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="6739f-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="6739f-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6739f-130">-ResourceId</span></span>
<span data-ttu-id="6739f-131">Identyfikator zasobu IotHub</span><span class="sxs-lookup"><span data-stu-id="6739f-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="6739f-132">-Value</span><span class="sxs-lookup"><span data-stu-id="6739f-132">-Value</span></span>
<span data-ttu-id="6739f-133">Wartość wzbogacenia.</span><span class="sxs-lookup"><span data-stu-id="6739f-133">The enrichment's value.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6739f-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6739f-134">-Confirm</span></span>
<span data-ttu-id="6739f-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6739f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6739f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6739f-136">-WhatIf</span></span>
<span data-ttu-id="6739f-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6739f-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6739f-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6739f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6739f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6739f-139">CommonParameters</span></span>
<span data-ttu-id="6739f-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6739f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6739f-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6739f-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6739f-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6739f-142">INPUTS</span></span>

### <span data-ttu-id="6739f-143">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="6739f-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="6739f-144">System. String</span><span class="sxs-lookup"><span data-stu-id="6739f-144">System.String</span></span>

## <span data-ttu-id="6739f-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6739f-145">OUTPUTS</span></span>

### <span data-ttu-id="6739f-146">Microsoft. Azure. Commands. Management. IotHub. models. PSEnrichmentMetadata</span><span class="sxs-lookup"><span data-stu-id="6739f-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span></span>

## <span data-ttu-id="6739f-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6739f-147">NOTES</span></span>

## <span data-ttu-id="6739f-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6739f-148">RELATED LINKS</span></span>
