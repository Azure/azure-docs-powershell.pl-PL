---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeRole.md
ms.openlocfilehash: f2244bc1d0471924ad7f69ff600e70e92fdc809a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503566"
---
# <span data-ttu-id="9b522-101">New-AzStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="9b522-101">New-AzStackEdgeRole</span></span>

## <span data-ttu-id="9b522-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9b522-102">SYNOPSIS</span></span>
<span data-ttu-id="9b522-103">Tworzy nową rolę dla urządzenia</span><span class="sxs-lookup"><span data-stu-id="9b522-103">Creates a new Role for a device</span></span>

## <span data-ttu-id="9b522-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9b522-104">SYNTAX</span></span>

### <span data-ttu-id="9b522-105">ConnectionStringParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9b522-105">ConnectionStringParameterSet (Default)</span></span>
```
New-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-ConnectionString]
 -IotDeviceConnectionString <SecureString> -IotEdgeDeviceConnectionString <SecureString>
 -EncryptionKey <SecureString> -Platform <String> [-RoleStatus <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b522-106">IotParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b522-106">IotParameterSet</span></span>
```
New-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-DeviceProperty]
 -IotDeviceId <String> -IotDeviceAccessKey <SecureString> -IotEdgeDeviceId <String>
 -IotEdgeDeviceAccessKey <SecureString> -IotHostHub <String> -EncryptionKey <SecureString> -Platform <String>
 [-RoleStatus <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9b522-107">Opis</span><span class="sxs-lookup"><span data-stu-id="9b522-107">DESCRIPTION</span></span>
<span data-ttu-id="9b522-108">Polecenie cmdlet **New-AzStackEdgeRole** tworzy nową rolę dla urządzenia z krawędzią stosu.</span><span class="sxs-lookup"><span data-stu-id="9b522-108">The **New-AzStackEdgeRole** cmdlet creates a new Role for a Stack Edge device.</span></span>

## <span data-ttu-id="9b522-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9b522-109">EXAMPLES</span></span>

### <span data-ttu-id="9b522-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9b522-110">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name iotrole -DeviceProperties
 -IotDeviceId iotDeviceId -IotDeviceAccessKey iotAccessKey -IotEdgeDeviceId iotEdgeDeviceId -IotEdgeDeviceAccessKey iotEdgeDeviceAccessKey
 -IotHostHub "ehub.azure-devices.net" -EncryptionKey @SecureString -Platform Linux -RoleStatus Enabled

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
iotrole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceId   iotDeviceId  resourceGroupName
```

## <span data-ttu-id="9b522-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9b522-111">PARAMETERS</span></span>

### <span data-ttu-id="9b522-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9b522-112">-AsJob</span></span>
<span data-ttu-id="9b522-113">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="9b522-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9b522-114">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="9b522-114">-ConnectionString</span></span>
<span data-ttu-id="9b522-115">Aby zapewnić parametry połączenia</span><span class="sxs-lookup"><span data-stu-id="9b522-115">To Provide Connection Strings</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ConnectionStringParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b522-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b522-116">-DefaultProfile</span></span>
<span data-ttu-id="9b522-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9b522-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b522-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="9b522-118">-DeviceName</span></span>
<span data-ttu-id="9b522-119">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="9b522-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b522-120">-DeviceProperty</span><span class="sxs-lookup"><span data-stu-id="9b522-120">-DeviceProperty</span></span>
<span data-ttu-id="9b522-121">Aby podać właściwości urządzenia</span><span class="sxs-lookup"><span data-stu-id="9b522-121">To Provide Device Properties</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: IotParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b522-122">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="9b522-122">-EncryptionKey</span></span>
<span data-ttu-id="9b522-123">Klucz szyfrowania urządzenia brzegowego</span><span class="sxs-lookup"><span data-stu-id="9b522-123">Encryption key of the Edge device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b522-124">-IotDeviceAccessKey</span><span class="sxs-lookup"><span data-stu-id="9b522-124">-IotDeviceAccessKey</span></span>
<span data-ttu-id="9b522-125">Klucz dostępu do urządzenia IoT</span><span class="sxs-lookup"><span data-stu-id="9b522-125">Iot Device Access Key</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: IotParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b522-126">-IotDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="9b522-126">-IotDeviceConnectionString</span></span>
<span data-ttu-id="9b522-127">Podaj parametry połączenia z urządzeniem IOT</span><span class="sxs-lookup"><span data-stu-id="9b522-127">Please provide connection string of IOT Device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ConnectionStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b522-128">-IotDeviceId</span><span class="sxs-lookup"><span data-stu-id="9b522-128">-IotDeviceId</span></span>
<span data-ttu-id="9b522-129">Identyfikator urządzenia IoT</span><span class="sxs-lookup"><span data-stu-id="9b522-129">Device Id of the Iot Device</span></span>

```yaml
Type: System.String
Parameter Sets: IotParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b522-130">-IotEdgeDeviceAccessKey</span><span class="sxs-lookup"><span data-stu-id="9b522-130">-IotEdgeDeviceAccessKey</span></span>
<span data-ttu-id="9b522-131">Klucz dostępu do urządzenia IoT Edge</span><span class="sxs-lookup"><span data-stu-id="9b522-131">Access key of the Iot Edge device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: IotParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b522-132">-IotEdgeDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="9b522-132">-IotEdgeDeviceConnectionString</span></span>
<span data-ttu-id="9b522-133">Podaj parametry połączenia urządzenia brzegowego</span><span class="sxs-lookup"><span data-stu-id="9b522-133">Please provide connection string of Edge Device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ConnectionStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b522-134">-IotEdgeDeviceId</span><span class="sxs-lookup"><span data-stu-id="9b522-134">-IotEdgeDeviceId</span></span>
<span data-ttu-id="9b522-135">Identyfikator urządzenia IoT Edge</span><span class="sxs-lookup"><span data-stu-id="9b522-135">Id of the Iot Edge Device</span></span>

```yaml
Type: System.String
Parameter Sets: IotParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b522-136">-IotHostHub</span><span class="sxs-lookup"><span data-stu-id="9b522-136">-IotHostHub</span></span>
<span data-ttu-id="9b522-137">Adres Hosthub</span><span class="sxs-lookup"><span data-stu-id="9b522-137">Hosthub address</span></span>

```yaml
Type: System.String
Parameter Sets: IotParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b522-138">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9b522-138">-Name</span></span>
<span data-ttu-id="9b522-139">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="9b522-139">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RoleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b522-140">-Platform</span><span class="sxs-lookup"><span data-stu-id="9b522-140">-Platform</span></span>
<span data-ttu-id="9b522-141">Dostarcz platformę na platformie ex: Linux</span><span class="sxs-lookup"><span data-stu-id="9b522-141">Provide the Platform, for ex: Linux</span></span>

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

### <span data-ttu-id="9b522-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b522-142">-ResourceGroupName</span></span>
<span data-ttu-id="9b522-143">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="9b522-143">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b522-144">-RoleStatus</span><span class="sxs-lookup"><span data-stu-id="9b522-144">-RoleStatus</span></span>
<span data-ttu-id="9b522-145">Zapewnianie włączenia/wyłączenia statusu</span><span class="sxs-lookup"><span data-stu-id="9b522-145">Provide the status enable/disable</span></span>

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

### <span data-ttu-id="9b522-146">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9b522-146">-Confirm</span></span>
<span data-ttu-id="9b522-147">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b522-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b522-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b522-148">-WhatIf</span></span>
<span data-ttu-id="9b522-149">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b522-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9b522-150">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9b522-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b522-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b522-151">CommonParameters</span></span>
<span data-ttu-id="9b522-152">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b522-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b522-153">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9b522-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b522-154">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9b522-154">INPUTS</span></span>

### <span data-ttu-id="9b522-155">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="9b522-155">None</span></span>

## <span data-ttu-id="9b522-156">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9b522-156">OUTPUTS</span></span>

### <span data-ttu-id="9b522-157">Microsoft. Azure. PowerShell. polecenia. StackEdge. models. PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="9b522-157">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="9b522-158">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9b522-158">NOTES</span></span>

## <span data-ttu-id="9b522-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9b522-159">RELATED LINKS</span></span>
