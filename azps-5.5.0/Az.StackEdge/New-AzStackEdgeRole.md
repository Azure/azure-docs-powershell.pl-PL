---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeRole.md
ms.openlocfilehash: f2244bc1d0471924ad7f69ff600e70e92fdc809a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241906"
---
# <span data-ttu-id="fafea-101">New-AzStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="fafea-101">New-AzStackEdgeRole</span></span>

## <span data-ttu-id="fafea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fafea-102">SYNOPSIS</span></span>
<span data-ttu-id="fafea-103">Tworzy nową rolę dla urządzenia</span><span class="sxs-lookup"><span data-stu-id="fafea-103">Creates a new Role for a device</span></span>

## <span data-ttu-id="fafea-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fafea-104">SYNTAX</span></span>

### <span data-ttu-id="fafea-105">ConnectionStringParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="fafea-105">ConnectionStringParameterSet (Default)</span></span>
```
New-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-ConnectionString]
 -IotDeviceConnectionString <SecureString> -IotEdgeDeviceConnectionString <SecureString>
 -EncryptionKey <SecureString> -Platform <String> [-RoleStatus <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fafea-106">IotParameterSet</span><span class="sxs-lookup"><span data-stu-id="fafea-106">IotParameterSet</span></span>
```
New-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-DeviceProperty]
 -IotDeviceId <String> -IotDeviceAccessKey <SecureString> -IotEdgeDeviceId <String>
 -IotEdgeDeviceAccessKey <SecureString> -IotHostHub <String> -EncryptionKey <SecureString> -Platform <String>
 [-RoleStatus <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fafea-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="fafea-107">DESCRIPTION</span></span>
<span data-ttu-id="fafea-108">Polecenie **cmdlet New-AzStackEdgeRole** tworzy nową rolę dla urządzenia Stack Edge.</span><span class="sxs-lookup"><span data-stu-id="fafea-108">The **New-AzStackEdgeRole** cmdlet creates a new Role for a Stack Edge device.</span></span>

## <span data-ttu-id="fafea-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fafea-109">EXAMPLES</span></span>

### <span data-ttu-id="fafea-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fafea-110">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name iotrole -DeviceProperties
 -IotDeviceId iotDeviceId -IotDeviceAccessKey iotAccessKey -IotEdgeDeviceId iotEdgeDeviceId -IotEdgeDeviceAccessKey iotEdgeDeviceAccessKey
 -IotHostHub "ehub.azure-devices.net" -EncryptionKey @SecureString -Platform Linux -RoleStatus Enabled

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
iotrole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceId   iotDeviceId  resourceGroupName
```

## <span data-ttu-id="fafea-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fafea-111">PARAMETERS</span></span>

### <span data-ttu-id="fafea-112">— AsJob</span><span class="sxs-lookup"><span data-stu-id="fafea-112">-AsJob</span></span>
<span data-ttu-id="fafea-113">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="fafea-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fafea-114">- ConnectionString</span><span class="sxs-lookup"><span data-stu-id="fafea-114">-ConnectionString</span></span>
<span data-ttu-id="fafea-115">Aby zapewnić parametry połączenia</span><span class="sxs-lookup"><span data-stu-id="fafea-115">To Provide Connection Strings</span></span>

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

### <span data-ttu-id="fafea-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fafea-116">-DefaultProfile</span></span>
<span data-ttu-id="fafea-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="fafea-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fafea-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="fafea-118">-DeviceName</span></span>
<span data-ttu-id="fafea-119">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="fafea-119">Device Name</span></span>

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

### <span data-ttu-id="fafea-120">- DeviceProperty</span><span class="sxs-lookup"><span data-stu-id="fafea-120">-DeviceProperty</span></span>
<span data-ttu-id="fafea-121">Aby podać właściwości urządzenia</span><span class="sxs-lookup"><span data-stu-id="fafea-121">To Provide Device Properties</span></span>

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

### <span data-ttu-id="fafea-122">— Klucz szyfrowania</span><span class="sxs-lookup"><span data-stu-id="fafea-122">-EncryptionKey</span></span>
<span data-ttu-id="fafea-123">Klucz szyfrowania urządzenia Edge</span><span class="sxs-lookup"><span data-stu-id="fafea-123">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="fafea-124">-IotDeviceAccessKey</span><span class="sxs-lookup"><span data-stu-id="fafea-124">-IotDeviceAccessKey</span></span>
<span data-ttu-id="fafea-125">Klawisz dostępu urządzenia Iot</span><span class="sxs-lookup"><span data-stu-id="fafea-125">Iot Device Access Key</span></span>

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

### <span data-ttu-id="fafea-126">-IotDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="fafea-126">-IotDeviceConnectionString</span></span>
<span data-ttu-id="fafea-127">Podaj ciąg połączenia urządzenia IOT</span><span class="sxs-lookup"><span data-stu-id="fafea-127">Please provide connection string of IOT Device</span></span>

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

### <span data-ttu-id="fafea-128">-IotDeviceId</span><span class="sxs-lookup"><span data-stu-id="fafea-128">-IotDeviceId</span></span>
<span data-ttu-id="fafea-129">Identyfikator urządzenia iot</span><span class="sxs-lookup"><span data-stu-id="fafea-129">Device Id of the Iot Device</span></span>

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

### <span data-ttu-id="fafea-130">-IotEdgeDeviceAccessKey</span><span class="sxs-lookup"><span data-stu-id="fafea-130">-IotEdgeDeviceAccessKey</span></span>
<span data-ttu-id="fafea-131">Klawisz dostępu urządzenia iot Edge</span><span class="sxs-lookup"><span data-stu-id="fafea-131">Access key of the Iot Edge device</span></span>

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

### <span data-ttu-id="fafea-132">-IotEdgeDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="fafea-132">-IotEdgeDeviceConnectionString</span></span>
<span data-ttu-id="fafea-133">Podaj ciąg połączenia urządzenia Edge</span><span class="sxs-lookup"><span data-stu-id="fafea-133">Please provide connection string of Edge Device</span></span>

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

### <span data-ttu-id="fafea-134">-IotEdgeDeviceId</span><span class="sxs-lookup"><span data-stu-id="fafea-134">-IotEdgeDeviceId</span></span>
<span data-ttu-id="fafea-135">Identyfikator urządzenia Edge Iot</span><span class="sxs-lookup"><span data-stu-id="fafea-135">Id of the Iot Edge Device</span></span>

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

### <span data-ttu-id="fafea-136">-IotHostHub</span><span class="sxs-lookup"><span data-stu-id="fafea-136">-IotHostHub</span></span>
<span data-ttu-id="fafea-137">Adres w witrynie Hosthub</span><span class="sxs-lookup"><span data-stu-id="fafea-137">Hosthub address</span></span>

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

### <span data-ttu-id="fafea-138">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="fafea-138">-Name</span></span>
<span data-ttu-id="fafea-139">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="fafea-139">Resource Name</span></span>

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

### <span data-ttu-id="fafea-140">— Platforma</span><span class="sxs-lookup"><span data-stu-id="fafea-140">-Platform</span></span>
<span data-ttu-id="fafea-141">Udostępnij platformę, na przykład: Linux</span><span class="sxs-lookup"><span data-stu-id="fafea-141">Provide the Platform, for ex: Linux</span></span>

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

### <span data-ttu-id="fafea-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fafea-142">-ResourceGroupName</span></span>
<span data-ttu-id="fafea-143">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="fafea-143">Resource Group Name</span></span>

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

### <span data-ttu-id="fafea-144">-RoleStatus</span><span class="sxs-lookup"><span data-stu-id="fafea-144">-RoleStatus</span></span>
<span data-ttu-id="fafea-145">Włączanie/wyłączanie stanu</span><span class="sxs-lookup"><span data-stu-id="fafea-145">Provide the status enable/disable</span></span>

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

### <span data-ttu-id="fafea-146">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fafea-146">-Confirm</span></span>
<span data-ttu-id="fafea-147">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="fafea-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fafea-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fafea-148">-WhatIf</span></span>
<span data-ttu-id="fafea-149">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fafea-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fafea-150">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="fafea-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fafea-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fafea-151">CommonParameters</span></span>
<span data-ttu-id="fafea-152">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fafea-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fafea-153">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fafea-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fafea-154">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fafea-154">INPUTS</span></span>

### <span data-ttu-id="fafea-155">Brak</span><span class="sxs-lookup"><span data-stu-id="fafea-155">None</span></span>

## <span data-ttu-id="fafea-156">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fafea-156">OUTPUTS</span></span>

### <span data-ttu-id="fafea-157">Microsoft.Azure.PowerShell.Cmdlet.StackEdge.Models.PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="fafea-157">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="fafea-158">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fafea-158">NOTES</span></span>

## <span data-ttu-id="fafea-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fafea-159">RELATED LINKS</span></span>
