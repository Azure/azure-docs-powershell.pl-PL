---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubMessageEnrichment.md
ms.openlocfilehash: 683d03537f410b38260b502bc25ed90c9da9b4d2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94304699"
---
# <span data-ttu-id="a9beb-101">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="a9beb-101">Remove-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="a9beb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a9beb-102">SYNOPSIS</span></span>
<span data-ttu-id="a9beb-103">Usuwanie wiadomości w centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="a9beb-103">Delete a message enrichment in your IoT hub.</span></span>

## <span data-ttu-id="a9beb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a9beb-104">SYNTAX</span></span>

### <span data-ttu-id="a9beb-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a9beb-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9beb-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a9beb-106">InputObjectSet</span></span>
```
Remove-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9beb-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a9beb-107">ResourceIdSet</span></span>
```
Remove-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9beb-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a9beb-108">DESCRIPTION</span></span>
<span data-ttu-id="a9beb-109">Aby uzyskać szczegółowe wyjaśnienie dotyczące wzbogacenia wiadomości w centrum usługi Azure IoT, zobacz https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="a9beb-109">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="a9beb-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a9beb-110">EXAMPLES</span></span>

### <span data-ttu-id="a9beb-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a9beb-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Passthru

True
```

<span data-ttu-id="a9beb-112">Usuwa wzbogacenie wiadomości "newKey".</span><span class="sxs-lookup"><span data-stu-id="a9beb-112">Deletes "newKey" message enrichment.</span></span>

## <span data-ttu-id="a9beb-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a9beb-113">PARAMETERS</span></span>

### <span data-ttu-id="a9beb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9beb-114">-DefaultProfile</span></span>
<span data-ttu-id="a9beb-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a9beb-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9beb-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a9beb-116">-InputObject</span></span>
<span data-ttu-id="a9beb-117">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="a9beb-117">IotHub object</span></span>

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

### <span data-ttu-id="a9beb-118">-Key</span><span class="sxs-lookup"><span data-stu-id="a9beb-118">-Key</span></span>
<span data-ttu-id="a9beb-119">Klucz wzbogacenia.</span><span class="sxs-lookup"><span data-stu-id="a9beb-119">The enrichment's key.</span></span>

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

### <span data-ttu-id="a9beb-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a9beb-120">-Name</span></span>
<span data-ttu-id="a9beb-121">Nazwa Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="a9beb-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="a9beb-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a9beb-122">-PassThru</span></span>
<span data-ttu-id="a9beb-123">Umożliwia zwrócenie obiektu logicznego.</span><span class="sxs-lookup"><span data-stu-id="a9beb-123">Allows to return the boolean object.</span></span>
<span data-ttu-id="a9beb-124">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="a9beb-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a9beb-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9beb-125">-ResourceGroupName</span></span>
<span data-ttu-id="a9beb-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="a9beb-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="a9beb-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a9beb-127">-ResourceId</span></span>
<span data-ttu-id="a9beb-128">Identyfikator zasobu IotHub</span><span class="sxs-lookup"><span data-stu-id="a9beb-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="a9beb-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a9beb-129">-Confirm</span></span>
<span data-ttu-id="a9beb-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9beb-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9beb-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9beb-131">-WhatIf</span></span>
<span data-ttu-id="a9beb-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9beb-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9beb-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a9beb-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9beb-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9beb-134">CommonParameters</span></span>
<span data-ttu-id="a9beb-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9beb-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9beb-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9beb-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9beb-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a9beb-137">INPUTS</span></span>

### <span data-ttu-id="a9beb-138">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="a9beb-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="a9beb-139">System. String</span><span class="sxs-lookup"><span data-stu-id="a9beb-139">System.String</span></span>

## <span data-ttu-id="a9beb-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a9beb-140">OUTPUTS</span></span>

### <span data-ttu-id="a9beb-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a9beb-141">System.Boolean</span></span>

## <span data-ttu-id="a9beb-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a9beb-142">NOTES</span></span>

## <span data-ttu-id="a9beb-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a9beb-143">RELATED LINKS</span></span>
