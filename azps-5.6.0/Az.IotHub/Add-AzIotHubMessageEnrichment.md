---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/add-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubMessageEnrichment.md
ms.openlocfilehash: 2e024d3b82b6e553aa40bd6e570a848645538e11
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997844"
---
# <span data-ttu-id="c72eb-101">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="c72eb-101">Add-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="c72eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c72eb-102">SYNOPSIS</span></span>
<span data-ttu-id="c72eb-103">Tworzy wzbogacanie wiadomości dla wybranych punktów końcowych w Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="c72eb-103">Creates a message enrichment for chosen endpoints in your IoT Hub.</span></span>

## <span data-ttu-id="c72eb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c72eb-104">SYNTAX</span></span>

### <span data-ttu-id="c72eb-105">Zestaw zasobów (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c72eb-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key] <String> -Value <String>
 -Endpoint <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c72eb-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c72eb-106">InputObjectSet</span></span>
```
Add-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key] <String> -Value <String> -Endpoint <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c72eb-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c72eb-107">ResourceIdSet</span></span>
```
Add-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key] <String> -Value <String> -Endpoint <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c72eb-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="c72eb-108">DESCRIPTION</span></span>
<span data-ttu-id="c72eb-109">Dodaj maksymalnie 10 wzbogacania wiadomości na centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="c72eb-109">Add up to 10 message enrichments per IoT Hub.</span></span> <span data-ttu-id="c72eb-110">Są one dodawane jako właściwości aplikacji do wiadomości wysyłanych do wybranych punktów końcowych.</span><span class="sxs-lookup"><span data-stu-id="c72eb-110">These are added as application properties to messages sent to chosen endpoint(s).</span></span>
<span data-ttu-id="c72eb-111">Aby dowiedzieć się więcej, zobacz https://docs.microsoft.com/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="c72eb-111">To know more, see https://docs.microsoft.com/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="c72eb-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c72eb-112">EXAMPLES</span></span>

### <span data-ttu-id="c72eb-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c72eb-113">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Value "newValue" -Endpoint endpoint1,endpoint2

Key          : newKey
Value        : newValue
Endpoint(s)  : { endpoint1, endpoint2 }
```

<span data-ttu-id="c72eb-114">Dodaj nowe wzbogacanie o klucz "newKey" i wartość "newValue".</span><span class="sxs-lookup"><span data-stu-id="c72eb-114">Add a new enrichment with key "newKey" and value "newValue".</span></span> <span data-ttu-id="c72eb-115">To nowe wzbogacanie jest stosowane do punktów końcowych "endpoint1" i "endpoint2".</span><span class="sxs-lookup"><span data-stu-id="c72eb-115">This new enrichment is applied to "endpoint1" and "endpoint2" endpoints.</span></span>

## <span data-ttu-id="c72eb-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c72eb-116">PARAMETERS</span></span>

### <span data-ttu-id="c72eb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c72eb-117">-DefaultProfile</span></span>
<span data-ttu-id="c72eb-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c72eb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c72eb-119">- Punkt końcowy</span><span class="sxs-lookup"><span data-stu-id="c72eb-119">-Endpoint</span></span>
<span data-ttu-id="c72eb-120">Punkty końcowe, do których można zastosować wzbogacenie.</span><span class="sxs-lookup"><span data-stu-id="c72eb-120">Endpoint(s) to apply enrichments to.</span></span>

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

### <span data-ttu-id="c72eb-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c72eb-121">-InputObject</span></span>
<span data-ttu-id="c72eb-122">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="c72eb-122">IotHub object</span></span>

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

### <span data-ttu-id="c72eb-123">- Key</span><span class="sxs-lookup"><span data-stu-id="c72eb-123">-Key</span></span>
<span data-ttu-id="c72eb-124">Klucz wzbogacenia.</span><span class="sxs-lookup"><span data-stu-id="c72eb-124">The enrichment's key.</span></span>

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

### <span data-ttu-id="c72eb-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c72eb-125">-Name</span></span>
<span data-ttu-id="c72eb-126">Nazwa Centrum Iot</span><span class="sxs-lookup"><span data-stu-id="c72eb-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="c72eb-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c72eb-127">-ResourceGroupName</span></span>
<span data-ttu-id="c72eb-128">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="c72eb-128">Name of the Resource Group</span></span>

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

### <span data-ttu-id="c72eb-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c72eb-129">-ResourceId</span></span>
<span data-ttu-id="c72eb-130">Identyfikator zasobu w aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="c72eb-130">IotHub Resource Id</span></span>

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

### <span data-ttu-id="c72eb-131">— Wartość</span><span class="sxs-lookup"><span data-stu-id="c72eb-131">-Value</span></span>
<span data-ttu-id="c72eb-132">Wartość tego wzbogacenia.</span><span class="sxs-lookup"><span data-stu-id="c72eb-132">The enrichment's value.</span></span>

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

### <span data-ttu-id="c72eb-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c72eb-133">-Confirm</span></span>
<span data-ttu-id="c72eb-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c72eb-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c72eb-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c72eb-135">-WhatIf</span></span>
<span data-ttu-id="c72eb-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c72eb-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c72eb-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c72eb-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c72eb-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c72eb-138">CommonParameters</span></span>
<span data-ttu-id="c72eb-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c72eb-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c72eb-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c72eb-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c72eb-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c72eb-141">INPUTS</span></span>

### <span data-ttu-id="c72eb-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="c72eb-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="c72eb-143">System.String</span><span class="sxs-lookup"><span data-stu-id="c72eb-143">System.String</span></span>

## <span data-ttu-id="c72eb-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c72eb-144">OUTPUTS</span></span>

### <span data-ttu-id="c72eb-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span><span class="sxs-lookup"><span data-stu-id="c72eb-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span></span>

## <span data-ttu-id="c72eb-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c72eb-146">NOTES</span></span>

## <span data-ttu-id="c72eb-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c72eb-147">RELATED LINKS</span></span>
