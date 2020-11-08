---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubdeviceparent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeviceParent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeviceParent.md
ms.openlocfilehash: 1ad24866b4e0403693ace7b53b17271786f218d1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050381"
---
# <span data-ttu-id="d7a9b-101">Set-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="d7a9b-101">Set-AzIotHubDeviceParent</span></span>

## <span data-ttu-id="d7a9b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d7a9b-102">SYNOPSIS</span></span>
<span data-ttu-id="d7a9b-103">Ustaw urządzenie nadrzędne określonego urządzenia.</span><span class="sxs-lookup"><span data-stu-id="d7a9b-103">Set the parent device of the specified device.</span></span>

## <span data-ttu-id="d7a9b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d7a9b-104">SYNTAX</span></span>

### <span data-ttu-id="d7a9b-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d7a9b-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubDeviceParent [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ParentDeviceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d7a9b-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d7a9b-106">InputObjectSet</span></span>
```
Set-AzIotHubDeviceParent [-InputObject] <PSIotHub> [-DeviceId] <String> [-ParentDeviceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7a9b-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d7a9b-107">ResourceIdSet</span></span>
```
Set-AzIotHubDeviceParent [-ResourceId] <String> [-DeviceId] <String> [-ParentDeviceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7a9b-108">Opis</span><span class="sxs-lookup"><span data-stu-id="d7a9b-108">DESCRIPTION</span></span>
<span data-ttu-id="d7a9b-109">Ustaw urządzenie nadrzędne określonego urządzenia niegranicznego.</span><span class="sxs-lookup"><span data-stu-id="d7a9b-109">Set the parent device of the specified non-edge device.</span></span>

## <span data-ttu-id="d7a9b-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d7a9b-110">EXAMPLES</span></span>

### <span data-ttu-id="d7a9b-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d7a9b-111">Example 1</span></span>
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

## <span data-ttu-id="d7a9b-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d7a9b-112">PARAMETERS</span></span>

### <span data-ttu-id="d7a9b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7a9b-113">-DefaultProfile</span></span>
<span data-ttu-id="d7a9b-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d7a9b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7a9b-115">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="d7a9b-115">-DeviceId</span></span>
<span data-ttu-id="d7a9b-116">Identyfikator urządzenia niebędącego krawędzią.</span><span class="sxs-lookup"><span data-stu-id="d7a9b-116">Id of non-edge device.</span></span>

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

### <span data-ttu-id="d7a9b-117">-Force</span><span class="sxs-lookup"><span data-stu-id="d7a9b-117">-Force</span></span>
<span data-ttu-id="d7a9b-118">Zastępuje nadrzędne urządzenie, które nie jest na urządzeniu nadrzędnym.</span><span class="sxs-lookup"><span data-stu-id="d7a9b-118">Overwrites the non-edge device's parent device.</span></span>

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

### <span data-ttu-id="d7a9b-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d7a9b-119">-InputObject</span></span>
<span data-ttu-id="d7a9b-120">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="d7a9b-120">IotHub object</span></span>

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

### <span data-ttu-id="d7a9b-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="d7a9b-121">-IotHubName</span></span>
<span data-ttu-id="d7a9b-122">Nazwa Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="d7a9b-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="d7a9b-123">-ParentDeviceId</span><span class="sxs-lookup"><span data-stu-id="d7a9b-123">-ParentDeviceId</span></span>
<span data-ttu-id="d7a9b-124">Identyfikator urządzenia brzegowego.</span><span class="sxs-lookup"><span data-stu-id="d7a9b-124">Id of edge device.</span></span>

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

### <span data-ttu-id="d7a9b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7a9b-125">-ResourceGroupName</span></span>
<span data-ttu-id="d7a9b-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="d7a9b-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="d7a9b-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d7a9b-127">-ResourceId</span></span>
<span data-ttu-id="d7a9b-128">Identyfikator zasobu IotHub</span><span class="sxs-lookup"><span data-stu-id="d7a9b-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="d7a9b-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d7a9b-129">-Confirm</span></span>
<span data-ttu-id="d7a9b-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7a9b-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7a9b-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7a9b-131">-WhatIf</span></span>
<span data-ttu-id="d7a9b-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7a9b-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d7a9b-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d7a9b-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7a9b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7a9b-134">CommonParameters</span></span>
<span data-ttu-id="d7a9b-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7a9b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7a9b-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7a9b-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7a9b-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d7a9b-137">INPUTS</span></span>

### <span data-ttu-id="d7a9b-138">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="d7a9b-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="d7a9b-139">System. String</span><span class="sxs-lookup"><span data-stu-id="d7a9b-139">System.String</span></span>

## <span data-ttu-id="d7a9b-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d7a9b-140">OUTPUTS</span></span>

### <span data-ttu-id="d7a9b-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span><span class="sxs-lookup"><span data-stu-id="d7a9b-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="d7a9b-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d7a9b-142">NOTES</span></span>

## <span data-ttu-id="d7a9b-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d7a9b-143">RELATED LINKS</span></span>
