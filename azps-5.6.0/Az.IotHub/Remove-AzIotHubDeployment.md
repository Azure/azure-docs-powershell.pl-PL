---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/remove-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDeployment.md
ms.openlocfilehash: a125bd402a58bc138e1fa74ec2f68d659f2a1d1c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970785"
---
# <span data-ttu-id="f1f0a-101">Remove-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="f1f0a-101">Remove-AzIotHubDeployment</span></span>

## <span data-ttu-id="f1f0a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1f0a-102">SYNOPSIS</span></span>
<span data-ttu-id="f1f0a-103">Usuń wdrożenie IoT Edge.</span><span class="sxs-lookup"><span data-stu-id="f1f0a-103">Delete an IoT Edge deployment.</span></span>

## <span data-ttu-id="f1f0a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f1f0a-104">SYNTAX</span></span>

### <span data-ttu-id="f1f0a-105">Zestaw zasobów (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f1f0a-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1f0a-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f1f0a-106">InputObjectSet</span></span>
```
Remove-AzIotHubDeployment [-InputObject] <PSIotHub> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1f0a-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f1f0a-107">ResourceIdSet</span></span>
```
Remove-AzIotHubDeployment [-ResourceId] <String> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1f0a-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="f1f0a-108">DESCRIPTION</span></span>
<span data-ttu-id="f1f0a-109">Aby https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring uzyskać więcej informacji, zobacz te informacje.</span><span class="sxs-lookup"><span data-stu-id="f1f0a-109">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring for more information.</span></span>

## <span data-ttu-id="f1f0a-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f1f0a-110">EXAMPLES</span></span>

### <span data-ttu-id="f1f0a-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f1f0a-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1"
```

<span data-ttu-id="f1f0a-112">Usuń wdrożenie IoT Edge.</span><span class="sxs-lookup"><span data-stu-id="f1f0a-112">Delete an IoT Edge deployment.</span></span>

## <span data-ttu-id="f1f0a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f1f0a-113">PARAMETERS</span></span>

### <span data-ttu-id="f1f0a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1f0a-114">-DefaultProfile</span></span>
<span data-ttu-id="f1f0a-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f1f0a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1f0a-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f1f0a-116">-InputObject</span></span>
<span data-ttu-id="f1f0a-117">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="f1f0a-117">IotHub object</span></span>

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

### <span data-ttu-id="f1f0a-118">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="f1f0a-118">-IotHubName</span></span>
<span data-ttu-id="f1f0a-119">Nazwa Centrum Iot</span><span class="sxs-lookup"><span data-stu-id="f1f0a-119">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="f1f0a-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f1f0a-120">-Name</span></span>
<span data-ttu-id="f1f0a-121">Identyfikator wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="f1f0a-121">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="f1f0a-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f1f0a-122">-PassThru</span></span>
<span data-ttu-id="f1f0a-123">Zwraca obiekt logiczny.</span><span class="sxs-lookup"><span data-stu-id="f1f0a-123">Allows to return the boolean object.</span></span>
<span data-ttu-id="f1f0a-124">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="f1f0a-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f1f0a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1f0a-125">-ResourceGroupName</span></span>
<span data-ttu-id="f1f0a-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="f1f0a-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="f1f0a-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f1f0a-127">-ResourceId</span></span>
<span data-ttu-id="f1f0a-128">Identyfikator zasobu w aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="f1f0a-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="f1f0a-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f1f0a-129">-Confirm</span></span>
<span data-ttu-id="f1f0a-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f1f0a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1f0a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1f0a-131">-WhatIf</span></span>
<span data-ttu-id="f1f0a-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1f0a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1f0a-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f1f0a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1f0a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1f0a-134">CommonParameters</span></span>
<span data-ttu-id="f1f0a-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1f0a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1f0a-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1f0a-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1f0a-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f1f0a-137">INPUTS</span></span>

### <span data-ttu-id="f1f0a-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="f1f0a-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="f1f0a-139">System.String</span><span class="sxs-lookup"><span data-stu-id="f1f0a-139">System.String</span></span>

## <span data-ttu-id="f1f0a-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f1f0a-140">OUTPUTS</span></span>

### <span data-ttu-id="f1f0a-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f1f0a-141">System.Boolean</span></span>

## <span data-ttu-id="f1f0a-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f1f0a-142">NOTES</span></span>

## <span data-ttu-id="f1f0a-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f1f0a-143">RELATED LINKS</span></span>
