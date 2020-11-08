---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubModule.md
ms.openlocfilehash: 3362fd6b1e60fa975277c97ea76a8e8c15ee29a4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223479"
---
# <span data-ttu-id="6e2b4-101">Remove-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="6e2b4-101">Remove-AzIotHubModule</span></span>

## <span data-ttu-id="6e2b4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6e2b4-102">SYNOPSIS</span></span>
<span data-ttu-id="6e2b4-103">Usuń moduły na docelowym urządzeniu IoT w centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="6e2b4-103">Delete module(s) on a target IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="6e2b4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6e2b4-104">SYNTAX</span></span>

### <span data-ttu-id="6e2b4-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6e2b4-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubModule [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6e2b4-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="6e2b4-106">InputObjectSet</span></span>
```
Remove-AzIotHubModule [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e2b4-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="6e2b4-107">ResourceIdSet</span></span>
```
Remove-AzIotHubModule [-ResourceId] <String> [-DeviceId] <String> [-ModuleId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e2b4-108">Opis</span><span class="sxs-lookup"><span data-stu-id="6e2b4-108">DESCRIPTION</span></span>
<span data-ttu-id="6e2b4-109">Usuń moduły na docelowym urządzeniu IoT w centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="6e2b4-109">Delete module(s) on a target IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="6e2b4-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6e2b4-110">EXAMPLES</span></span>

### <span data-ttu-id="6e2b4-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6e2b4-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -PassThru

True
```

<span data-ttu-id="6e2b4-112">Usuwanie modułu urządzenia IoT.</span><span class="sxs-lookup"><span data-stu-id="6e2b4-112">Delete an Iot device module.</span></span>

### <span data-ttu-id="6e2b4-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="6e2b4-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIotHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -PassThru

True
```

<span data-ttu-id="6e2b4-114">Usuń wszystkie moduły urządzeń IoT.</span><span class="sxs-lookup"><span data-stu-id="6e2b4-114">Delete all Iot device modules.</span></span>

## <span data-ttu-id="6e2b4-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6e2b4-115">PARAMETERS</span></span>

### <span data-ttu-id="6e2b4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e2b4-116">-DefaultProfile</span></span>
<span data-ttu-id="6e2b4-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6e2b4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e2b4-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="6e2b4-118">-DeviceId</span></span>
<span data-ttu-id="6e2b4-119">Identyfikator urządzenia docelowego.</span><span class="sxs-lookup"><span data-stu-id="6e2b4-119">Target Device Id.</span></span>

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

### <span data-ttu-id="6e2b4-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6e2b4-120">-InputObject</span></span>
<span data-ttu-id="6e2b4-121">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="6e2b4-121">IotHub object</span></span>

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

### <span data-ttu-id="6e2b4-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="6e2b4-122">-IotHubName</span></span>
<span data-ttu-id="6e2b4-123">Nazwa Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="6e2b4-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="6e2b4-124">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="6e2b4-124">-ModuleId</span></span>
<span data-ttu-id="6e2b4-125">Identyfikator modułu docelowego.</span><span class="sxs-lookup"><span data-stu-id="6e2b4-125">Target Module Id.</span></span>

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

### <span data-ttu-id="6e2b4-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6e2b4-126">-PassThru</span></span>
<span data-ttu-id="6e2b4-127">Umożliwia zwrócenie obiektu logicznego.</span><span class="sxs-lookup"><span data-stu-id="6e2b4-127">Allows to return the boolean object.</span></span>
<span data-ttu-id="6e2b4-128">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="6e2b4-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6e2b4-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e2b4-129">-ResourceGroupName</span></span>
<span data-ttu-id="6e2b4-130">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="6e2b4-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="6e2b4-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6e2b4-131">-ResourceId</span></span>
<span data-ttu-id="6e2b4-132">Identyfikator zasobu IotHub</span><span class="sxs-lookup"><span data-stu-id="6e2b4-132">IotHub Resource Id</span></span>

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

### <span data-ttu-id="6e2b4-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6e2b4-133">-Confirm</span></span>
<span data-ttu-id="6e2b4-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e2b4-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e2b4-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e2b4-135">-WhatIf</span></span>
<span data-ttu-id="6e2b4-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e2b4-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e2b4-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6e2b4-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e2b4-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e2b4-138">CommonParameters</span></span>
<span data-ttu-id="6e2b4-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e2b4-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e2b4-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e2b4-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e2b4-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6e2b4-141">INPUTS</span></span>

### <span data-ttu-id="6e2b4-142">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="6e2b4-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="6e2b4-143">System. String</span><span class="sxs-lookup"><span data-stu-id="6e2b4-143">System.String</span></span>

## <span data-ttu-id="6e2b4-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6e2b4-144">OUTPUTS</span></span>

### <span data-ttu-id="6e2b4-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6e2b4-145">System.Boolean</span></span>

## <span data-ttu-id="6e2b4-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6e2b4-146">NOTES</span></span>

## <span data-ttu-id="6e2b4-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6e2b4-147">RELATED LINKS</span></span>
