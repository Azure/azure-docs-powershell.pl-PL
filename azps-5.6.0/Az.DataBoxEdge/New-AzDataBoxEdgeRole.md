---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/new-azdataboxedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeRole.md
ms.openlocfilehash: 0158116440ae7ffc1638ce08c6561e80ca034ae8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978618"
---
# <span data-ttu-id="c7aae-101">New-AzDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="c7aae-101">New-AzDataBoxEdgeRole</span></span>

## <span data-ttu-id="c7aae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7aae-102">SYNOPSIS</span></span>
<span data-ttu-id="c7aae-103">Tworzy nową rolę dla urządzenia</span><span class="sxs-lookup"><span data-stu-id="c7aae-103">Creates a new Role for a device</span></span>

## <span data-ttu-id="c7aae-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c7aae-104">SYNTAX</span></span>

### <span data-ttu-id="c7aae-105">ConnectionStringParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="c7aae-105">ConnectionStringParameterSet (Default)</span></span>
```
New-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-ConnectionString]
 -IotDeviceConnectionString <SecureString> -IotEdgeDeviceConnectionString <SecureString>
 -EncryptionKey <SecureString> -Platform <String> -RoleStatus <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7aae-106">IotParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7aae-106">IotParameterSet</span></span>
```
New-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-DeviceProperty]
 -IotDeviceId <String> -IotDeviceAccessKey <SecureString> -IotEdgeDeviceId <String>
 -IotEdgeDeviceAccessKey <SecureString> -IotHostHub <String> -EncryptionKey <SecureString> -Platform <String>
 -RoleStatus <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c7aae-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="c7aae-107">DESCRIPTION</span></span>
<span data-ttu-id="c7aae-108">Polecenie **cmdlet New-AzDataBoxEdgeRole** tworzy nową rolę dla urządzenia z krawędzią pola danych.</span><span class="sxs-lookup"><span data-stu-id="c7aae-108">The **New-AzDataBoxEdgeRole** cmdlet creates a new Role for a Data Box Edge device.</span></span>

## <span data-ttu-id="c7aae-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c7aae-109">EXAMPLES</span></span>

