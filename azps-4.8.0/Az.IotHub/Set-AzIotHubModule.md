---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubModule.md
ms.openlocfilehash: c88ee9af5d03b50ed80bf677ccff6e7236668756
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94220860"
---
# <span data-ttu-id="35a0a-101">Set-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="35a0a-101">Set-AzIotHubModule</span></span>

## <span data-ttu-id="35a0a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="35a0a-102">SYNOPSIS</span></span>
<span data-ttu-id="35a0a-103">Zaktualizuj moduł na docelowym urządzeniu IoT w centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="35a0a-103">Update a module on a target IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="35a0a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="35a0a-104">SYNTAX</span></span>

### <span data-ttu-id="35a0a-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="35a0a-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubModule [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String> [-ModuleId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="35a0a-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="35a0a-106">InputObjectSet</span></span>
```
Set-AzIotHubModule [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="35a0a-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="35a0a-107">ResourceIdSet</span></span>
```
Set-AzIotHubModule [-ResourceId] <String> [-DeviceId] <String> [-ModuleId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="35a0a-108">Opis</span><span class="sxs-lookup"><span data-stu-id="35a0a-108">DESCRIPTION</span></span>
<span data-ttu-id="35a0a-109">Zaktualizuj moduł na docelowym urządzeniu IoT w centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="35a0a-109">Update a module on a target IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="35a0a-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="35a0a-110">EXAMPLES</span></span>

### <span data-ttu-id="35a0a-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="35a0a-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -AuthMethod "shared_private_key"

ModuleId                   : myModule1
DeviceId                   : myDevice1
GenerationId               : 637148941292917073
ETag                       : "NzIyMDI4MTk3"
LastActivityTime           : 1/1/0001 12:00:00 AM
ConnectionState            : Disconnected
ConnectionStateUpdatedTime : 1/1/0001 12:00:00 AM
CloudToDeviceMessageCount  : 0
Authentication             : Sas
ManagedBy                  : 
```

<span data-ttu-id="35a0a-112">Aktualizowanie typu autoryzacji modułu urządzenia IoT.</span><span class="sxs-lookup"><span data-stu-id="35a0a-112">Update authorization type of an Iot device module.</span></span>

## <span data-ttu-id="35a0a-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="35a0a-113">PARAMETERS</span></span>

### <span data-ttu-id="35a0a-114">-AuthMethod</span><span class="sxs-lookup"><span data-stu-id="35a0a-114">-AuthMethod</span></span>
<span data-ttu-id="35a0a-115">Typ autoryzacji, z którym ma zostać utworzony obiekt.</span><span class="sxs-lookup"><span data-stu-id="35a0a-115">The authorization type an entity is to be created with.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceAuthType
Parameter Sets: (All)
Aliases:
Accepted values: shared_private_key, x509_thumbprint, x509_ca

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35a0a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35a0a-116">-DefaultProfile</span></span>
<span data-ttu-id="35a0a-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="35a0a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35a0a-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="35a0a-118">-DeviceId</span></span>
<span data-ttu-id="35a0a-119">Identyfikator urządzenia docelowego.</span><span class="sxs-lookup"><span data-stu-id="35a0a-119">Target Device Id.</span></span>

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

### <span data-ttu-id="35a0a-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="35a0a-120">-InputObject</span></span>
<span data-ttu-id="35a0a-121">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="35a0a-121">IotHub object</span></span>

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

### <span data-ttu-id="35a0a-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="35a0a-122">-IotHubName</span></span>
<span data-ttu-id="35a0a-123">Nazwa Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="35a0a-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="35a0a-124">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="35a0a-124">-ModuleId</span></span>
<span data-ttu-id="35a0a-125">Identyfikator modułu docelowego.</span><span class="sxs-lookup"><span data-stu-id="35a0a-125">Target Module Id.</span></span>

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

### <span data-ttu-id="35a0a-126">-PrimaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="35a0a-126">-PrimaryThumbprint</span></span>
<span data-ttu-id="35a0a-127">Jawny odcisk palca certyfikatu z podpisem własnym, który ma być używany dla klucza podstawowego.</span><span class="sxs-lookup"><span data-stu-id="35a0a-127">Explicit self-signed certificate thumbprint to use for primary key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35a0a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35a0a-128">-ResourceGroupName</span></span>
<span data-ttu-id="35a0a-129">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="35a0a-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="35a0a-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="35a0a-130">-ResourceId</span></span>
<span data-ttu-id="35a0a-131">Identyfikator zasobu IotHub</span><span class="sxs-lookup"><span data-stu-id="35a0a-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="35a0a-132">-SecondaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="35a0a-132">-SecondaryThumbprint</span></span>
<span data-ttu-id="35a0a-133">Jawny odcisk palca certyfikatu z podpisem własnym, który ma być używany dla klucza pomocniczego.</span><span class="sxs-lookup"><span data-stu-id="35a0a-133">Explicit self-signed certificate thumbprint to use for secondary key.</span></span>

```yaml
Type:System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35a0a-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="35a0a-134">-Confirm</span></span>
<span data-ttu-id="35a0a-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35a0a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35a0a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35a0a-136">-WhatIf</span></span>
<span data-ttu-id="35a0a-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35a0a-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35a0a-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="35a0a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35a0a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35a0a-139">CommonParameters</span></span>
<span data-ttu-id="35a0a-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35a0a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35a0a-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35a0a-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35a0a-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="35a0a-142">INPUTS</span></span>

### <span data-ttu-id="35a0a-143">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="35a0a-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="35a0a-144">System. String</span><span class="sxs-lookup"><span data-stu-id="35a0a-144">System.String</span></span>

## <span data-ttu-id="35a0a-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="35a0a-145">OUTPUTS</span></span>

### <span data-ttu-id="35a0a-146">Microsoft. Azure. Commands. Management. IotHub. models. PSModule</span><span class="sxs-lookup"><span data-stu-id="35a0a-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSModule</span></span>

## <span data-ttu-id="35a0a-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="35a0a-147">NOTES</span></span>

## <span data-ttu-id="35a0a-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="35a0a-148">RELATED LINKS</span></span>