---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/set-aziothubdeviceparent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeviceParent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeviceParent.md
ms.openlocfilehash: af4b605c25ff3c35b0235612d7258be66a772c43
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955834"
---
# <span data-ttu-id="de5eb-101">Set-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="de5eb-101">Set-AzIotHubDeviceParent</span></span>

## <span data-ttu-id="de5eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de5eb-102">SYNOPSIS</span></span>
<span data-ttu-id="de5eb-103">Ustaw urządzenie nadrzędne określonego urządzenia.</span><span class="sxs-lookup"><span data-stu-id="de5eb-103">Set the parent device of the specified device.</span></span>

## <span data-ttu-id="de5eb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="de5eb-104">SYNTAX</span></span>

### <span data-ttu-id="de5eb-105">Zestaw zasobów (domyślny)</span><span class="sxs-lookup"><span data-stu-id="de5eb-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubDeviceParent [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ParentDeviceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="de5eb-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="de5eb-106">InputObjectSet</span></span>
```
Set-AzIotHubDeviceParent [-InputObject] <PSIotHub> [-DeviceId] <String> [-ParentDeviceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de5eb-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="de5eb-107">ResourceIdSet</span></span>
```
Set-AzIotHubDeviceParent [-ResourceId] <String> [-DeviceId] <String> [-ParentDeviceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de5eb-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="de5eb-108">DESCRIPTION</span></span>
<span data-ttu-id="de5eb-109">Ustaw urządzenie nadrzędne określonego urządzenia niebędące krawędzią.</span><span class="sxs-lookup"><span data-stu-id="de5eb-109">Set the parent device of the specified non-edge device.</span></span>

## <span data-ttu-id="de5eb-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="de5eb-110">EXAMPLES</span></span>

### <span data-ttu-id="de5eb-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="de5eb-111">Example 1</span></span>
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

## <span data-ttu-id="de5eb-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="de5eb-112">PARAMETERS</span></span>

### <span data-ttu-id="de5eb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de5eb-113">-DefaultProfile</span></span>
<span data-ttu-id="de5eb-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="de5eb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de5eb-115">— DeviceId</span><span class="sxs-lookup"><span data-stu-id="de5eb-115">-DeviceId</span></span>
<span data-ttu-id="de5eb-116">Identyfikator urządzenia niebędące krawędzią.</span><span class="sxs-lookup"><span data-stu-id="de5eb-116">Id of non-edge device.</span></span>

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

### <span data-ttu-id="de5eb-117">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="de5eb-117">-Force</span></span>
<span data-ttu-id="de5eb-118">Zastępuje urządzenie nadrzędne urządzenia niebędące krawędzią.</span><span class="sxs-lookup"><span data-stu-id="de5eb-118">Overwrites the non-edge device's parent device.</span></span>

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

### <span data-ttu-id="de5eb-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="de5eb-119">-InputObject</span></span>
<span data-ttu-id="de5eb-120">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="de5eb-120">IotHub object</span></span>

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

### <span data-ttu-id="de5eb-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="de5eb-121">-IotHubName</span></span>
<span data-ttu-id="de5eb-122">Nazwa Centrum Iot</span><span class="sxs-lookup"><span data-stu-id="de5eb-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="de5eb-123">-ParentDeviceId</span><span class="sxs-lookup"><span data-stu-id="de5eb-123">-ParentDeviceId</span></span>
<span data-ttu-id="de5eb-124">Identyfikator urządzenia edge.</span><span class="sxs-lookup"><span data-stu-id="de5eb-124">Id of edge device.</span></span>

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

### <span data-ttu-id="de5eb-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de5eb-125">-ResourceGroupName</span></span>
<span data-ttu-id="de5eb-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="de5eb-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="de5eb-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="de5eb-127">-ResourceId</span></span>
<span data-ttu-id="de5eb-128">Identyfikator zasobu w aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="de5eb-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="de5eb-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="de5eb-129">-Confirm</span></span>
<span data-ttu-id="de5eb-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="de5eb-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de5eb-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de5eb-131">-WhatIf</span></span>
<span data-ttu-id="de5eb-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de5eb-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="de5eb-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="de5eb-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de5eb-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de5eb-134">CommonParameters</span></span>
<span data-ttu-id="de5eb-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de5eb-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de5eb-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de5eb-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de5eb-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="de5eb-137">INPUTS</span></span>

### <span data-ttu-id="de5eb-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="de5eb-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="de5eb-139">System.String</span><span class="sxs-lookup"><span data-stu-id="de5eb-139">System.String</span></span>

## <span data-ttu-id="de5eb-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="de5eb-140">OUTPUTS</span></span>

### <span data-ttu-id="de5eb-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span><span class="sxs-lookup"><span data-stu-id="de5eb-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="de5eb-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="de5eb-142">NOTES</span></span>

## <span data-ttu-id="de5eb-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="de5eb-143">RELATED LINKS</span></span>
