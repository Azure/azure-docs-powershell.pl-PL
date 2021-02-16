---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzDeviceSecurityGroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzDeviceSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzDeviceSecurityGroup.md
ms.openlocfilehash: fd15ebdcb52c167441a3278769a22c277aea6982
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242378"
---
# <span data-ttu-id="6a1ea-101">Remove-AzDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="6a1ea-101">Remove-AzDeviceSecurityGroup</span></span>

## <span data-ttu-id="6a1ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a1ea-102">SYNOPSIS</span></span>
<span data-ttu-id="6a1ea-103">Usuwanie grupy zabezpieczeń urządzenia</span><span class="sxs-lookup"><span data-stu-id="6a1ea-103">Delete device security group</span></span>

## <span data-ttu-id="6a1ea-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6a1ea-104">SYNTAX</span></span>

### <span data-ttu-id="6a1ea-105">ResourceIdLevelResource (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="6a1ea-105">ResourceIdLevelResource (Default)</span></span>
```
Remove-AzDeviceSecurityGroup -Name <String> -HubResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a1ea-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="6a1ea-106">InputObject</span></span>
```
Remove-AzDeviceSecurityGroup -InputObject <PSDeviceSecurityGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a1ea-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="6a1ea-107">ResourceId</span></span>
```
Remove-AzDeviceSecurityGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a1ea-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="6a1ea-108">DESCRIPTION</span></span>
<span data-ttu-id="6a1ea-109">Polecenie Remove-AzDeviceSecurityGroup usuwa grupę zabezpieczeń urządzenia zdefiniowaną w rozwiązaniu zabezpieczeń systemu iot.</span><span class="sxs-lookup"><span data-stu-id="6a1ea-109">The Remove-AzDeviceSecurityGroup cmdlet deletes a device security group defined in iot security solution.</span></span>

## <span data-ttu-id="6a1ea-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6a1ea-110">EXAMPLES</span></span>

### <span data-ttu-id="6a1ea-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6a1ea-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeviceSecurityGroup -Name "MySecurityGroup" -HubResourceId "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"
```

<span data-ttu-id="6a1ea-112">Usuń grupę zabezpieczeń urządzenia "MySecurityGroup" centrum iot z identyfikatorem zasobu "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHubs"</span><span class="sxs-lookup"><span data-stu-id="6a1ea-112">Delete the device security group "MySecurityGroup" of iot hub with resource id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span></span>

## <span data-ttu-id="6a1ea-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6a1ea-113">PARAMETERS</span></span>

### <span data-ttu-id="6a1ea-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a1ea-114">-DefaultProfile</span></span>
<span data-ttu-id="6a1ea-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6a1ea-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a1ea-116">-HubResourceId</span><span class="sxs-lookup"><span data-stu-id="6a1ea-116">-HubResourceId</span></span>
<span data-ttu-id="6a1ea-117">Identyfikator zasobu zabezpieczeń, dla którego chcesz wywołać polecenie.</span><span class="sxs-lookup"><span data-stu-id="6a1ea-117">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a1ea-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6a1ea-118">-InputObject</span></span>
<span data-ttu-id="6a1ea-119">Obiekt Input.</span><span class="sxs-lookup"><span data-stu-id="6a1ea-119">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a1ea-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="6a1ea-120">-Name</span></span>
<span data-ttu-id="6a1ea-121">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="6a1ea-121">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a1ea-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6a1ea-122">-PassThru</span></span>
<span data-ttu-id="6a1ea-123">Sprawdź, czy operacja się powiedzie.</span><span class="sxs-lookup"><span data-stu-id="6a1ea-123">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="6a1ea-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6a1ea-124">-ResourceId</span></span>
<span data-ttu-id="6a1ea-125">Identyfikator zasobu zabezpieczeń, dla którego chcesz wywołać polecenie.</span><span class="sxs-lookup"><span data-stu-id="6a1ea-125">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a1ea-126">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6a1ea-126">-Confirm</span></span>
<span data-ttu-id="6a1ea-127">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6a1ea-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a1ea-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a1ea-128">-WhatIf</span></span>
<span data-ttu-id="6a1ea-129">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a1ea-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a1ea-130">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="6a1ea-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a1ea-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a1ea-131">CommonParameters</span></span>
<span data-ttu-id="6a1ea-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a1ea-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a1ea-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6a1ea-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a1ea-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6a1ea-134">INPUTS</span></span>

### <span data-ttu-id="6a1ea-135">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="6a1ea-135">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span></span>

### <span data-ttu-id="6a1ea-136">System.String</span><span class="sxs-lookup"><span data-stu-id="6a1ea-136">System.String</span></span>

## <span data-ttu-id="6a1ea-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6a1ea-137">OUTPUTS</span></span>

### <span data-ttu-id="6a1ea-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6a1ea-138">System.Boolean</span></span>

## <span data-ttu-id="6a1ea-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6a1ea-139">NOTES</span></span>

## <span data-ttu-id="6a1ea-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6a1ea-140">RELATED LINKS</span></span>
