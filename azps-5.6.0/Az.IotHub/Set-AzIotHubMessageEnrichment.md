---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/set-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubMessageEnrichment.md
ms.openlocfilehash: 0e9b26b4bd22d167dffbee4449aa811381960732
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004129"
---
# <span data-ttu-id="b7156-101">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="b7156-101">Set-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="b7156-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7156-102">SYNOPSIS</span></span>
<span data-ttu-id="b7156-103">Aktualizowanie wzbogacania wiadomości w centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="b7156-103">Update a message enrichment in your IoT hub.</span></span>

## <span data-ttu-id="b7156-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b7156-104">SYNTAX</span></span>

### <span data-ttu-id="b7156-105">Zestaw zasobów (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b7156-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key] <String> [-Value <String>]
 [-Endpoint <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7156-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b7156-106">InputObjectSet</span></span>
```
Set-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key] <String> [-Value <String>]
 [-Endpoint <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7156-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b7156-107">ResourceIdSet</span></span>
```
Set-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key] <String> [-Value <String>] [-Endpoint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7156-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="b7156-108">DESCRIPTION</span></span>
<span data-ttu-id="b7156-109">Aby uzyskać szczegółowe objaśnienie wzbogacania wiadomości w centrum Azure IoT Hub, zobacz https://docs.microsoft.com/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="b7156-109">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="b7156-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b7156-110">EXAMPLES</span></span>

### <span data-ttu-id="b7156-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b7156-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Value "updatedValue"

Key         : newKey
Value       : updatedValue
Endpoint(s) : {endpoint1, endpoint2}
```

<span data-ttu-id="b7156-112">Aktualizuje wartość wzbogacenia klucza "newKey" o wartość "updatedValue".</span><span class="sxs-lookup"><span data-stu-id="b7156-112">Updates enrichment's value to "updatedValue" for the key "newKey".</span></span>
<span data-ttu-id="b7156-113">Aby uzyskać szczegółowe objaśnienie wzbogacania wiadomości w centrum Azure IoT Hub, zobacz https://docs.microsoft.com/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="b7156-113">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

### <span data-ttu-id="b7156-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="b7156-114">Example 2</span></span>
```powershell
PS C:\> Set-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Endpoint endpoint1,endpoint2,endpoint3

Key         : newKey
Value       : value1
Endpoint(s) : {endpoint1, endpoint2, endpoint3}
```

<span data-ttu-id="b7156-115">Aktualizuje punkt końcowy wzbogacenia o "punkt końcowy1, punkt końcowy2, punkt końcowy3" dla klucza "newKey".</span><span class="sxs-lookup"><span data-stu-id="b7156-115">Updates enrichment's endpoint to "endpoint1, endpoint2, endpoint3" for the key "newKey".</span></span>
<span data-ttu-id="b7156-116">Aby uzyskać szczegółowe objaśnienie wzbogacania wiadomości w centrum Azure IoT Hub, zobacz https://docs.microsoft.com/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="b7156-116">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="b7156-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b7156-117">PARAMETERS</span></span>

### <span data-ttu-id="b7156-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7156-118">-DefaultProfile</span></span>
<span data-ttu-id="b7156-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b7156-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7156-120">- Punkt końcowy</span><span class="sxs-lookup"><span data-stu-id="b7156-120">-Endpoint</span></span>
<span data-ttu-id="b7156-121">Punkty końcowe, do których można zastosować wzbogacenie.</span><span class="sxs-lookup"><span data-stu-id="b7156-121">Endpoint(s) to apply enrichments to.</span></span>

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

### <span data-ttu-id="b7156-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b7156-122">-InputObject</span></span>
<span data-ttu-id="b7156-123">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="b7156-123">IotHub Object</span></span>

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

### <span data-ttu-id="b7156-124">- Key</span><span class="sxs-lookup"><span data-stu-id="b7156-124">-Key</span></span>
<span data-ttu-id="b7156-125">Klucz wzbogacenia.</span><span class="sxs-lookup"><span data-stu-id="b7156-125">The enrichment's key.</span></span>

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

### <span data-ttu-id="b7156-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b7156-126">-Name</span></span>
<span data-ttu-id="b7156-127">Nazwa Centrum Iot</span><span class="sxs-lookup"><span data-stu-id="b7156-127">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="b7156-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7156-128">-ResourceGroupName</span></span>
<span data-ttu-id="b7156-129">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="b7156-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="b7156-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b7156-130">-ResourceId</span></span>
<span data-ttu-id="b7156-131">Identyfikator zasobu w aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="b7156-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="b7156-132">— Wartość</span><span class="sxs-lookup"><span data-stu-id="b7156-132">-Value</span></span>
<span data-ttu-id="b7156-133">Wartość tego wzbogacenia.</span><span class="sxs-lookup"><span data-stu-id="b7156-133">The enrichment's value.</span></span>

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

### <span data-ttu-id="b7156-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b7156-134">-Confirm</span></span>
<span data-ttu-id="b7156-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b7156-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7156-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7156-136">-WhatIf</span></span>
<span data-ttu-id="b7156-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7156-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7156-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b7156-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7156-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7156-139">CommonParameters</span></span>
<span data-ttu-id="b7156-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7156-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7156-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7156-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7156-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b7156-142">INPUTS</span></span>

### <span data-ttu-id="b7156-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="b7156-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="b7156-144">System.String</span><span class="sxs-lookup"><span data-stu-id="b7156-144">System.String</span></span>

## <span data-ttu-id="b7156-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b7156-145">OUTPUTS</span></span>

### <span data-ttu-id="b7156-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span><span class="sxs-lookup"><span data-stu-id="b7156-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span></span>

## <span data-ttu-id="b7156-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b7156-147">NOTES</span></span>

## <span data-ttu-id="b7156-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b7156-148">RELATED LINKS</span></span>
