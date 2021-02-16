---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDeployment.md
ms.openlocfilehash: f5463015b93c209c6cf8952c566e9656da2fba18
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200066"
---
# <span data-ttu-id="4cfef-101">Remove-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="4cfef-101">Remove-AzIotHubDeployment</span></span>

## <span data-ttu-id="4cfef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4cfef-102">SYNOPSIS</span></span>
<span data-ttu-id="4cfef-103">Usuń wdrożenie IoT Edge.</span><span class="sxs-lookup"><span data-stu-id="4cfef-103">Delete an IoT Edge deployment.</span></span>

## <span data-ttu-id="4cfef-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4cfef-104">SYNTAX</span></span>

### <span data-ttu-id="4cfef-105">ResourceSet (Default)</span><span class="sxs-lookup"><span data-stu-id="4cfef-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4cfef-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4cfef-106">InputObjectSet</span></span>
```
Remove-AzIotHubDeployment [-InputObject] <PSIotHub> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4cfef-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="4cfef-107">ResourceIdSet</span></span>
```
Remove-AzIotHubDeployment [-ResourceId] <String> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4cfef-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="4cfef-108">DESCRIPTION</span></span>
<span data-ttu-id="4cfef-109">Aby https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring uzyskać więcej informacji, zobacz.</span><span class="sxs-lookup"><span data-stu-id="4cfef-109">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring for more information.</span></span>

## <span data-ttu-id="4cfef-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4cfef-110">EXAMPLES</span></span>

### <span data-ttu-id="4cfef-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4cfef-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1"
```

<span data-ttu-id="4cfef-112">Usuń wdrożenie IoT Edge.</span><span class="sxs-lookup"><span data-stu-id="4cfef-112">Delete an IoT Edge deployment.</span></span>

## <span data-ttu-id="4cfef-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4cfef-113">PARAMETERS</span></span>

### <span data-ttu-id="4cfef-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cfef-114">-DefaultProfile</span></span>
<span data-ttu-id="4cfef-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4cfef-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4cfef-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4cfef-116">-InputObject</span></span>
<span data-ttu-id="4cfef-117">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="4cfef-117">IotHub object</span></span>

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

### <span data-ttu-id="4cfef-118">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="4cfef-118">-IotHubName</span></span>
<span data-ttu-id="4cfef-119">Nazwa Centrum Iot</span><span class="sxs-lookup"><span data-stu-id="4cfef-119">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="4cfef-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="4cfef-120">-Name</span></span>
<span data-ttu-id="4cfef-121">Identyfikator wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="4cfef-121">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="4cfef-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4cfef-122">-PassThru</span></span>
<span data-ttu-id="4cfef-123">Zwraca obiekt logiczny.</span><span class="sxs-lookup"><span data-stu-id="4cfef-123">Allows to return the boolean object.</span></span>
<span data-ttu-id="4cfef-124">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="4cfef-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4cfef-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4cfef-125">-ResourceGroupName</span></span>
<span data-ttu-id="4cfef-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="4cfef-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="4cfef-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4cfef-127">-ResourceId</span></span>
<span data-ttu-id="4cfef-128">Identyfikator zasobu w aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="4cfef-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="4cfef-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4cfef-129">-Confirm</span></span>
<span data-ttu-id="4cfef-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4cfef-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4cfef-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4cfef-131">-WhatIf</span></span>
<span data-ttu-id="4cfef-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4cfef-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4cfef-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="4cfef-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4cfef-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cfef-134">CommonParameters</span></span>
<span data-ttu-id="4cfef-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cfef-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cfef-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4cfef-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cfef-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4cfef-137">INPUTS</span></span>

### <span data-ttu-id="4cfef-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="4cfef-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="4cfef-139">System.String</span><span class="sxs-lookup"><span data-stu-id="4cfef-139">System.String</span></span>

## <span data-ttu-id="4cfef-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4cfef-140">OUTPUTS</span></span>

### <span data-ttu-id="4cfef-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4cfef-141">System.Boolean</span></span>

## <span data-ttu-id="4cfef-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4cfef-142">NOTES</span></span>

## <span data-ttu-id="4cfef-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4cfef-143">RELATED LINKS</span></span>
