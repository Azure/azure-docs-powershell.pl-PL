---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeRole.md
ms.openlocfilehash: aa44399adcfd5e39d956215b7ca824e5ef9abd60
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501636"
---
# <span data-ttu-id="1d4ee-101">New-AzDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="1d4ee-101">New-AzDataBoxEdgeRole</span></span>

## <span data-ttu-id="1d4ee-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1d4ee-102">SYNOPSIS</span></span>
<span data-ttu-id="1d4ee-103">Tworzy nową rolę dla urządzenia</span><span class="sxs-lookup"><span data-stu-id="1d4ee-103">Creates a new Role for a device</span></span>

## <span data-ttu-id="1d4ee-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1d4ee-104">SYNTAX</span></span>

### <span data-ttu-id="1d4ee-105">ConnectionStringParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1d4ee-105">ConnectionStringParameterSet (Default)</span></span>
```
New-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-ConnectionString]
 -IotDeviceConnectionString <SecureString> -IotEdgeDeviceConnectionString <SecureString>
 -EncryptionKey <SecureString> -Platform <String> -RoleStatus <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d4ee-106">IotParameterSet</span><span class="sxs-lookup"><span data-stu-id="1d4ee-106">IotParameterSet</span></span>
```
New-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-DeviceProperty]
 -IotDeviceId <String> -IotDeviceAccessKey <SecureString> -IotEdgeDeviceId <String>
 -IotEdgeDeviceAccessKey <SecureString> -IotHostHub <String> -EncryptionKey <SecureString> -Platform <String>
 -RoleStatus <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1d4ee-107">Opis</span><span class="sxs-lookup"><span data-stu-id="1d4ee-107">DESCRIPTION</span></span>
<span data-ttu-id="1d4ee-108">Polecenie cmdlet **New-AzDataBoxEdgeRole** tworzy nową rolę dla urządzenia z polem danych Edge.</span><span class="sxs-lookup"><span data-stu-id="1d4ee-108">The **New-AzDataBoxEdgeRole** cmdlet creates a new Role for a Data Box Edge device.</span></span>

## <span data-ttu-id="1d4ee-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1d4ee-109">EXAMPLES</span></span>

