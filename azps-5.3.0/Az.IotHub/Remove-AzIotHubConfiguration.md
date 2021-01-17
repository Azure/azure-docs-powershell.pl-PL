---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubConfiguration.md
ms.openlocfilehash: 0b87bece7bca0ea3f534746dd20a163f69f21262
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386743"
---
# <span data-ttu-id="90a96-101">Remove-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="90a96-101">Remove-AzIotHubConfiguration</span></span>

## <span data-ttu-id="90a96-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="90a96-102">SYNOPSIS</span></span>
<span data-ttu-id="90a96-103">Usuwanie konfiguracji urządzenia IoT.</span><span class="sxs-lookup"><span data-stu-id="90a96-103">Delete an IoT device configuration.</span></span>

## <span data-ttu-id="90a96-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="90a96-104">SYNTAX</span></span>

### <span data-ttu-id="90a96-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="90a96-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubConfiguration [-ResourceGroupName] <String> [-IotHubName] <String> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90a96-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="90a96-106">InputObjectSet</span></span>
```
Remove-AzIotHubConfiguration [-InputObject] <PSIotHub> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90a96-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="90a96-107">ResourceIdSet</span></span>
```
Remove-AzIotHubConfiguration [-ResourceId] <String> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90a96-108">Opis</span><span class="sxs-lookup"><span data-stu-id="90a96-108">DESCRIPTION</span></span>
<span data-ttu-id="90a96-109"> https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-managementAby uzyskać więcej informacji, zobacz.</span><span class="sxs-lookup"><span data-stu-id="90a96-109">See https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management for more information.</span></span>

## <span data-ttu-id="90a96-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="90a96-110">EXAMPLES</span></span>

### <span data-ttu-id="90a96-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="90a96-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1"
```

<span data-ttu-id="90a96-112">Usuwanie konfiguracji urządzenia IoT.</span><span class="sxs-lookup"><span data-stu-id="90a96-112">Delete an IoT device configuration.</span></span>

## <span data-ttu-id="90a96-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="90a96-113">PARAMETERS</span></span>

### <span data-ttu-id="90a96-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90a96-114">-DefaultProfile</span></span>
<span data-ttu-id="90a96-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="90a96-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90a96-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="90a96-116">-InputObject</span></span>
<span data-ttu-id="90a96-117">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="90a96-117">IotHub object</span></span>

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

### <span data-ttu-id="90a96-118">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="90a96-118">-IotHubName</span></span>
<span data-ttu-id="90a96-119">Nazwa Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="90a96-119">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="90a96-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="90a96-120">-Name</span></span>
<span data-ttu-id="90a96-121">Identyfikator konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="90a96-121">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="90a96-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="90a96-122">-PassThru</span></span>
<span data-ttu-id="90a96-123">Umożliwia zwrócenie obiektu logicznego.</span><span class="sxs-lookup"><span data-stu-id="90a96-123">Allows to return the boolean object.</span></span>
<span data-ttu-id="90a96-124">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="90a96-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="90a96-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90a96-125">-ResourceGroupName</span></span>
<span data-ttu-id="90a96-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="90a96-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="90a96-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="90a96-127">-ResourceId</span></span>
<span data-ttu-id="90a96-128">Identyfikator zasobu IotHub</span><span class="sxs-lookup"><span data-stu-id="90a96-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="90a96-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="90a96-129">-Confirm</span></span>
<span data-ttu-id="90a96-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90a96-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90a96-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90a96-131">-WhatIf</span></span>
<span data-ttu-id="90a96-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90a96-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90a96-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="90a96-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90a96-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90a96-134">CommonParameters</span></span>
<span data-ttu-id="90a96-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90a96-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90a96-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90a96-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90a96-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="90a96-137">INPUTS</span></span>

### <span data-ttu-id="90a96-138">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="90a96-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="90a96-139">System. String</span><span class="sxs-lookup"><span data-stu-id="90a96-139">System.String</span></span>

## <span data-ttu-id="90a96-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="90a96-140">OUTPUTS</span></span>

### <span data-ttu-id="90a96-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="90a96-141">System.Boolean</span></span>

## <span data-ttu-id="90a96-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="90a96-142">NOTES</span></span>

## <span data-ttu-id="90a96-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="90a96-143">RELATED LINKS</span></span>
