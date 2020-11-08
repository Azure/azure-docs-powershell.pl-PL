---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubdeviceparent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeviceParent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeviceParent.md
ms.openlocfilehash: 1ad24866b4e0403693ace7b53b17271786f218d1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94234718"
---
# <span data-ttu-id="9d674-101">Set-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="9d674-101">Set-AzIotHubDeviceParent</span></span>

## <span data-ttu-id="9d674-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9d674-102">SYNOPSIS</span></span>
<span data-ttu-id="9d674-103">Ustaw urządzenie nadrzędne określonego urządzenia.</span><span class="sxs-lookup"><span data-stu-id="9d674-103">Set the parent device of the specified device.</span></span>

## <span data-ttu-id="9d674-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9d674-104">SYNTAX</span></span>

### <span data-ttu-id="9d674-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9d674-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubDeviceParent [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ParentDeviceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9d674-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="9d674-106">InputObjectSet</span></span>
```
Set-AzIotHubDeviceParent [-InputObject] <PSIotHub> [-DeviceId] <String> [-ParentDeviceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d674-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="9d674-107">ResourceIdSet</span></span>
```
Set-AzIotHubDeviceParent [-ResourceId] <String> [-DeviceId] <String> [-ParentDeviceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d674-108">Opis</span><span class="sxs-lookup"><span data-stu-id="9d674-108">DESCRIPTION</span></span>
<span data-ttu-id="9d674-109">Ustaw urządzenie nadrzędne określonego urządzenia niegranicznego.</span><span class="sxs-lookup"><span data-stu-id="9d674-109">Set the parent device of the specified non-edge device.</span></span>

## <span data-ttu-id="9d674-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9d674-110">EXAMPLES</span></span>

### <span data-ttu-id="9d674-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9d674-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDeviceParent -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ParentDeviceId "myParentDevice1"

DeviceId                   : myDevice1
GenerationId               : 637148941292917073
ETag                       : "NzIyMDI4MTk3"
LastActivityTime           : 1/1/0001 12:00:00 AM
ConnectionState            : Disconnected
ConnectionStateUpdatedTime : 1/1/0001 12:00:00 AM
Status                     : Enabled
StatusReason               : 
StatusUpdatedTime          : 1/17/2020 10:15:04 PM
CloudToDeviceMessageCount  : 0
Authentication             : Sas
EdgeEnabled                : False
DeviceScope                : ms-azure-iot-edge://myParentDevice1-637176526047419634
```

## <span data-ttu-id="9d674-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9d674-112">PARAMETERS</span></span>

### <span data-ttu-id="9d674-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d674-113">-DefaultProfile</span></span>
<span data-ttu-id="9d674-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9d674-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d674-115">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="9d674-115">-DeviceId</span></span>
<span data-ttu-id="9d674-116">Identyfikator urządzenia niebędącego krawędzią.</span><span class="sxs-lookup"><span data-stu-id="9d674-116">Id of non-edge device.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d674-117">-Force</span><span class="sxs-lookup"><span data-stu-id="9d674-117">-Force</span></span>
<span data-ttu-id="9d674-118">Zastępuje nadrzędne urządzenie, które nie jest na urządzeniu nadrzędnym.</span><span class="sxs-lookup"><span data-stu-id="9d674-118">Overwrites the non-edge device's parent device.</span></span>

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

### <span data-ttu-id="9d674-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9d674-119">-InputObject</span></span>
<span data-ttu-id="9d674-120">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="9d674-120">IotHub object</span></span>

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

### <span data-ttu-id="9d674-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="9d674-121">-IotHubName</span></span>
<span data-ttu-id="9d674-122">Nazwa Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="9d674-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="9d674-123">-ParentDeviceId</span><span class="sxs-lookup"><span data-stu-id="9d674-123">-ParentDeviceId</span></span>
<span data-ttu-id="9d674-124">Identyfikator urządzenia brzegowego.</span><span class="sxs-lookup"><span data-stu-id="9d674-124">Id of edge device.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d674-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d674-125">-ResourceGroupName</span></span>
<span data-ttu-id="9d674-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="9d674-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="9d674-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9d674-127">-ResourceId</span></span>
<span data-ttu-id="9d674-128">Identyfikator zasobu IotHub</span><span class="sxs-lookup"><span data-stu-id="9d674-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="9d674-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9d674-129">-Confirm</span></span>
<span data-ttu-id="9d674-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d674-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d674-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d674-131">-WhatIf</span></span>
<span data-ttu-id="9d674-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d674-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9d674-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9d674-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d674-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d674-134">CommonParameters</span></span>
<span data-ttu-id="9d674-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d674-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d674-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d674-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d674-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9d674-137">INPUTS</span></span>

### <span data-ttu-id="9d674-138">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="9d674-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="9d674-139">System. String</span><span class="sxs-lookup"><span data-stu-id="9d674-139">System.String</span></span>

## <span data-ttu-id="9d674-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9d674-140">OUTPUTS</span></span>

### <span data-ttu-id="9d674-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span><span class="sxs-lookup"><span data-stu-id="9d674-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="9d674-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9d674-142">NOTES</span></span>

## <span data-ttu-id="9d674-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9d674-143">RELATED LINKS</span></span>
