---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/remove-aziothubdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDevice.md
ms.openlocfilehash: 15a8f9aa8ed3c0746b402b29967999d395794fc1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007882"
---
# <span data-ttu-id="209f0-101">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="209f0-101">Remove-AzIotHubDevice</span></span>

## <span data-ttu-id="209f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="209f0-102">SYNOPSIS</span></span>
<span data-ttu-id="209f0-103">Usuń urządzenie Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="209f0-103">Delete an IoT Hub device.</span></span>

## <span data-ttu-id="209f0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="209f0-104">SYNTAX</span></span>

### <span data-ttu-id="209f0-105">Zestaw zasobów (domyślny)</span><span class="sxs-lookup"><span data-stu-id="209f0-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="209f0-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="209f0-106">InputObjectSet</span></span>
```
Remove-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="209f0-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="209f0-107">ResourceIdSet</span></span>
```
Remove-AzIotHubDevice [-ResourceId] <String> [-DeviceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="209f0-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="209f0-108">DESCRIPTION</span></span>
<span data-ttu-id="209f0-109">Usuń wszystkie urządzenia lub określone urządzenie z centrum Iot.</span><span class="sxs-lookup"><span data-stu-id="209f0-109">Delete all devices or a specific device from an Iot Hub.</span></span>

## <span data-ttu-id="209f0-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="209f0-110">EXAMPLES</span></span>

### <span data-ttu-id="209f0-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="209f0-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="209f0-112">Usuń wszystkie urządzenia Centrum Iot.</span><span class="sxs-lookup"><span data-stu-id="209f0-112">Delete all Iot Hub devices.</span></span>

### <span data-ttu-id="209f0-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="209f0-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -PassThru

True
```

<span data-ttu-id="209f0-114">Usuń urządzenie Centrum Iot.</span><span class="sxs-lookup"><span data-stu-id="209f0-114">Delete an Iot Hub device.</span></span>

## <span data-ttu-id="209f0-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="209f0-115">PARAMETERS</span></span>

### <span data-ttu-id="209f0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="209f0-116">-DefaultProfile</span></span>
<span data-ttu-id="209f0-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="209f0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="209f0-118">— DeviceId</span><span class="sxs-lookup"><span data-stu-id="209f0-118">-DeviceId</span></span>
<span data-ttu-id="209f0-119">Identyfikator urządzenia docelowego.</span><span class="sxs-lookup"><span data-stu-id="209f0-119">Target Device Id.</span></span>

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

### <span data-ttu-id="209f0-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="209f0-120">-InputObject</span></span>
<span data-ttu-id="209f0-121">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="209f0-121">IotHub object</span></span>

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

### <span data-ttu-id="209f0-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="209f0-122">-IotHubName</span></span>
<span data-ttu-id="209f0-123">Nazwa Centrum Iot</span><span class="sxs-lookup"><span data-stu-id="209f0-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="209f0-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="209f0-124">-PassThru</span></span>
<span data-ttu-id="209f0-125">Zwraca obiekt logiczny.</span><span class="sxs-lookup"><span data-stu-id="209f0-125">Allows to return the boolean object.</span></span>
<span data-ttu-id="209f0-126">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="209f0-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="209f0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="209f0-127">-ResourceGroupName</span></span>
<span data-ttu-id="209f0-128">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="209f0-128">Name of the Resource Group</span></span>

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

### <span data-ttu-id="209f0-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="209f0-129">-ResourceId</span></span>
<span data-ttu-id="209f0-130">Identyfikator zasobu w aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="209f0-130">IotHub Resource Id</span></span>

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

### <span data-ttu-id="209f0-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="209f0-131">-Confirm</span></span>
<span data-ttu-id="209f0-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="209f0-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="209f0-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="209f0-133">-WhatIf</span></span>
<span data-ttu-id="209f0-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="209f0-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="209f0-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="209f0-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="209f0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="209f0-136">CommonParameters</span></span>
<span data-ttu-id="209f0-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="209f0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="209f0-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="209f0-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="209f0-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="209f0-139">INPUTS</span></span>

### <span data-ttu-id="209f0-140">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="209f0-140">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="209f0-141">System.String</span><span class="sxs-lookup"><span data-stu-id="209f0-141">System.String</span></span>

## <span data-ttu-id="209f0-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="209f0-142">OUTPUTS</span></span>

### <span data-ttu-id="209f0-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="209f0-143">System.Boolean</span></span>

## <span data-ttu-id="209f0-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="209f0-144">NOTES</span></span>

## <span data-ttu-id="209f0-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="209f0-145">RELATED LINKS</span></span>
