---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzDeviceSecurityGroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzDeviceSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzDeviceSecurityGroup.md
ms.openlocfilehash: fd15ebdcb52c167441a3278769a22c277aea6982
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503021"
---
# <span data-ttu-id="5f4b5-101">Remove-AzDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5f4b5-101">Remove-AzDeviceSecurityGroup</span></span>

## <span data-ttu-id="5f4b5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5f4b5-102">SYNOPSIS</span></span>
<span data-ttu-id="5f4b5-103">Usuń grupę zabezpieczeń urządzenia</span><span class="sxs-lookup"><span data-stu-id="5f4b5-103">Delete device security group</span></span>

## <span data-ttu-id="5f4b5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5f4b5-104">SYNTAX</span></span>

### <span data-ttu-id="5f4b5-105">ResourceIdLevelResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5f4b5-105">ResourceIdLevelResource (Default)</span></span>
```
Remove-AzDeviceSecurityGroup -Name <String> -HubResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f4b5-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="5f4b5-106">InputObject</span></span>
```
Remove-AzDeviceSecurityGroup -InputObject <PSDeviceSecurityGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f4b5-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="5f4b5-107">ResourceId</span></span>
```
Remove-AzDeviceSecurityGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f4b5-108">Opis</span><span class="sxs-lookup"><span data-stu-id="5f4b5-108">DESCRIPTION</span></span>
<span data-ttu-id="5f4b5-109">Polecenie cmdlet Remove-AzDeviceSecurityGroup usuwa grupę zabezpieczeń urządzenia zdefiniowaną w rozwiązaniu zabezpieczeń IoT.</span><span class="sxs-lookup"><span data-stu-id="5f4b5-109">The Remove-AzDeviceSecurityGroup cmdlet deletes a device security group defined in iot security solution.</span></span>

## <span data-ttu-id="5f4b5-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5f4b5-110">EXAMPLES</span></span>

### <span data-ttu-id="5f4b5-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5f4b5-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeviceSecurityGroup -Name "MySecurityGroup" -HubResourceId "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"
```

<span data-ttu-id="5f4b5-112">Usuwanie grupy zabezpieczeń urządzenia Centrum IoT z identyfikatorem zasobu "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span><span class="sxs-lookup"><span data-stu-id="5f4b5-112">Delete the device security group "MySecurityGroup" of iot hub with resource id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span></span>

## <span data-ttu-id="5f4b5-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5f4b5-113">PARAMETERS</span></span>

### <span data-ttu-id="5f4b5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f4b5-114">-DefaultProfile</span></span>
<span data-ttu-id="5f4b5-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5f4b5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f4b5-116">-HubResourceId</span><span class="sxs-lookup"><span data-stu-id="5f4b5-116">-HubResourceId</span></span>
<span data-ttu-id="5f4b5-117">Identyfikator zasobu zabezpieczeń, dla którego ma zostać wywołane polecenie.</span><span class="sxs-lookup"><span data-stu-id="5f4b5-117">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="5f4b5-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5f4b5-118">-InputObject</span></span>
<span data-ttu-id="5f4b5-119">Obiekt wejściowy.</span><span class="sxs-lookup"><span data-stu-id="5f4b5-119">Input Object.</span></span>

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

### <span data-ttu-id="5f4b5-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5f4b5-120">-Name</span></span>
<span data-ttu-id="5f4b5-121">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="5f4b5-121">Resource name.</span></span>

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

### <span data-ttu-id="5f4b5-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5f4b5-122">-PassThru</span></span>
<span data-ttu-id="5f4b5-123">Zwraca, czy operacja zakończyła się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="5f4b5-123">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="5f4b5-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5f4b5-124">-ResourceId</span></span>
<span data-ttu-id="5f4b5-125">Identyfikator zasobu zabezpieczeń, dla którego ma zostać wywołane polecenie.</span><span class="sxs-lookup"><span data-stu-id="5f4b5-125">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="5f4b5-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5f4b5-126">-Confirm</span></span>
<span data-ttu-id="5f4b5-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5f4b5-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f4b5-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f4b5-128">-WhatIf</span></span>
<span data-ttu-id="5f4b5-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5f4b5-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f4b5-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5f4b5-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f4b5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f4b5-131">CommonParameters</span></span>
<span data-ttu-id="5f4b5-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f4b5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f4b5-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5f4b5-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f4b5-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5f4b5-134">INPUTS</span></span>

### <span data-ttu-id="5f4b5-135">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5f4b5-135">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span></span>

### <span data-ttu-id="5f4b5-136">System. String</span><span class="sxs-lookup"><span data-stu-id="5f4b5-136">System.String</span></span>

## <span data-ttu-id="5f4b5-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5f4b5-137">OUTPUTS</span></span>

### <span data-ttu-id="5f4b5-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5f4b5-138">System.Boolean</span></span>

## <span data-ttu-id="5f4b5-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5f4b5-139">NOTES</span></span>

## <span data-ttu-id="5f4b5-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5f4b5-140">RELATED LINKS</span></span>
