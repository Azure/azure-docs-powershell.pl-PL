---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Remove-AzDeviceSecurityGroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzDeviceSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzDeviceSecurityGroup.md
ms.openlocfilehash: 302e4b096c3a41c6dd5a57a87d23bf15b83c96a9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984138"
---
# <span data-ttu-id="a63d4-101">Remove-AzDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a63d4-101">Remove-AzDeviceSecurityGroup</span></span>

## <span data-ttu-id="a63d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a63d4-102">SYNOPSIS</span></span>
<span data-ttu-id="a63d4-103">Usuwanie grupy zabezpieczeń urządzenia</span><span class="sxs-lookup"><span data-stu-id="a63d4-103">Delete device security group</span></span>

## <span data-ttu-id="a63d4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a63d4-104">SYNTAX</span></span>

### <span data-ttu-id="a63d4-105">ResourceIdLevelResource (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="a63d4-105">ResourceIdLevelResource (Default)</span></span>
```
Remove-AzDeviceSecurityGroup -Name <String> -HubResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a63d4-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="a63d4-106">InputObject</span></span>
```
Remove-AzDeviceSecurityGroup -InputObject <PSDeviceSecurityGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a63d4-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a63d4-107">ResourceId</span></span>
```
Remove-AzDeviceSecurityGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a63d4-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="a63d4-108">DESCRIPTION</span></span>
<span data-ttu-id="a63d4-109">Polecenie Remove-AzDeviceSecurityGroup usuwa grupę zabezpieczeń urządzenia zdefiniowaną w rozwiązaniu zabezpieczeń systemu iot.</span><span class="sxs-lookup"><span data-stu-id="a63d4-109">The Remove-AzDeviceSecurityGroup cmdlet deletes a device security group defined in iot security solution.</span></span>

## <span data-ttu-id="a63d4-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a63d4-110">EXAMPLES</span></span>

### <span data-ttu-id="a63d4-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a63d4-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeviceSecurityGroup -Name "MySecurityGroup" -HubResourceId "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"
```

<span data-ttu-id="a63d4-112">Usuń grupę zabezpieczeń urządzenia "MySecurityGroup" centrum iot z identyfikatorem zasobu "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHubs"</span><span class="sxs-lookup"><span data-stu-id="a63d4-112">Delete the device security group "MySecurityGroup" of iot hub with resource id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span></span>

## <span data-ttu-id="a63d4-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a63d4-113">PARAMETERS</span></span>

### <span data-ttu-id="a63d4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a63d4-114">-DefaultProfile</span></span>
<span data-ttu-id="a63d4-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a63d4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a63d4-116">-HubResourceId</span><span class="sxs-lookup"><span data-stu-id="a63d4-116">-HubResourceId</span></span>
<span data-ttu-id="a63d4-117">Identyfikator zasobu zabezpieczeń, dla którego chcesz wywołać polecenie.</span><span class="sxs-lookup"><span data-stu-id="a63d4-117">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="a63d4-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a63d4-118">-InputObject</span></span>
<span data-ttu-id="a63d4-119">Obiekt Input.</span><span class="sxs-lookup"><span data-stu-id="a63d4-119">Input Object.</span></span>

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

### <span data-ttu-id="a63d4-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a63d4-120">-Name</span></span>
<span data-ttu-id="a63d4-121">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="a63d4-121">Resource name.</span></span>

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

### <span data-ttu-id="a63d4-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a63d4-122">-PassThru</span></span>
<span data-ttu-id="a63d4-123">Sprawdź, czy operacja się powiedzie.</span><span class="sxs-lookup"><span data-stu-id="a63d4-123">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="a63d4-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a63d4-124">-ResourceId</span></span>
<span data-ttu-id="a63d4-125">Identyfikator zasobu zabezpieczeń, dla którego chcesz wywołać polecenie.</span><span class="sxs-lookup"><span data-stu-id="a63d4-125">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="a63d4-126">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a63d4-126">-Confirm</span></span>
<span data-ttu-id="a63d4-127">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a63d4-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a63d4-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a63d4-128">-WhatIf</span></span>
<span data-ttu-id="a63d4-129">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a63d4-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a63d4-130">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a63d4-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a63d4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a63d4-131">CommonParameters</span></span>
<span data-ttu-id="a63d4-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a63d4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a63d4-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a63d4-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a63d4-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a63d4-134">INPUTS</span></span>

### <span data-ttu-id="a63d4-135">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a63d4-135">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span></span>

### <span data-ttu-id="a63d4-136">System.String</span><span class="sxs-lookup"><span data-stu-id="a63d4-136">System.String</span></span>

## <span data-ttu-id="a63d4-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a63d4-137">OUTPUTS</span></span>

### <span data-ttu-id="a63d4-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a63d4-138">System.Boolean</span></span>

## <span data-ttu-id="a63d4-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a63d4-139">NOTES</span></span>

## <span data-ttu-id="a63d4-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a63d4-140">RELATED LINKS</span></span>