### <span data-ttu-id="c7aae-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c7aae-110">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name iotrole -DeviceProperties
 -IotDeviceId iotDeviceId -IotDeviceAccessKey iotAccessKey -IotEdgeDeviceId iotEdgeDeviceId -IotEdgeDeviceAccessKey iotEdgeDeviceAccessKey
 -IotHostHub "ehub.azure-devices.net" -EncryptionKey @SecureString -Platform Linux -RoleStatus Enabled

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
iotrole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceId   iotDeviceId  resourceGroupName
```

## <span data-ttu-id="c7aae-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c7aae-111">PARAMETERS</span></span>

### <span data-ttu-id="c7aae-112">— AsJob</span><span class="sxs-lookup"><span data-stu-id="c7aae-112">-AsJob</span></span>
<span data-ttu-id="c7aae-113">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="c7aae-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c7aae-114">- ConnectionString</span><span class="sxs-lookup"><span data-stu-id="c7aae-114">-ConnectionString</span></span>
<span data-ttu-id="c7aae-115">Aby zapewnić parametry połączenia</span><span class="sxs-lookup"><span data-stu-id="c7aae-115">To Provide Connection Strings</span></span>

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

### <span data-ttu-id="c7aae-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7aae-116">-DefaultProfile</span></span>
<span data-ttu-id="c7aae-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c7aae-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7aae-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="c7aae-118">-DeviceName</span></span>
<span data-ttu-id="c7aae-119">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="c7aae-119">Device Name</span></span>

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

### <span data-ttu-id="c7aae-120">- DeviceProperty</span><span class="sxs-lookup"><span data-stu-id="c7aae-120">-DeviceProperty</span></span>
<span data-ttu-id="c7aae-121">Aby podać właściwości urządzenia</span><span class="sxs-lookup"><span data-stu-id="c7aae-121">To Provide Device Properties</span></span>

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

### <span data-ttu-id="c7aae-122">— Klucz szyfrowania</span><span class="sxs-lookup"><span data-stu-id="c7aae-122">-EncryptionKey</span></span>
<span data-ttu-id="c7aae-123">Klucz szyfrowania urządzenia Edge</span><span class="sxs-lookup"><span data-stu-id="c7aae-123">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="c7aae-124">-IotDeviceAccessKey</span><span class="sxs-lookup"><span data-stu-id="c7aae-124">-IotDeviceAccessKey</span></span>
<span data-ttu-id="c7aae-125">Klawisz dostępu urządzenia Iot</span><span class="sxs-lookup"><span data-stu-id="c7aae-125">Iot Device Access Key</span></span>

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

### <span data-ttu-id="c7aae-126">-IotDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="c7aae-126">-IotDeviceConnectionString</span></span>
<span data-ttu-id="c7aae-127">Podaj ciąg połączenia urządzenia IOT</span><span class="sxs-lookup"><span data-stu-id="c7aae-127">Please provide connection string of IOT Device</span></span>

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

### <span data-ttu-id="c7aae-128">-IotDeviceId</span><span class="sxs-lookup"><span data-stu-id="c7aae-128">-IotDeviceId</span></span>
<span data-ttu-id="c7aae-129">Identyfikator urządzenia iot</span><span class="sxs-lookup"><span data-stu-id="c7aae-129">Device Id of the Iot Device</span></span>

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

### <span data-ttu-id="c7aae-130">-IotEdgeDeviceAccessKey</span><span class="sxs-lookup"><span data-stu-id="c7aae-130">-IotEdgeDeviceAccessKey</span></span>
<span data-ttu-id="c7aae-131">Klawisz dostępu urządzenia Iot Edge</span><span class="sxs-lookup"><span data-stu-id="c7aae-131">Access key of the Iot Edge device</span></span>

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

### <span data-ttu-id="c7aae-132">-IotEdgeDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="c7aae-132">-IotEdgeDeviceConnectionString</span></span>
<span data-ttu-id="c7aae-133">Podaj ciąg połączenia urządzenia Edge</span><span class="sxs-lookup"><span data-stu-id="c7aae-133">Please provide connection string of Edge Device</span></span>

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

### <span data-ttu-id="c7aae-134">-IotEdgeDeviceId</span><span class="sxs-lookup"><span data-stu-id="c7aae-134">-IotEdgeDeviceId</span></span>
<span data-ttu-id="c7aae-135">Identyfikator urządzenia Edge Iot</span><span class="sxs-lookup"><span data-stu-id="c7aae-135">Id of the Iot Edge Device</span></span>

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

### <span data-ttu-id="c7aae-136">-IotHostHub</span><span class="sxs-lookup"><span data-stu-id="c7aae-136">-IotHostHub</span></span>
<span data-ttu-id="c7aae-137">Adres w witrynie Hosthub</span><span class="sxs-lookup"><span data-stu-id="c7aae-137">Hosthub address</span></span>

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

### <span data-ttu-id="c7aae-138">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c7aae-138">-Name</span></span>
<span data-ttu-id="c7aae-139">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="c7aae-139">Resource Name</span></span>

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

### <span data-ttu-id="c7aae-140">— Platforma</span><span class="sxs-lookup"><span data-stu-id="c7aae-140">-Platform</span></span>
<span data-ttu-id="c7aae-141">Udostępnij platformę, na przykład: Linux</span><span class="sxs-lookup"><span data-stu-id="c7aae-141">Provide the Platform, for ex: Linux</span></span>

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

### <span data-ttu-id="c7aae-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7aae-142">-ResourceGroupName</span></span>
<span data-ttu-id="c7aae-143">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="c7aae-143">Resource Group Name</span></span>

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

### <span data-ttu-id="c7aae-144">-RoleStatus</span><span class="sxs-lookup"><span data-stu-id="c7aae-144">-RoleStatus</span></span>
<span data-ttu-id="c7aae-145">Włączanie/wyłączanie stanu</span><span class="sxs-lookup"><span data-stu-id="c7aae-145">Provide the status enable/disable</span></span>

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

### <span data-ttu-id="c7aae-146">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c7aae-146">-Confirm</span></span>
<span data-ttu-id="c7aae-147">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c7aae-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7aae-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7aae-148">-WhatIf</span></span>
<span data-ttu-id="c7aae-149">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c7aae-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c7aae-150">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c7aae-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7aae-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7aae-151">CommonParameters</span></span>
<span data-ttu-id="c7aae-152">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7aae-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7aae-153">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c7aae-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7aae-154">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c7aae-154">INPUTS</span></span>

### <span data-ttu-id="c7aae-155">Brak</span><span class="sxs-lookup"><span data-stu-id="c7aae-155">None</span></span>

## <span data-ttu-id="c7aae-156">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c7aae-156">OUTPUTS</span></span>

### <span data-ttu-id="c7aae-157">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="c7aae-157">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="c7aae-158">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c7aae-158">NOTES</span></span>

## <span data-ttu-id="c7aae-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c7aae-159">RELATED LINKS</span></span>
