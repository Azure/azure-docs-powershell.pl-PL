---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CC306D8C-A5EE-4655-B686-E5A77CCE5042
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmchefextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMChefExtension.md
ms.openlocfilehash: 2821e9404fe4101415aa04a8b0d331b3066563df
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177475"
---
# <span data-ttu-id="cc945-101">Set-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="cc945-101">Set-AzVMChefExtension</span></span>

## <span data-ttu-id="cc945-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc945-102">SYNOPSIS</span></span>
<span data-ttu-id="cc945-103">Dodaje rozszerzenie do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="cc945-103">Adds a Chef extension to a virtual machine.</span></span>

## <span data-ttu-id="cc945-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="cc945-104">SYNTAX</span></span>

### <span data-ttu-id="cc945-105">Linux</span><span class="sxs-lookup"><span data-stu-id="cc945-105">Linux</span></span>
```
Set-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-TypeHandlerVersion] <String>]
 -ValidationPem <String> [-ClientRb <String>] [-BootstrapOptions <String>] [-JsonAttribute <String>]
 [-ChefDaemonInterval <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>]
 [-RunList <String>] [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Linux] [[-Location] <String>] [[-Name] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc945-106">Windows</span><span class="sxs-lookup"><span data-stu-id="cc945-106">Windows</span></span>
```
Set-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-TypeHandlerVersion] <String>]
 -ValidationPem <String> [-ClientRb <String>] [-BootstrapOptions <String>] [-JsonAttribute <String>]
 [-ChefDaemonInterval <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>]
 [-RunList <String>] [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Windows] [[-Location] <String>] [[-Name] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc945-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="cc945-107">DESCRIPTION</span></span>
<span data-ttu-id="cc945-108">Polecenie **cmdlet Set-AzVMChefExtension** dodaje rozszerzenie Do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="cc945-108">The **Set-AzVMChefExtension** cmdlet adds the Chef extension to the virtual machine.</span></span>

## <span data-ttu-id="cc945-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="cc945-109">EXAMPLES</span></span>

### <span data-ttu-id="cc945-110">Przykład 1. Dodawanie rozszerzenia Do maszyny wirtualnej systemu Windows</span><span class="sxs-lookup"><span data-stu-id="cc945-110">Example 1: Add a Chef extension to a Windows virtual machine</span></span>
```
PS C:\> Set-AzVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -ValidationPem "C:\my-org-validator.pem" -ClientRb "C:\client.rb" -RunList "Apache" -Daemon "service" -SecretFile "C:\my_encrypted_data_bag_secret" -Windows
```

<span data-ttu-id="cc945-111">To polecenie powoduje dodanie rozszerzenia do maszyny wirtualnej systemu Windows o nazwie WindowsVM001.</span><span class="sxs-lookup"><span data-stu-id="cc945-111">This command adds a Chef extension to a Windows virtual machine named WindowsVM001.</span></span>
<span data-ttu-id="cc945-112">Gdy zaczyna się maszyny wirtualnej, Bootstraps maszyny wirtualnej, aby uruchomić Gryna.</span><span class="sxs-lookup"><span data-stu-id="cc945-112">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>

### <span data-ttu-id="cc945-113">Przykład 2. Dodawanie rozszerzenia do maszyny wirtualnej systemu Linux</span><span class="sxs-lookup"><span data-stu-id="cc945-113">Example 2: Add a Chef extension to a Linux virtual machine</span></span>
```
PS C:\> Set-AzVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -ValidationPem "C:\my-org-validator.pem" -ClientRb "C:\client.rb" -RunList "Apache" -Secret "my_secret" -Linux
```

<span data-ttu-id="cc945-114">To polecenie dodaje rozszerzenie do maszyny wirtualnej systemu Linux o nazwie LinuxVM001.</span><span class="sxs-lookup"><span data-stu-id="cc945-114">This command adds a Chef extension to a Linux virtual machine named LinuxVM001.</span></span>
<span data-ttu-id="cc945-115">Gdy zaczyna się maszyny wirtualnej, Bootstraps maszyny wirtualnej, aby uruchomić Gryna.</span><span class="sxs-lookup"><span data-stu-id="cc945-115">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>

### <span data-ttu-id="cc945-116">Przykład 3. Dodanie rozszerzenia do maszyny wirtualnej systemu Windows z opcjami bootstrap</span><span class="sxs-lookup"><span data-stu-id="cc945-116">Example 3: Add a Chef extension to a Windows virtual machine with bootstrap options</span></span>
```
PS C:\> Set-AzVMChefExtension -ResourceGroupName "ResourceGroup003" -VMName "WindowsVM002" -ValidationPem C:\my-org-validator.pem -ClientRb C:\client.rb -BootstrapOptions '{"chef_node_name":"your_node_name","chef_server_url":"https://api.opscode.com/organizations/some-org", "validation_client_name":"some-org-validator"}' -RunList "Apache" -Windows
```

<span data-ttu-id="cc945-117">To polecenie dodaje rozszerzenie do maszyny wirtualnej systemu Windows o nazwie WindowsVM002.</span><span class="sxs-lookup"><span data-stu-id="cc945-117">This command adds the Chef extension to a Windows virtual machine named WindowsVM002.</span></span>
<span data-ttu-id="cc945-118">Po uruchomieniu maszyny wirtualnej, Bootstraps maszyny wirtualnej, aby uruchomić Oprogramowanie.</span><span class="sxs-lookup"><span data-stu-id="cc945-118">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>
<span data-ttu-id="cc945-119">Po bootstrapping, maszyny wirtualnej odwołuje się do BootstrapOptions określonych w formacie JSON.</span><span class="sxs-lookup"><span data-stu-id="cc945-119">After bootstrapping, the virtual machine refers to the BootstrapOptions specified in JSON format.</span></span>

## <span data-ttu-id="cc945-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cc945-120">PARAMETERS</span></span>

### <span data-ttu-id="cc945-121">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="cc945-121">-AutoUpgradeMinorVersion</span></span>
```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc945-122">-BootstrapOptions</span><span class="sxs-lookup"><span data-stu-id="cc945-122">-BootstrapOptions</span></span>
<span data-ttu-id="cc945-123">Określa ustawienia konfiguracji w client_rb konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="cc945-123">Specifies configuration settings in the client_rb option.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc945-124">-BootstrapVersion</span><span class="sxs-lookup"><span data-stu-id="cc945-124">-BootstrapVersion</span></span>
<span data-ttu-id="cc945-125">Określa wersję konfiguracji bootstrap.</span><span class="sxs-lookup"><span data-stu-id="cc945-125">Specifies the version of the bootstrap configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc945-126">- NadaemonInterval</span><span class="sxs-lookup"><span data-stu-id="cc945-126">-ChefDaemonInterval</span></span>
<span data-ttu-id="cc945-127">Określa częstotliwość (w minutach) uruchamianą przez usługę.</span><span class="sxs-lookup"><span data-stu-id="cc945-127">Specifies the frequency (in minutes) at which the chef-service runs.</span></span> <span data-ttu-id="cc945-128">Jeśli nie chcesz, aby usługa została zainstalowana na maszyny wirtualnej Azure, ustaw w tym polu wartość 0.</span><span class="sxs-lookup"><span data-stu-id="cc945-128">If in case you don't want the chef-service to be installed on the Azure VM then set value as 0 in this field.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ChefServiceInterval

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc945-129">-ServerUrl</span><span class="sxs-lookup"><span data-stu-id="cc945-129">-ChefServerUrl</span></span>
<span data-ttu-id="cc945-130">Określa link serwera Oad jako adres URL.</span><span class="sxs-lookup"><span data-stu-id="cc945-130">Specifies the Chef server link, as a URL.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc945-131">-ClientRb</span><span class="sxs-lookup"><span data-stu-id="cc945-131">-ClientRb</span></span>
<span data-ttu-id="cc945-132">Określa pełną ścieżkę pliku client.rb.</span><span class="sxs-lookup"><span data-stu-id="cc945-132">Specifies the full path of the Chef client.rb.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc945-133">-Daemon</span><span class="sxs-lookup"><span data-stu-id="cc945-133">-Daemon</span></span>
<span data-ttu-id="cc945-134">Konfiguruje usługę po stronie klienta w celu wykonywania bez nadzoru.</span><span class="sxs-lookup"><span data-stu-id="cc945-134">Configures the chef-client service for unattended execution.</span></span> <span data-ttu-id="cc945-135">Platformą węzła powinna być system Windows.</span><span class="sxs-lookup"><span data-stu-id="cc945-135">The node platform should be Windows.</span></span>
<span data-ttu-id="cc945-136">Dozwolone opcje: "brak", "usługa" i "zadanie".</span><span class="sxs-lookup"><span data-stu-id="cc945-136">Allowed options: 'none','service' and 'task'.</span></span>
<span data-ttu-id="cc945-137">none — obecnie uniemożliwia skonfigurowanie usługi klient-klient jako usługi.</span><span class="sxs-lookup"><span data-stu-id="cc945-137">none - Currently prevents the chef-client service from being configured as a service.</span></span>
<span data-ttu-id="cc945-138">usługa — konfiguruje klienta, który ma być uruchamiany automatycznie w tle jako usługa.</span><span class="sxs-lookup"><span data-stu-id="cc945-138">service - Configures the chef-client to run automatically in the background as a service.</span></span>
<span data-ttu-id="cc945-139">zadanie — konfiguruje klienta, który ma być uruchamiany automatycznie w tle jako zaplanowane zadanie.</span><span class="sxs-lookup"><span data-stu-id="cc945-139">task - Configures the chef-client to run automatically in the background as a scheduled task.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: none, service, task

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc945-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc945-140">-DefaultProfile</span></span>
<span data-ttu-id="cc945-141">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="cc945-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc945-142">-JsonAttribute</span><span class="sxs-lookup"><span data-stu-id="cc945-142">-JsonAttribute</span></span>
<span data-ttu-id="cc945-143">Ciąg JSON, który ma zostać dodany do pierwszego uruchomienia klienta-klienta.</span><span class="sxs-lookup"><span data-stu-id="cc945-143">A JSON string to be added to the first run of chef-client.</span></span> <span data-ttu-id="cc945-144">np. -JsonAttribute '{"foo": "bar"}'</span><span class="sxs-lookup"><span data-stu-id="cc945-144">e.g. -JsonAttribute '{"foo" : "bar"}'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc945-145">— Linux</span><span class="sxs-lookup"><span data-stu-id="cc945-145">-Linux</span></span>
<span data-ttu-id="cc945-146">Wskazuje, że to polecenie cmdlet tworzy maszynę wirtualną systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="cc945-146">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc945-147">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="cc945-147">-Location</span></span>
<span data-ttu-id="cc945-148">Określa lokalizację maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="cc945-148">Specifies the location of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc945-149">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="cc945-149">-Name</span></span>
<span data-ttu-id="cc945-150">Określa nazwę rozszerzenia Doc.</span><span class="sxs-lookup"><span data-stu-id="cc945-150">Specifies the name of the Chef extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc945-151">-NoWait</span><span class="sxs-lookup"><span data-stu-id="cc945-151">-NoWait</span></span>
<span data-ttu-id="cc945-152">Rozpoczyna operację i zwraca bezpośrednio przed jej ukończeniem.</span><span class="sxs-lookup"><span data-stu-id="cc945-152">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="cc945-153">Aby ustalić, czy operacja została pomyślnie ukończona, użyj innego mechanizmu.</span><span class="sxs-lookup"><span data-stu-id="cc945-153">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="cc945-154">-OrganizationName</span><span class="sxs-lookup"><span data-stu-id="cc945-154">-OrganizationName</span></span>
<span data-ttu-id="cc945-155">Określa nazwę organizacji rozszerzenia Doc.</span><span class="sxs-lookup"><span data-stu-id="cc945-155">Specifies the organization name of the Chef extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc945-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc945-156">-ResourceGroupName</span></span>
<span data-ttu-id="cc945-157">Określa nazwę grupy zasobów zawierającej maszynę wirtualną.</span><span class="sxs-lookup"><span data-stu-id="cc945-157">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="cc945-158">-RunList</span><span class="sxs-lookup"><span data-stu-id="cc945-158">-RunList</span></span>
<span data-ttu-id="cc945-159">Określa listę uruchamiania węzła Węzeł Węzeł.</span><span class="sxs-lookup"><span data-stu-id="cc945-159">Specifies the Chef node run list.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc945-160">- Tajna</span><span class="sxs-lookup"><span data-stu-id="cc945-160">-Secret</span></span>
<span data-ttu-id="cc945-161">Klucz szyfrowania używany do szyfrowania i odszyfrowywania wartości elementów worka danych.</span><span class="sxs-lookup"><span data-stu-id="cc945-161">The encryption key used to encrypt and decrypt the data bag item values.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc945-162">-SecretFile</span><span class="sxs-lookup"><span data-stu-id="cc945-162">-SecretFile</span></span>
<span data-ttu-id="cc945-163">Ścieżka do pliku zawierającego klucz szyfrowania używany do szyfrowania i odszyfrowywania wartości elementów worka danych.</span><span class="sxs-lookup"><span data-stu-id="cc945-163">The path to the file that contains the encryption key used to encrypt and decrypt the data bag item values.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc945-164">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="cc945-164">-TypeHandlerVersion</span></span>
<span data-ttu-id="cc945-165">Określa wersję rozszerzenia do użycia dla tej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="cc945-165">Specifies the version of the extension to use for this virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc945-166">-ValidationClientName</span><span class="sxs-lookup"><span data-stu-id="cc945-166">-ValidationClientName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc945-167">-ValidationPem</span><span class="sxs-lookup"><span data-stu-id="cc945-167">-ValidationPem</span></span>
<span data-ttu-id="cc945-168">Określa ścieżkę pliku pem sprawdzania prawidłowego sprawdzania prawidłowego pliku</span><span class="sxs-lookup"><span data-stu-id="cc945-168">Specifies the Chef validator .pem file path</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc945-169">-NAZWA.MASZYNY.WIRTUALNEJ</span><span class="sxs-lookup"><span data-stu-id="cc945-169">-VMName</span></span>
<span data-ttu-id="cc945-170">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="cc945-170">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="cc945-171">To polecenie cmdlet dodaje rozszerzenie do maszyny wirtualnej, które określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="cc945-171">This cmdlet adds the Chef extension for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc945-172">— Windows</span><span class="sxs-lookup"><span data-stu-id="cc945-172">-Windows</span></span>
<span data-ttu-id="cc945-173">Wskazuje, że to polecenie cmdlet tworzy maszynę wirtualną systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="cc945-173">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc945-174">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cc945-174">-Confirm</span></span>
<span data-ttu-id="cc945-175">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="cc945-175">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc945-176">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc945-176">-WhatIf</span></span>
<span data-ttu-id="cc945-177">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc945-177">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc945-178">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="cc945-178">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc945-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc945-179">CommonParameters</span></span>
<span data-ttu-id="cc945-180">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc945-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc945-181">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cc945-181">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc945-182">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cc945-182">INPUTS</span></span>

### <span data-ttu-id="cc945-183">System.String</span><span class="sxs-lookup"><span data-stu-id="cc945-183">System.String</span></span>

### <span data-ttu-id="cc945-184">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cc945-184">System.Boolean</span></span>

## <span data-ttu-id="cc945-185">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cc945-185">OUTPUTS</span></span>

### <span data-ttu-id="cc945-186">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="cc945-186">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="cc945-187">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="cc945-187">NOTES</span></span>

## <span data-ttu-id="cc945-188">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cc945-188">RELATED LINKS</span></span>

[<span data-ttu-id="cc945-189">Get-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="cc945-189">Get-AzVMChefExtension</span></span>](./Get-AzVMChefExtension.md)

[<span data-ttu-id="cc945-190">Remove-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="cc945-190">Remove-AzVMChefExtension</span></span>](./Remove-AzVMChefExtension.md)
