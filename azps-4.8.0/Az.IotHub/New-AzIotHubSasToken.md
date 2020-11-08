---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/new-aziothubsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubSasToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubSasToken.md
ms.openlocfilehash: 486ca6543bb32d096e454d16ff3640720f2f53fe
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062718"
---
# <span data-ttu-id="e738e-101">New-AzIotHubSasToken</span><span class="sxs-lookup"><span data-stu-id="e738e-101">New-AzIotHubSasToken</span></span>

## <span data-ttu-id="e738e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e738e-102">SYNOPSIS</span></span>
<span data-ttu-id="e738e-103">Generuj token SAS dla docelowego Centrum IoT, urządzenia lub modułu.</span><span class="sxs-lookup"><span data-stu-id="e738e-103">Generate a SAS token for a target IoT Hub, device or module.</span></span>

## <span data-ttu-id="e738e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e738e-104">SYNTAX</span></span>

### <span data-ttu-id="e738e-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e738e-105">ResourceSet (Default)</span></span>
```
New-AzIotHubSasToken [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>]
 [-ModuleId <String>] [-KeyName <String>] [-KeyType <PSKeyType>] [-Duration <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e738e-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e738e-106">InputObjectSet</span></span>
```
New-AzIotHubSasToken [-InputObject] <PSIotHub> [-DeviceId <String>] [-ModuleId <String>] [-KeyName <String>]
 [-KeyType <PSKeyType>] [-Duration <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e738e-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e738e-107">ResourceIdSet</span></span>
```
New-AzIotHubSasToken [-ResourceId] <String> [-DeviceId <String>] [-ModuleId <String>] [-KeyName <String>]
 [-KeyType <PSKeyType>] [-Duration <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e738e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e738e-108">DESCRIPTION</span></span>
<span data-ttu-id="e738e-109">W przypadku tokenów SAS urządzenia parametr Policy jest wykorzystywany tylko w celu uzyskania dostępu do rejestru urządzenia.</span><span class="sxs-lookup"><span data-stu-id="e738e-109">For device SAS tokens, the policy parameter is used to access the the device registry only.</span></span> <span data-ttu-id="e738e-110">Dlatego zasady powinny mieć dostęp do odczytu do rejestru.</span><span class="sxs-lookup"><span data-stu-id="e738e-110">Therefore the policy should have read access to the registry.</span></span>
<span data-ttu-id="e738e-111">W przypadku tokenów Centrum IoT zasady są częścią skojarzeń zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="e738e-111">For IoT Hub tokens the policy is part of the SAS.</span></span>

## <span data-ttu-id="e738e-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e738e-112">EXAMPLES</span></span>

### <span data-ttu-id="e738e-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e738e-113">Example 1</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="e738e-114">Wygeneruj token SAS Centrum IoT przy użyciu zasad iothubowner i klucza podstawowego.</span><span class="sxs-lookup"><span data-stu-id="e738e-114">Generate an IoT Hub SAS token using the iothubowner policy and primary key.</span></span>

### <span data-ttu-id="e738e-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="e738e-115">Example 2</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -KeyName "registryRead" -KeyType "secondary"
```

<span data-ttu-id="e738e-116">Wygeneruj token SAS Centrum IoT przy użyciu zasad registryRead i klucza pomocniczego.</span><span class="sxs-lookup"><span data-stu-id="e738e-116">Generate an IoT Hub SAS token using the registryRead policy and secondary key.</span></span>

### <span data-ttu-id="e738e-117">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="e738e-117">Example 3</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"
```

<span data-ttu-id="e738e-118">Wygeneruj token SAS urządzenia przy użyciu zasad iothubowner, aby uzyskać dostęp do rejestru urządzenia {iothub_name}.</span><span class="sxs-lookup"><span data-stu-id="e738e-118">Generate a device SAS token using the iothubowner policy to access the {iothub_name} device registry.</span></span>

### <span data-ttu-id="e738e-119">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="e738e-119">Example 4</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1"
```

<span data-ttu-id="e738e-120">Wygeneruj token SAS modułu przy użyciu zasad iothubowner, aby uzyskać dostęp do rejestru urządzenia {iothub_name}.</span><span class="sxs-lookup"><span data-stu-id="e738e-120">Generate a module SAS token using the iothubowner policy to access the {iothub_name} device registry.</span></span>

## <span data-ttu-id="e738e-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e738e-121">PARAMETERS</span></span>

### <span data-ttu-id="e738e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e738e-122">-DefaultProfile</span></span>
<span data-ttu-id="e738e-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e738e-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e738e-124">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="e738e-124">-DeviceId</span></span>
<span data-ttu-id="e738e-125">Identyfikator urządzenia docelowego.</span><span class="sxs-lookup"><span data-stu-id="e738e-125">Target Device Id.</span></span>

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

### <span data-ttu-id="e738e-126">— Czas trwania</span><span class="sxs-lookup"><span data-stu-id="e738e-126">-Duration</span></span>
<span data-ttu-id="e738e-127">Przyszły wygaśnięcie (w sekundach) tokenu do wygenerowania.</span><span class="sxs-lookup"><span data-stu-id="e738e-127">Future expiry (in seconds) of the token to be generated.</span></span>
<span data-ttu-id="e738e-128">Wartość domyślna to 3600.</span><span class="sxs-lookup"><span data-stu-id="e738e-128">Default is 3600.</span></span>

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

### <span data-ttu-id="e738e-129">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e738e-129">-InputObject</span></span>
<span data-ttu-id="e738e-130">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="e738e-130">IotHub object</span></span>

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

### <span data-ttu-id="e738e-131">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="e738e-131">-IotHubName</span></span>
<span data-ttu-id="e738e-132">Nazwa Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="e738e-132">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="e738e-133">-NazwaKlucza</span><span class="sxs-lookup"><span data-stu-id="e738e-133">-KeyName</span></span>
<span data-ttu-id="e738e-134">Nazwa klucza programu Access.</span><span class="sxs-lookup"><span data-stu-id="e738e-134">Access key name.</span></span>

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

### <span data-ttu-id="e738e-135">-KeyType</span><span class="sxs-lookup"><span data-stu-id="e738e-135">-KeyType</span></span>
<span data-ttu-id="e738e-136">Typ klawisza dostępu.</span><span class="sxs-lookup"><span data-stu-id="e738e-136">Access key type.</span></span>

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

### <span data-ttu-id="e738e-137">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="e738e-137">-ModuleId</span></span>
<span data-ttu-id="e738e-138">Identyfikator modułu docelowego.</span><span class="sxs-lookup"><span data-stu-id="e738e-138">Target Module Id.</span></span>

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

### <span data-ttu-id="e738e-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e738e-139">-ResourceGroupName</span></span>
<span data-ttu-id="e738e-140">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="e738e-140">Name of the Resource Group</span></span>

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

### <span data-ttu-id="e738e-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e738e-141">-ResourceId</span></span>
<span data-ttu-id="e738e-142">Identyfikator zasobu IotHub</span><span class="sxs-lookup"><span data-stu-id="e738e-142">IotHub Resource Id</span></span>

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

### <span data-ttu-id="e738e-143">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e738e-143">-Confirm</span></span>
<span data-ttu-id="e738e-144">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e738e-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e738e-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e738e-145">-WhatIf</span></span>
<span data-ttu-id="e738e-146">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e738e-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e738e-147">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e738e-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e738e-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e738e-148">CommonParameters</span></span>
<span data-ttu-id="e738e-149">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e738e-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e738e-150">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e738e-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e738e-151">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e738e-151">INPUTS</span></span>

### <span data-ttu-id="e738e-152">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="e738e-152">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="e738e-153">System. String</span><span class="sxs-lookup"><span data-stu-id="e738e-153">System.String</span></span>

## <span data-ttu-id="e738e-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e738e-154">OUTPUTS</span></span>

### <span data-ttu-id="e738e-155">System. String</span><span class="sxs-lookup"><span data-stu-id="e738e-155">System.String</span></span>

## <span data-ttu-id="e738e-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e738e-156">NOTES</span></span>

## <span data-ttu-id="e738e-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e738e-157">RELATED LINKS</span></span>
