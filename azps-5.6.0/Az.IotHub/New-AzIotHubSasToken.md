---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/new-aziothubsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubSasToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubSasToken.md
ms.openlocfilehash: 39b936f6b9ec4bb133ecc6510963207c5e7d96a8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977041"
---
# <span data-ttu-id="13938-101">New-AzIotHubSasToken</span><span class="sxs-lookup"><span data-stu-id="13938-101">New-AzIotHubSasToken</span></span>

## <span data-ttu-id="13938-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13938-102">SYNOPSIS</span></span>
<span data-ttu-id="13938-103">Wygeneruj token SAS dla docelowego centrum IoT Hub, urządzenia lub modułu.</span><span class="sxs-lookup"><span data-stu-id="13938-103">Generate a SAS token for a target IoT Hub, device or module.</span></span>

## <span data-ttu-id="13938-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="13938-104">SYNTAX</span></span>

### <span data-ttu-id="13938-105">Zestaw zasobów (domyślny)</span><span class="sxs-lookup"><span data-stu-id="13938-105">ResourceSet (Default)</span></span>
```
New-AzIotHubSasToken [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>]
 [-ModuleId <String>] [-KeyName <String>] [-KeyType <PSKeyType>] [-Duration <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13938-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="13938-106">InputObjectSet</span></span>
```
New-AzIotHubSasToken [-InputObject] <PSIotHub> [-DeviceId <String>] [-ModuleId <String>] [-KeyName <String>]
 [-KeyType <PSKeyType>] [-Duration <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="13938-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="13938-107">ResourceIdSet</span></span>
```
New-AzIotHubSasToken [-ResourceId] <String> [-DeviceId <String>] [-ModuleId <String>] [-KeyName <String>]
 [-KeyType <PSKeyType>] [-Duration <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="13938-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="13938-108">DESCRIPTION</span></span>
<span data-ttu-id="13938-109">W przypadku tokenów SAS urządzenia parametr zasad jest używany tylko do uzyskiwania dostępu do rejestru urządzenia.</span><span class="sxs-lookup"><span data-stu-id="13938-109">For device SAS tokens, the policy parameter is used to access the the device registry only.</span></span> <span data-ttu-id="13938-110">Dlatego zasady powinny mieć dostęp do odczytu rejestru.</span><span class="sxs-lookup"><span data-stu-id="13938-110">Therefore the policy should have read access to the registry.</span></span>
<span data-ttu-id="13938-111">W przypadku tokenów centrum IoT zasady są częścią interfejsu SAS.</span><span class="sxs-lookup"><span data-stu-id="13938-111">For IoT Hub tokens the policy is part of the SAS.</span></span>

## <span data-ttu-id="13938-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="13938-112">EXAMPLES</span></span>

### <span data-ttu-id="13938-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="13938-113">Example 1</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="13938-114">Wygeneruj token SAS centrum IoT przy użyciu zasad iothubowner i klucza podstawowego.</span><span class="sxs-lookup"><span data-stu-id="13938-114">Generate an IoT Hub SAS token using the iothubowner policy and primary key.</span></span>

### <span data-ttu-id="13938-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="13938-115">Example 2</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -KeyName "registryRead" -KeyType "secondary"
```

<span data-ttu-id="13938-116">Wygeneruj token SAS centrum IoT przy użyciu zasad registryRead i klucza pomocniczego.</span><span class="sxs-lookup"><span data-stu-id="13938-116">Generate an IoT Hub SAS token using the registryRead policy and secondary key.</span></span>

### <span data-ttu-id="13938-117">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="13938-117">Example 3</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"
```

<span data-ttu-id="13938-118">Wygeneruj token SAS urządzenia przy użyciu zasad właściciela iothub w celu uzyskania dostępu do rejestru urządzenia usługi {iothub_name}.</span><span class="sxs-lookup"><span data-stu-id="13938-118">Generate a device SAS token using the iothubowner policy to access the {iothub_name} device registry.</span></span>

### <span data-ttu-id="13938-119">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="13938-119">Example 4</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1"
```

<span data-ttu-id="13938-120">Wygeneruj token SAS modułu za pomocą zasad właściciela iothub w celu uzyskania dostępu do rejestru urządzenia usługi {iothub_name}.</span><span class="sxs-lookup"><span data-stu-id="13938-120">Generate a module SAS token using the iothubowner policy to access the {iothub_name} device registry.</span></span>

## <span data-ttu-id="13938-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="13938-121">PARAMETERS</span></span>

### <span data-ttu-id="13938-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13938-122">-DefaultProfile</span></span>
<span data-ttu-id="13938-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="13938-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13938-124">— DeviceId</span><span class="sxs-lookup"><span data-stu-id="13938-124">-DeviceId</span></span>
<span data-ttu-id="13938-125">Identyfikator urządzenia docelowego.</span><span class="sxs-lookup"><span data-stu-id="13938-125">Target Device Id.</span></span>

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

### <span data-ttu-id="13938-126">— Czas trwania</span><span class="sxs-lookup"><span data-stu-id="13938-126">-Duration</span></span>
<span data-ttu-id="13938-127">Przyszła wygaśnięcie (w sekundach) tokenu do wygenerowania.</span><span class="sxs-lookup"><span data-stu-id="13938-127">Future expiry (in seconds) of the token to be generated.</span></span>
<span data-ttu-id="13938-128">Wartość domyślna to 3600.</span><span class="sxs-lookup"><span data-stu-id="13938-128">Default is 3600.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13938-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="13938-129">-InputObject</span></span>
<span data-ttu-id="13938-130">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="13938-130">IotHub object</span></span>

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

### <span data-ttu-id="13938-131">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="13938-131">-IotHubName</span></span>
<span data-ttu-id="13938-132">Nazwa Centrum Iot</span><span class="sxs-lookup"><span data-stu-id="13938-132">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="13938-133">-KeyName</span><span class="sxs-lookup"><span data-stu-id="13938-133">-KeyName</span></span>
<span data-ttu-id="13938-134">Nazwa klucza programu Access.</span><span class="sxs-lookup"><span data-stu-id="13938-134">Access key name.</span></span>

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

### <span data-ttu-id="13938-135">-KeyType</span><span class="sxs-lookup"><span data-stu-id="13938-135">-KeyType</span></span>
<span data-ttu-id="13938-136">Typ klucza programu Access.</span><span class="sxs-lookup"><span data-stu-id="13938-136">Access key type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSKeyType
Parameter Sets: (All)
Aliases:
Accepted values: primary, secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13938-137">- ModuleId</span><span class="sxs-lookup"><span data-stu-id="13938-137">-ModuleId</span></span>
<span data-ttu-id="13938-138">Identyfikator modułu docelowego.</span><span class="sxs-lookup"><span data-stu-id="13938-138">Target Module Id.</span></span>

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

### <span data-ttu-id="13938-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13938-139">-ResourceGroupName</span></span>
<span data-ttu-id="13938-140">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="13938-140">Name of the Resource Group</span></span>

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

### <span data-ttu-id="13938-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="13938-141">-ResourceId</span></span>
<span data-ttu-id="13938-142">Identyfikator zasobu w aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="13938-142">IotHub Resource Id</span></span>

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

### <span data-ttu-id="13938-143">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="13938-143">-Confirm</span></span>
<span data-ttu-id="13938-144">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="13938-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13938-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13938-145">-WhatIf</span></span>
<span data-ttu-id="13938-146">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13938-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13938-147">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="13938-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13938-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13938-148">CommonParameters</span></span>
<span data-ttu-id="13938-149">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13938-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13938-150">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13938-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13938-151">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="13938-151">INPUTS</span></span>

### <span data-ttu-id="13938-152">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="13938-152">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="13938-153">System.String</span><span class="sxs-lookup"><span data-stu-id="13938-153">System.String</span></span>

## <span data-ttu-id="13938-154">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="13938-154">OUTPUTS</span></span>

### <span data-ttu-id="13938-155">System.String</span><span class="sxs-lookup"><span data-stu-id="13938-155">System.String</span></span>

## <span data-ttu-id="13938-156">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="13938-156">NOTES</span></span>

## <span data-ttu-id="13938-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="13938-157">RELATED LINKS</span></span>