### <span data-ttu-id="1d4ee-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1d4ee-110">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name iotrole -DeviceProperties
 -IotDeviceId iotDeviceId -IotDeviceAccessKey iotAccessKey -IotEdgeDeviceId iotEdgeDeviceId -IotEdgeDeviceAccessKey iotEdgeDeviceAccessKey
 -IotHostHub "ehub.azure-devices.net" -EncryptionKey @SecureString -Platform Linux -RoleStatus Enabled

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
iotrole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceId   iotDeviceId  resourceGroupName
```

## <span data-ttu-id="1d4ee-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1d4ee-111">PARAMETERS</span></span>

### <span data-ttu-id="1d4ee-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1d4ee-112">-AsJob</span></span>
<span data-ttu-id="1d4ee-113">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="1d4ee-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1d4ee-114">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="1d4ee-114">-ConnectionString</span></span>
<span data-ttu-id="1d4ee-115">Aby zapewnić parametry połączenia</span><span class="sxs-lookup"><span data-stu-id="1d4ee-115">To Provide Connection Strings</span></span>

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

### <span data-ttu-id="1d4ee-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d4ee-116">-DefaultProfile</span></span>
<span data-ttu-id="1d4ee-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1d4ee-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d4ee-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="1d4ee-118">-DeviceName</span></span>
<span data-ttu-id="1d4ee-119">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="1d4ee-119">Device Name</span></span>

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

### <span data-ttu-id="1d4ee-120">-DeviceProperty</span><span class="sxs-lookup"><span data-stu-id="1d4ee-120">-DeviceProperty</span></span>
<span data-ttu-id="1d4ee-121">Aby podać właściwości urządzenia</span><span class="sxs-lookup"><span data-stu-id="1d4ee-121">To Provide Device Properties</span></span>

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

### <span data-ttu-id="1d4ee-122">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="1d4ee-122">-EncryptionKey</span></span>
<span data-ttu-id="1d4ee-123">Klucz szyfrowania urządzenia brzegowego</span><span class="sxs-lookup"><span data-stu-id="1d4ee-123">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="1d4ee-124">-IotDeviceAccessKey</span><span class="sxs-lookup"><span data-stu-id="1d4ee-124">-IotDeviceAccessKey</span></span>
<span data-ttu-id="1d4ee-125">Klucz dostępu do urządzenia IoT</span><span class="sxs-lookup"><span data-stu-id="1d4ee-125">Iot Device Access Key</span></span>

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

### <span data-ttu-id="1d4ee-126">-IotDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="1d4ee-126">-IotDeviceConnectionString</span></span>
<span data-ttu-id="1d4ee-127">Podaj parametry połączenia z urządzeniem IOT</span><span class="sxs-lookup"><span data-stu-id="1d4ee-127">Please provide connection string of IOT Device</span></span>

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

### <span data-ttu-id="1d4ee-128">-IotDeviceId</span><span class="sxs-lookup"><span data-stu-id="1d4ee-128">-IotDeviceId</span></span>
<span data-ttu-id="1d4ee-129">Identyfikator urządzenia IoT</span><span class="sxs-lookup"><span data-stu-id="1d4ee-129">Device Id of the Iot Device</span></span>

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

### <span data-ttu-id="1d4ee-130">-IotEdgeDeviceAccessKey</span><span class="sxs-lookup"><span data-stu-id="1d4ee-130">-IotEdgeDeviceAccessKey</span></span>
<span data-ttu-id="1d4ee-131">Klucz dostępu do urządzenia IoT Edge</span><span class="sxs-lookup"><span data-stu-id="1d4ee-131">Access key of the Iot Edge device</span></span>

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

### <span data-ttu-id="1d4ee-132">-IotEdgeDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="1d4ee-132">-IotEdgeDeviceConnectionString</span></span>
<span data-ttu-id="1d4ee-133">Podaj parametry połączenia urządzenia brzegowego</span><span class="sxs-lookup"><span data-stu-id="1d4ee-133">Please provide connection string of Edge Device</span></span>

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

### <span data-ttu-id="1d4ee-134">-IotEdgeDeviceId</span><span class="sxs-lookup"><span data-stu-id="1d4ee-134">-IotEdgeDeviceId</span></span>
<span data-ttu-id="1d4ee-135">Identyfikator urządzenia IoT Edge</span><span class="sxs-lookup"><span data-stu-id="1d4ee-135">Id of the Iot Edge Device</span></span>

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

### <span data-ttu-id="1d4ee-136">-IotHostHub</span><span class="sxs-lookup"><span data-stu-id="1d4ee-136">-IotHostHub</span></span>
<span data-ttu-id="1d4ee-137">Adres Hosthub</span><span class="sxs-lookup"><span data-stu-id="1d4ee-137">Hosthub address</span></span>

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

### <span data-ttu-id="1d4ee-138">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1d4ee-138">-Name</span></span>
<span data-ttu-id="1d4ee-139">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="1d4ee-139">Resource Name</span></span>

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

### <span data-ttu-id="1d4ee-140">-Platform</span><span class="sxs-lookup"><span data-stu-id="1d4ee-140">-Platform</span></span>
<span data-ttu-id="1d4ee-141">Dostarcz platformę na platformie ex: Linux</span><span class="sxs-lookup"><span data-stu-id="1d4ee-141">Provide the Platform, for ex: Linux</span></span>

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

### <span data-ttu-id="1d4ee-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d4ee-142">-ResourceGroupName</span></span>
<span data-ttu-id="1d4ee-143">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="1d4ee-143">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d4ee-144">-RoleStatus</span><span class="sxs-lookup"><span data-stu-id="1d4ee-144">-RoleStatus</span></span>
<span data-ttu-id="1d4ee-145">Zapewnianie włączenia/wyłączenia statusu</span><span class="sxs-lookup"><span data-stu-id="1d4ee-145">Provide the status enable/disable</span></span>

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

### <span data-ttu-id="1d4ee-146">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1d4ee-146">-Confirm</span></span>
<span data-ttu-id="1d4ee-147">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d4ee-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d4ee-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d4ee-148">-WhatIf</span></span>
<span data-ttu-id="1d4ee-149">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d4ee-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1d4ee-150">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1d4ee-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d4ee-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d4ee-151">CommonParameters</span></span>
<span data-ttu-id="1d4ee-152">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d4ee-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d4ee-153">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1d4ee-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d4ee-154">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1d4ee-154">INPUTS</span></span>

### <span data-ttu-id="1d4ee-155">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="1d4ee-155">None</span></span>

## <span data-ttu-id="1d4ee-156">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1d4ee-156">OUTPUTS</span></span>

### <span data-ttu-id="1d4ee-157">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="1d4ee-157">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="1d4ee-158">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1d4ee-158">NOTES</span></span>

## <span data-ttu-id="1d4ee-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1d4ee-159">RELATED LINKS</span></span>
