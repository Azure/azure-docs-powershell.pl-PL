---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDevice.md
ms.openlocfilehash: 3d137f93c32b77afd29a833086ff5c55823bc104
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94224294"
---
# <span data-ttu-id="1d073-101">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="1d073-101">Remove-AzIotHubDevice</span></span>

## <span data-ttu-id="1d073-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1d073-102">SYNOPSIS</span></span>
<span data-ttu-id="1d073-103">Usuwanie urządzenia Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="1d073-103">Delete an IoT Hub device.</span></span>

## <span data-ttu-id="1d073-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1d073-104">SYNTAX</span></span>

### <span data-ttu-id="1d073-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1d073-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d073-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="1d073-106">InputObjectSet</span></span>
```
Remove-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d073-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="1d073-107">ResourceIdSet</span></span>
```
Remove-AzIotHubDevice [-ResourceId] <String> [-DeviceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d073-108">Opis</span><span class="sxs-lookup"><span data-stu-id="1d073-108">DESCRIPTION</span></span>
<span data-ttu-id="1d073-109">Usuń wszystkie urządzenia lub konkretne urządzenie z Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="1d073-109">Delete all devices or a specific device from an Iot Hub.</span></span>

## <span data-ttu-id="1d073-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1d073-110">EXAMPLES</span></span>

### <span data-ttu-id="1d073-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1d073-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="1d073-112">Usuń wszystkie urządzenia Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="1d073-112">Delete all Iot Hub devices.</span></span>

### <span data-ttu-id="1d073-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="1d073-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -PassThru

True
```

<span data-ttu-id="1d073-114">Usuwanie urządzenia Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="1d073-114">Delete an Iot Hub device.</span></span>

## <span data-ttu-id="1d073-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1d073-115">PARAMETERS</span></span>

### <span data-ttu-id="1d073-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d073-116">-DefaultProfile</span></span>
<span data-ttu-id="1d073-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1d073-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d073-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="1d073-118">-DeviceId</span></span>
<span data-ttu-id="1d073-119">Identyfikator urządzenia docelowego.</span><span class="sxs-lookup"><span data-stu-id="1d073-119">Target Device Id.</span></span>

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

### <span data-ttu-id="1d073-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1d073-120">-InputObject</span></span>
<span data-ttu-id="1d073-121">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="1d073-121">IotHub object</span></span>

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

### <span data-ttu-id="1d073-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="1d073-122">-IotHubName</span></span>
<span data-ttu-id="1d073-123">Nazwa Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="1d073-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="1d073-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1d073-124">-PassThru</span></span>
<span data-ttu-id="1d073-125">Umożliwia zwrócenie obiektu logicznego.</span><span class="sxs-lookup"><span data-stu-id="1d073-125">Allows to return the boolean object.</span></span>
<span data-ttu-id="1d073-126">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="1d073-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1d073-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d073-127">-ResourceGroupName</span></span>
<span data-ttu-id="1d073-128">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="1d073-128">Name of the Resource Group</span></span>

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

### <span data-ttu-id="1d073-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1d073-129">-ResourceId</span></span>
<span data-ttu-id="1d073-130">Identyfikator zasobu IotHub</span><span class="sxs-lookup"><span data-stu-id="1d073-130">IotHub Resource Id</span></span>

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

### <span data-ttu-id="1d073-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1d073-131">-Confirm</span></span>
<span data-ttu-id="1d073-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d073-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d073-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d073-133">-WhatIf</span></span>
<span data-ttu-id="1d073-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d073-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d073-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1d073-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d073-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d073-136">CommonParameters</span></span>
<span data-ttu-id="1d073-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d073-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d073-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d073-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d073-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1d073-139">INPUTS</span></span>

### <span data-ttu-id="1d073-140">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="1d073-140">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="1d073-141">System. String</span><span class="sxs-lookup"><span data-stu-id="1d073-141">System.String</span></span>

## <span data-ttu-id="1d073-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1d073-142">OUTPUTS</span></span>

### <span data-ttu-id="1d073-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1d073-143">System.Boolean</span></span>

## <span data-ttu-id="1d073-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1d073-144">NOTES</span></span>

## <span data-ttu-id="1d073-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1d073-145">RELATED LINKS</span></span>
