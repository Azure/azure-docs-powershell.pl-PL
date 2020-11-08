---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubModule.md
ms.openlocfilehash: 3362fd6b1e60fa975277c97ea76a8e8c15ee29a4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050477"
---
# <span data-ttu-id="83907-101">Remove-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="83907-101">Remove-AzIotHubModule</span></span>

## <span data-ttu-id="83907-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="83907-102">SYNOPSIS</span></span>
<span data-ttu-id="83907-103">Usuń moduły na docelowym urządzeniu IoT w centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="83907-103">Delete module(s) on a target IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="83907-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="83907-104">SYNTAX</span></span>

### <span data-ttu-id="83907-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="83907-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubModule [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="83907-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="83907-106">InputObjectSet</span></span>
```
Remove-AzIotHubModule [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83907-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="83907-107">ResourceIdSet</span></span>
```
Remove-AzIotHubModule [-ResourceId] <String> [-DeviceId] <String> [-ModuleId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83907-108">Opis</span><span class="sxs-lookup"><span data-stu-id="83907-108">DESCRIPTION</span></span>
<span data-ttu-id="83907-109">Usuń moduły na docelowym urządzeniu IoT w centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="83907-109">Delete module(s) on a target IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="83907-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="83907-110">EXAMPLES</span></span>

### <span data-ttu-id="83907-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="83907-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -PassThru

True
```

<span data-ttu-id="83907-112">Usuwanie modułu urządzenia IoT.</span><span class="sxs-lookup"><span data-stu-id="83907-112">Delete an Iot device module.</span></span>

### <span data-ttu-id="83907-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="83907-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIotHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -PassThru

True
```

<span data-ttu-id="83907-114">Usuń wszystkie moduły urządzeń IoT.</span><span class="sxs-lookup"><span data-stu-id="83907-114">Delete all Iot device modules.</span></span>

## <span data-ttu-id="83907-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="83907-115">PARAMETERS</span></span>

### <span data-ttu-id="83907-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83907-116">-DefaultProfile</span></span>
<span data-ttu-id="83907-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="83907-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83907-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="83907-118">-DeviceId</span></span>
<span data-ttu-id="83907-119">Identyfikator urządzenia docelowego.</span><span class="sxs-lookup"><span data-stu-id="83907-119">Target Device Id.</span></span>

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

### <span data-ttu-id="83907-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="83907-120">-InputObject</span></span>
<span data-ttu-id="83907-121">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="83907-121">IotHub object</span></span>

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

### <span data-ttu-id="83907-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="83907-122">-IotHubName</span></span>
<span data-ttu-id="83907-123">Nazwa Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="83907-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="83907-124">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="83907-124">-ModuleId</span></span>
<span data-ttu-id="83907-125">Identyfikator modułu docelowego.</span><span class="sxs-lookup"><span data-stu-id="83907-125">Target Module Id.</span></span>

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

### <span data-ttu-id="83907-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="83907-126">-PassThru</span></span>
<span data-ttu-id="83907-127">Umożliwia zwrócenie obiektu logicznego.</span><span class="sxs-lookup"><span data-stu-id="83907-127">Allows to return the boolean object.</span></span>
<span data-ttu-id="83907-128">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="83907-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="83907-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83907-129">-ResourceGroupName</span></span>
<span data-ttu-id="83907-130">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="83907-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="83907-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="83907-131">-ResourceId</span></span>
<span data-ttu-id="83907-132">Identyfikator zasobu IotHub</span><span class="sxs-lookup"><span data-stu-id="83907-132">IotHub Resource Id</span></span>

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

### <span data-ttu-id="83907-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="83907-133">-Confirm</span></span>
<span data-ttu-id="83907-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83907-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83907-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83907-135">-WhatIf</span></span>
<span data-ttu-id="83907-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83907-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83907-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="83907-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83907-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83907-138">CommonParameters</span></span>
<span data-ttu-id="83907-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83907-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83907-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83907-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83907-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="83907-141">INPUTS</span></span>

### <span data-ttu-id="83907-142">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="83907-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="83907-143">System. String</span><span class="sxs-lookup"><span data-stu-id="83907-143">System.String</span></span>

## <span data-ttu-id="83907-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="83907-144">OUTPUTS</span></span>

### <span data-ttu-id="83907-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="83907-145">System.Boolean</span></span>

## <span data-ttu-id="83907-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="83907-146">NOTES</span></span>

## <span data-ttu-id="83907-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="83907-147">RELATED LINKS</span></span>
