---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubMessageEnrichment.md
ms.openlocfilehash: 558452481ed3feef979b78d7f134869d141caa20
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705210"
---
# <span data-ttu-id="d9688-101">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="d9688-101">Remove-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="d9688-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d9688-102">SYNOPSIS</span></span>
<span data-ttu-id="d9688-103">Usuwanie wiadomości w centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="d9688-103">Delete a message enrichment in your IoT hub.</span></span>

## <span data-ttu-id="d9688-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d9688-104">SYNTAX</span></span>

### <span data-ttu-id="d9688-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d9688-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9688-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d9688-106">InputObjectSet</span></span>
```
Remove-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9688-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d9688-107">ResourceIdSet</span></span>
```
Remove-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9688-108">Opis</span><span class="sxs-lookup"><span data-stu-id="d9688-108">DESCRIPTION</span></span>
<span data-ttu-id="d9688-109">Aby uzyskać szczegółowe wyjaśnienie dotyczące wzbogacenia wiadomości w centrum usługi Azure IoT, zobacz https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="d9688-109">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="d9688-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d9688-110">EXAMPLES</span></span>

### <span data-ttu-id="d9688-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d9688-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Passthru

True
```

<span data-ttu-id="d9688-112">Usuwa wzbogacenie wiadomości "newKey".</span><span class="sxs-lookup"><span data-stu-id="d9688-112">Deletes "newKey" message enrichment.</span></span>

## <span data-ttu-id="d9688-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d9688-113">PARAMETERS</span></span>

### <span data-ttu-id="d9688-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9688-114">-DefaultProfile</span></span>
<span data-ttu-id="d9688-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d9688-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9688-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d9688-116">-InputObject</span></span>
<span data-ttu-id="d9688-117">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="d9688-117">IotHub object</span></span>

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

### <span data-ttu-id="d9688-118">-Key</span><span class="sxs-lookup"><span data-stu-id="d9688-118">-Key</span></span>
<span data-ttu-id="d9688-119">Klucz wzbogacenia.</span><span class="sxs-lookup"><span data-stu-id="d9688-119">The enrichment's key.</span></span>

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

### <span data-ttu-id="d9688-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d9688-120">-Name</span></span>
<span data-ttu-id="d9688-121">Nazwa Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="d9688-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="d9688-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d9688-122">-PassThru</span></span>
<span data-ttu-id="d9688-123">Umożliwia zwrócenie obiektu logicznego.</span><span class="sxs-lookup"><span data-stu-id="d9688-123">Allows to return the boolean object.</span></span>
<span data-ttu-id="d9688-124">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="d9688-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d9688-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9688-125">-ResourceGroupName</span></span>
<span data-ttu-id="d9688-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="d9688-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="d9688-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d9688-127">-ResourceId</span></span>
<span data-ttu-id="d9688-128">Identyfikator zasobu IotHub</span><span class="sxs-lookup"><span data-stu-id="d9688-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="d9688-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d9688-129">-Confirm</span></span>
<span data-ttu-id="d9688-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9688-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9688-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9688-131">-WhatIf</span></span>
<span data-ttu-id="d9688-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9688-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9688-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d9688-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9688-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9688-134">CommonParameters</span></span>
<span data-ttu-id="d9688-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9688-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9688-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9688-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9688-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d9688-137">INPUTS</span></span>

### <span data-ttu-id="d9688-138">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="d9688-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="d9688-139">System. String</span><span class="sxs-lookup"><span data-stu-id="d9688-139">System.String</span></span>

## <span data-ttu-id="d9688-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d9688-140">OUTPUTS</span></span>

### <span data-ttu-id="d9688-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d9688-141">System.Boolean</span></span>

## <span data-ttu-id="d9688-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d9688-142">NOTES</span></span>

## <span data-ttu-id="d9688-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d9688-143">RELATED LINKS</span></span>
