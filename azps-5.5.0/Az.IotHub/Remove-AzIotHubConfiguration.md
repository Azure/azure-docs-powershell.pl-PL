---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubConfiguration.md
ms.openlocfilehash: 0b87bece7bca0ea3f534746dd20a163f69f21262
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200067"
---
# <span data-ttu-id="5706e-101">Remove-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="5706e-101">Remove-AzIotHubConfiguration</span></span>

## <span data-ttu-id="5706e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5706e-102">SYNOPSIS</span></span>
<span data-ttu-id="5706e-103">Usuń konfigurację urządzenia IoT.</span><span class="sxs-lookup"><span data-stu-id="5706e-103">Delete an IoT device configuration.</span></span>

## <span data-ttu-id="5706e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5706e-104">SYNTAX</span></span>

### <span data-ttu-id="5706e-105">ResourceSet (Default)</span><span class="sxs-lookup"><span data-stu-id="5706e-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubConfiguration [-ResourceGroupName] <String> [-IotHubName] <String> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5706e-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5706e-106">InputObjectSet</span></span>
```
Remove-AzIotHubConfiguration [-InputObject] <PSIotHub> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5706e-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="5706e-107">ResourceIdSet</span></span>
```
Remove-AzIotHubConfiguration [-ResourceId] <String> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5706e-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="5706e-108">DESCRIPTION</span></span>
<span data-ttu-id="5706e-109">Aby https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management uzyskać więcej informacji, zobacz.</span><span class="sxs-lookup"><span data-stu-id="5706e-109">See https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management for more information.</span></span>

## <span data-ttu-id="5706e-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5706e-110">EXAMPLES</span></span>

### <span data-ttu-id="5706e-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5706e-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1"
```

<span data-ttu-id="5706e-112">Usuń konfigurację urządzenia IoT.</span><span class="sxs-lookup"><span data-stu-id="5706e-112">Delete an IoT device configuration.</span></span>

## <span data-ttu-id="5706e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5706e-113">PARAMETERS</span></span>

### <span data-ttu-id="5706e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5706e-114">-DefaultProfile</span></span>
<span data-ttu-id="5706e-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5706e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5706e-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5706e-116">-InputObject</span></span>
<span data-ttu-id="5706e-117">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="5706e-117">IotHub object</span></span>

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

### <span data-ttu-id="5706e-118">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="5706e-118">-IotHubName</span></span>
<span data-ttu-id="5706e-119">Nazwa Centrum Iot</span><span class="sxs-lookup"><span data-stu-id="5706e-119">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="5706e-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="5706e-120">-Name</span></span>
<span data-ttu-id="5706e-121">Identyfikator konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="5706e-121">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="5706e-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5706e-122">-PassThru</span></span>
<span data-ttu-id="5706e-123">Zwraca obiekt logiczny.</span><span class="sxs-lookup"><span data-stu-id="5706e-123">Allows to return the boolean object.</span></span>
<span data-ttu-id="5706e-124">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="5706e-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5706e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5706e-125">-ResourceGroupName</span></span>
<span data-ttu-id="5706e-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="5706e-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="5706e-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5706e-127">-ResourceId</span></span>
<span data-ttu-id="5706e-128">Identyfikator zasobu w aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="5706e-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="5706e-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5706e-129">-Confirm</span></span>
<span data-ttu-id="5706e-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5706e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5706e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5706e-131">-WhatIf</span></span>
<span data-ttu-id="5706e-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5706e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5706e-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="5706e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5706e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5706e-134">CommonParameters</span></span>
<span data-ttu-id="5706e-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5706e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5706e-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5706e-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5706e-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5706e-137">INPUTS</span></span>

### <span data-ttu-id="5706e-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="5706e-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="5706e-139">System.String</span><span class="sxs-lookup"><span data-stu-id="5706e-139">System.String</span></span>

## <span data-ttu-id="5706e-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5706e-140">OUTPUTS</span></span>

### <span data-ttu-id="5706e-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5706e-141">System.Boolean</span></span>

## <span data-ttu-id="5706e-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5706e-142">NOTES</span></span>

## <span data-ttu-id="5706e-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5706e-143">RELATED LINKS</span></span>
