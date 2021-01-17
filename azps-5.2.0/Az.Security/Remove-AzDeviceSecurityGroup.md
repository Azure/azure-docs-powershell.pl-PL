---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzDeviceSecurityGroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzDeviceSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzDeviceSecurityGroup.md
ms.openlocfilehash: fd15ebdcb52c167441a3278769a22c277aea6982
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98337306"
---
# <span data-ttu-id="f9ba4-101">Remove-AzDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f9ba4-101">Remove-AzDeviceSecurityGroup</span></span>

## <span data-ttu-id="f9ba4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f9ba4-102">SYNOPSIS</span></span>
<span data-ttu-id="f9ba4-103">Usuń grupę zabezpieczeń urządzenia</span><span class="sxs-lookup"><span data-stu-id="f9ba4-103">Delete device security group</span></span>

## <span data-ttu-id="f9ba4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f9ba4-104">SYNTAX</span></span>

### <span data-ttu-id="f9ba4-105">ResourceIdLevelResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f9ba4-105">ResourceIdLevelResource (Default)</span></span>
```
Remove-AzDeviceSecurityGroup -Name <String> -HubResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9ba4-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="f9ba4-106">InputObject</span></span>
```
Remove-AzDeviceSecurityGroup -InputObject <PSDeviceSecurityGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9ba4-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="f9ba4-107">ResourceId</span></span>
```
Remove-AzDeviceSecurityGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9ba4-108">Opis</span><span class="sxs-lookup"><span data-stu-id="f9ba4-108">DESCRIPTION</span></span>
<span data-ttu-id="f9ba4-109">Polecenie cmdlet Remove-AzDeviceSecurityGroup usuwa grupę zabezpieczeń urządzenia zdefiniowaną w rozwiązaniu zabezpieczeń IoT.</span><span class="sxs-lookup"><span data-stu-id="f9ba4-109">The Remove-AzDeviceSecurityGroup cmdlet deletes a device security group defined in iot security solution.</span></span>

## <span data-ttu-id="f9ba4-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f9ba4-110">EXAMPLES</span></span>

### <span data-ttu-id="f9ba4-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f9ba4-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeviceSecurityGroup -Name "MySecurityGroup" -HubResourceId "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"
```

<span data-ttu-id="f9ba4-112">Usuwanie grupy zabezpieczeń urządzenia Centrum IoT z identyfikatorem zasobu "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span><span class="sxs-lookup"><span data-stu-id="f9ba4-112">Delete the device security group "MySecurityGroup" of iot hub with resource id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span></span>

## <span data-ttu-id="f9ba4-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f9ba4-113">PARAMETERS</span></span>

### <span data-ttu-id="f9ba4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9ba4-114">-DefaultProfile</span></span>
<span data-ttu-id="f9ba4-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f9ba4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9ba4-116">-HubResourceId</span><span class="sxs-lookup"><span data-stu-id="f9ba4-116">-HubResourceId</span></span>
<span data-ttu-id="f9ba4-117">Identyfikator zasobu zabezpieczeń, dla którego ma zostać wywołane polecenie.</span><span class="sxs-lookup"><span data-stu-id="f9ba4-117">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="f9ba4-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f9ba4-118">-InputObject</span></span>
<span data-ttu-id="f9ba4-119">Obiekt wejściowy.</span><span class="sxs-lookup"><span data-stu-id="f9ba4-119">Input Object.</span></span>

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

### <span data-ttu-id="f9ba4-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f9ba4-120">-Name</span></span>
<span data-ttu-id="f9ba4-121">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="f9ba4-121">Resource name.</span></span>

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

### <span data-ttu-id="f9ba4-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f9ba4-122">-PassThru</span></span>
<span data-ttu-id="f9ba4-123">Zwraca, czy operacja zakończyła się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="f9ba4-123">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="f9ba4-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f9ba4-124">-ResourceId</span></span>
<span data-ttu-id="f9ba4-125">Identyfikator zasobu zabezpieczeń, dla którego ma zostać wywołane polecenie.</span><span class="sxs-lookup"><span data-stu-id="f9ba4-125">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="f9ba4-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f9ba4-126">-Confirm</span></span>
<span data-ttu-id="f9ba4-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f9ba4-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9ba4-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9ba4-128">-WhatIf</span></span>
<span data-ttu-id="f9ba4-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f9ba4-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9ba4-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f9ba4-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9ba4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9ba4-131">CommonParameters</span></span>
<span data-ttu-id="f9ba4-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9ba4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9ba4-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f9ba4-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9ba4-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f9ba4-134">INPUTS</span></span>

### <span data-ttu-id="f9ba4-135">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f9ba4-135">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span></span>

### <span data-ttu-id="f9ba4-136">System. String</span><span class="sxs-lookup"><span data-stu-id="f9ba4-136">System.String</span></span>

## <span data-ttu-id="f9ba4-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f9ba4-137">OUTPUTS</span></span>

### <span data-ttu-id="f9ba4-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f9ba4-138">System.Boolean</span></span>

## <span data-ttu-id="f9ba4-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f9ba4-139">NOTES</span></span>

## <span data-ttu-id="f9ba4-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f9ba4-140">RELATED LINKS</span></span>
