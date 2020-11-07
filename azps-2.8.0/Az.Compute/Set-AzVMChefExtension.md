---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CC306D8C-A5EE-4655-B686-E5A77CCE5042
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmchefextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMChefExtension.md
ms.openlocfilehash: 22efab85694d7d2af359052b264a9aa932816f4e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706183"
---
# <span data-ttu-id="63f9f-101">Set-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="63f9f-101">Set-AzVMChefExtension</span></span>

## <span data-ttu-id="63f9f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="63f9f-102">SYNOPSIS</span></span>
<span data-ttu-id="63f9f-103">Dodaje rozszerzenie Kuchmistrz do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="63f9f-103">Adds a Chef extension to a virtual machine.</span></span>

## <span data-ttu-id="63f9f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="63f9f-104">SYNTAX</span></span>

### <span data-ttu-id="63f9f-105">Linux</span><span class="sxs-lookup"><span data-stu-id="63f9f-105">Linux</span></span>
```
Set-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-TypeHandlerVersion] <String>]
 -ValidationPem <String> [-ClientRb <String>] [-BootstrapOptions <String>] [-JsonAttribute <String>]
 [-ChefDaemonInterval <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>]
 [-RunList <String>] [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Linux] [[-Location] <String>] [[-Name] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63f9f-106">Microsoft</span><span class="sxs-lookup"><span data-stu-id="63f9f-106">Windows</span></span>
```
Set-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-TypeHandlerVersion] <String>]
 -ValidationPem <String> [-ClientRb <String>] [-BootstrapOptions <String>] [-JsonAttribute <String>]
 [-ChefDaemonInterval <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>]
 [-RunList <String>] [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Windows] [[-Location] <String>] [[-Name] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63f9f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="63f9f-107">DESCRIPTION</span></span>
<span data-ttu-id="63f9f-108">Polecenie cmdlet **Set-AzVMChefExtension** dodaje rozszerzenie Kuchmistrz do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="63f9f-108">The **Set-AzVMChefExtension** cmdlet adds the Chef extension to the virtual machine.</span></span>

## <span data-ttu-id="63f9f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="63f9f-109">EXAMPLES</span></span>

### <span data-ttu-id="63f9f-110">Przykład 1: Dodawanie rozszerzenia Kuchmistrz do maszyny wirtualnej systemu Windows</span><span class="sxs-lookup"><span data-stu-id="63f9f-110">Example 1: Add a Chef extension to a Windows virtual machine</span></span>
```
PS C:\> Set-AzVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -ValidationPem "C:\my-org-validator.pem" -ClientRb "C:\client.rb" -RunList "Apache" -Daemon "service" -SecretFile "C:\my_encrypted_data_bag_secret" -Windows
```

<span data-ttu-id="63f9f-111">To polecenie umożliwia dodanie rozszerzenia Kuchmistrz do maszyny wirtualnej systemu Windows o nazwie WindowsVM001.</span><span class="sxs-lookup"><span data-stu-id="63f9f-111">This command adds a Chef extension to a Windows virtual machine named WindowsVM001.</span></span>
<span data-ttu-id="63f9f-112">Po uruchomieniu maszyny wirtualnej Kuchmistrz Bootstrap na maszynie wirtualnej w celu uruchomienia programu Apache.</span><span class="sxs-lookup"><span data-stu-id="63f9f-112">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>

### <span data-ttu-id="63f9f-113">Przykład 2: Dodawanie rozszerzenia Kuchmistrz do maszyny wirtualnej Linux</span><span class="sxs-lookup"><span data-stu-id="63f9f-113">Example 2: Add a Chef extension to a Linux virtual machine</span></span>
```
PS C:\> Set-AzVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -ValidationPem "C:\my-org-validator.pem" -ClientRb "C:\client.rb" -RunList "Apache" -Secret "my_secret" -Linux
```

<span data-ttu-id="63f9f-114">To polecenie umożliwia dodanie rozszerzenia Kuchmistrz do maszyny wirtualnej Linux o nazwie LinuxVM001.</span><span class="sxs-lookup"><span data-stu-id="63f9f-114">This command adds a Chef extension to a Linux virtual machine named LinuxVM001.</span></span>
<span data-ttu-id="63f9f-115">Po uruchomieniu maszyny wirtualnej Kuchmistrz Bootstrap na maszynie wirtualnej w celu uruchomienia programu Apache.</span><span class="sxs-lookup"><span data-stu-id="63f9f-115">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>

### <span data-ttu-id="63f9f-116">Przykład 3: Dodawanie rozszerzenia Kuchmistrz do maszyny wirtualnej systemu Windows przy użyciu opcji Bootstrap</span><span class="sxs-lookup"><span data-stu-id="63f9f-116">Example 3: Add a Chef extension to a Windows virtual machine with bootstrap options</span></span>
```
PS C:\> Set-AzVMChefExtension -ResourceGroupName "ResourceGroup003" -VMName "WindowsVM002" -ValidationPem C:\my-org-validator.pem -ClientRb C:\client.rb -BootstrapOptions '{"chef_node_name":"your_node_name","chef_server_url":"https://api.opscode.com/organizations/some-org", "validation_client_name":"some-org-validator"}' -RunList "Apache" -Windows
```

<span data-ttu-id="63f9f-117">To polecenie powoduje dodanie rozszerzenia Kuchmistrz do maszyny wirtualnej systemu Windows o nazwie WindowsVM002.</span><span class="sxs-lookup"><span data-stu-id="63f9f-117">This command adds the Chef extension to a Windows virtual machine named WindowsVM002.</span></span>
<span data-ttu-id="63f9f-118">Po uruchomieniu maszyny wirtualnej Kuchmistrz Bootstrap na maszynie wirtualnej w celu uruchomienia programu Apache.</span><span class="sxs-lookup"><span data-stu-id="63f9f-118">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>
<span data-ttu-id="63f9f-119">Po zakończeniu ładowania maszyna wirtualna odwołuje się do BootstrapOptions określonej w formacie JSON.</span><span class="sxs-lookup"><span data-stu-id="63f9f-119">After bootstrapping, the virtual machine refers to the BootstrapOptions specified in JSON format.</span></span>

## <span data-ttu-id="63f9f-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="63f9f-120">PARAMETERS</span></span>

### <span data-ttu-id="63f9f-121">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="63f9f-121">-AutoUpgradeMinorVersion</span></span>
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

### <span data-ttu-id="63f9f-122">-BootstrapOptions</span><span class="sxs-lookup"><span data-stu-id="63f9f-122">-BootstrapOptions</span></span>
<span data-ttu-id="63f9f-123">Określa ustawienia konfiguracji w opcji client_rb.</span><span class="sxs-lookup"><span data-stu-id="63f9f-123">Specifies configuration settings in the client_rb option.</span></span>

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

### <span data-ttu-id="63f9f-124">-BootstrapVersion</span><span class="sxs-lookup"><span data-stu-id="63f9f-124">-BootstrapVersion</span></span>
<span data-ttu-id="63f9f-125">Określa wersję konfiguracji uruchamiania.</span><span class="sxs-lookup"><span data-stu-id="63f9f-125">Specifies the version of the bootstrap configuration.</span></span>

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

### <span data-ttu-id="63f9f-126">-ChefDaemonInterval</span><span class="sxs-lookup"><span data-stu-id="63f9f-126">-ChefDaemonInterval</span></span>
<span data-ttu-id="63f9f-127">Określa częstotliwość (w minutach) uruchamiania usługi Kuchmistrz.</span><span class="sxs-lookup"><span data-stu-id="63f9f-127">Specifies the frequency (in minutes) at which the chef-service runs.</span></span> <span data-ttu-id="63f9f-128">Jeśli nie chcesz, aby usługa Kuchmistrz była zainstalowana na platformie Azure VM, ustaw wartość 0 w tym polu.</span><span class="sxs-lookup"><span data-stu-id="63f9f-128">If in case you don't want the chef-service to be installed on the Azure VM then set value as 0 in this field.</span></span>

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

### <span data-ttu-id="63f9f-129">-ChefServerUrl</span><span class="sxs-lookup"><span data-stu-id="63f9f-129">-ChefServerUrl</span></span>
<span data-ttu-id="63f9f-130">Określa łącze serwera Kuchmistrz jako adres URL.</span><span class="sxs-lookup"><span data-stu-id="63f9f-130">Specifies the Chef server link, as a URL.</span></span>

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

### <span data-ttu-id="63f9f-131">-ClientRb</span><span class="sxs-lookup"><span data-stu-id="63f9f-131">-ClientRb</span></span>
<span data-ttu-id="63f9f-132">Określa pełną ścieżkę klienta Kuchmistrz.</span><span class="sxs-lookup"><span data-stu-id="63f9f-132">Specifies the full path of the Chef client.rb.</span></span>

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

### <span data-ttu-id="63f9f-133">-Demon</span><span class="sxs-lookup"><span data-stu-id="63f9f-133">-Daemon</span></span>
<span data-ttu-id="63f9f-134">Konfiguruje Kuchmistrz-Client w celu wykonania nienadzorowanej pracy.</span><span class="sxs-lookup"><span data-stu-id="63f9f-134">Configures the chef-client service for unattended execution.</span></span> <span data-ttu-id="63f9f-135">Platformą węzłową powinna być system Windows.</span><span class="sxs-lookup"><span data-stu-id="63f9f-135">The node platform should be Windows.</span></span>
<span data-ttu-id="63f9f-136">Dozwolone opcje: "Brak", "usługa" i "zadanie".</span><span class="sxs-lookup"><span data-stu-id="63f9f-136">Allowed options: 'none','service' and 'task'.</span></span>
<span data-ttu-id="63f9f-137">Brak — obecnie uniemożliwia skonfigurowanie usługi Kuchmistrz-Client jako usługi.</span><span class="sxs-lookup"><span data-stu-id="63f9f-137">none - Currently prevents the chef-client service from being configured as a service.</span></span>
<span data-ttu-id="63f9f-138">Usługa — konfiguruje Kuchmistrz-Client do automatycznego uruchamiania w tle jako usługi.</span><span class="sxs-lookup"><span data-stu-id="63f9f-138">service - Configures the chef-client to run automatically in the background as a service.</span></span>
<span data-ttu-id="63f9f-139">Task-konfiguruje Kuchmistrz-Client do automatycznego uruchamiania w tle jako zaplanowane zadanie.</span><span class="sxs-lookup"><span data-stu-id="63f9f-139">task - Configures the chef-client to run automatically in the background as a scheduled task.</span></span>

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

### <span data-ttu-id="63f9f-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63f9f-140">-DefaultProfile</span></span>
<span data-ttu-id="63f9f-141">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="63f9f-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63f9f-142">-Jsonattribute</span><span class="sxs-lookup"><span data-stu-id="63f9f-142">-JsonAttribute</span></span>
<span data-ttu-id="63f9f-143">Ciąg JSON do dodania do pierwszego uruchomienia Kuchmistrz-Client.</span><span class="sxs-lookup"><span data-stu-id="63f9f-143">A JSON string to be added to the first run of chef-client.</span></span> <span data-ttu-id="63f9f-144">na przykład-Jsonattribute "{" foo ":" bar "}"</span><span class="sxs-lookup"><span data-stu-id="63f9f-144">e.g. -JsonAttribute '{"foo" : "bar"}'</span></span>

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

### <span data-ttu-id="63f9f-145">-Linux</span><span class="sxs-lookup"><span data-stu-id="63f9f-145">-Linux</span></span>
<span data-ttu-id="63f9f-146">Wskazuje, że w tym poleceniu cmdlet jest tworzona maszyna wirtualna systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="63f9f-146">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

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

### <span data-ttu-id="63f9f-147">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="63f9f-147">-Location</span></span>
<span data-ttu-id="63f9f-148">Określa lokalizację maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="63f9f-148">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="63f9f-149">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="63f9f-149">-Name</span></span>
<span data-ttu-id="63f9f-150">Określa nazwę rozszerzenia Kuchmistrz.</span><span class="sxs-lookup"><span data-stu-id="63f9f-150">Specifies the name of the Chef extension.</span></span>

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

### <span data-ttu-id="63f9f-151">-Nowait</span><span class="sxs-lookup"><span data-stu-id="63f9f-151">-NoWait</span></span>
<span data-ttu-id="63f9f-152">Rozpoczyna operację i wraca natychmiast, zanim operacja zostanie ukończona.</span><span class="sxs-lookup"><span data-stu-id="63f9f-152">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="63f9f-153">W celu ustalenia, czy operacja została wykonana pomyślnie, użyj innego mechanizmu.</span><span class="sxs-lookup"><span data-stu-id="63f9f-153">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="63f9f-154">-Nazwa_organizacji</span><span class="sxs-lookup"><span data-stu-id="63f9f-154">-OrganizationName</span></span>
<span data-ttu-id="63f9f-155">Określa nazwę organizacji rozszerzenia Kuchmistrz.</span><span class="sxs-lookup"><span data-stu-id="63f9f-155">Specifies the organization name of the Chef extension.</span></span>

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

### <span data-ttu-id="63f9f-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63f9f-156">-ResourceGroupName</span></span>
<span data-ttu-id="63f9f-157">Określa nazwę grupy zasobów zawierającej maszynę wirtualną.</span><span class="sxs-lookup"><span data-stu-id="63f9f-157">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="63f9f-158">-RunList</span><span class="sxs-lookup"><span data-stu-id="63f9f-158">-RunList</span></span>
<span data-ttu-id="63f9f-159">Określa listę uruchamiania węzła Kuchmistrz.</span><span class="sxs-lookup"><span data-stu-id="63f9f-159">Specifies the Chef node run list.</span></span>

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

### <span data-ttu-id="63f9f-160">-Secret</span><span class="sxs-lookup"><span data-stu-id="63f9f-160">-Secret</span></span>
<span data-ttu-id="63f9f-161">Klucz szyfrowania użyty do szyfrowania i odszyfrowywania wartości elementu worka danych.</span><span class="sxs-lookup"><span data-stu-id="63f9f-161">The encryption key used to encrypt and decrypt the data bag item values.</span></span>

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

### <span data-ttu-id="63f9f-162">-SecretFile</span><span class="sxs-lookup"><span data-stu-id="63f9f-162">-SecretFile</span></span>
<span data-ttu-id="63f9f-163">Ścieżka do pliku zawierającego klucz szyfrowania użyty do szyfrowania i odszyfrowywania wartości elementu worka danych.</span><span class="sxs-lookup"><span data-stu-id="63f9f-163">The path to the file that contains the encryption key used to encrypt and decrypt the data bag item values.</span></span>

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

### <span data-ttu-id="63f9f-164">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="63f9f-164">-TypeHandlerVersion</span></span>
<span data-ttu-id="63f9f-165">Określa wersję rozszerzenia, która ma być używana dla tej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="63f9f-165">Specifies the version of the extension to use for this virtual machine.</span></span>

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

### <span data-ttu-id="63f9f-166">-ValidationClientName</span><span class="sxs-lookup"><span data-stu-id="63f9f-166">-ValidationClientName</span></span>
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

### <span data-ttu-id="63f9f-167">-ValidationPem</span><span class="sxs-lookup"><span data-stu-id="63f9f-167">-ValidationPem</span></span>
<span data-ttu-id="63f9f-168">Określa ścieżkę pliku modułu sprawdzania poprawności Kuchmistrz.</span><span class="sxs-lookup"><span data-stu-id="63f9f-168">Specifies the Chef validator .pem file path</span></span>

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

### <span data-ttu-id="63f9f-169">-VMName</span><span class="sxs-lookup"><span data-stu-id="63f9f-169">-VMName</span></span>
<span data-ttu-id="63f9f-170">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="63f9f-170">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="63f9f-171">To polecenie cmdlet umożliwia dodanie rozszerzenia Kuchmistrz dla maszyny wirtualnej, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="63f9f-171">This cmdlet adds the Chef extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="63f9f-172">-Windows</span><span class="sxs-lookup"><span data-stu-id="63f9f-172">-Windows</span></span>
<span data-ttu-id="63f9f-173">Wskazuje, że w tym poleceniu cmdlet jest tworzona maszyna wirtualna systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="63f9f-173">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

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

### <span data-ttu-id="63f9f-174">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="63f9f-174">-Confirm</span></span>
<span data-ttu-id="63f9f-175">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63f9f-175">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63f9f-176">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63f9f-176">-WhatIf</span></span>
<span data-ttu-id="63f9f-177">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63f9f-177">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63f9f-178">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="63f9f-178">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63f9f-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63f9f-179">CommonParameters</span></span>
<span data-ttu-id="63f9f-180">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63f9f-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63f9f-181">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="63f9f-181">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63f9f-182">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="63f9f-182">INPUTS</span></span>

### <span data-ttu-id="63f9f-183">System. String</span><span class="sxs-lookup"><span data-stu-id="63f9f-183">System.String</span></span>

### <span data-ttu-id="63f9f-184">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="63f9f-184">System.Boolean</span></span>

## <span data-ttu-id="63f9f-185">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="63f9f-185">OUTPUTS</span></span>

### <span data-ttu-id="63f9f-186">Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="63f9f-186">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="63f9f-187">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="63f9f-187">NOTES</span></span>

## <span data-ttu-id="63f9f-188">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="63f9f-188">RELATED LINKS</span></span>

[<span data-ttu-id="63f9f-189">Get-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="63f9f-189">Get-AzVMChefExtension</span></span>](./Get-AzVMChefExtension.md)

[<span data-ttu-id="63f9f-190">Remove-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="63f9f-190">Remove-AzVMChefExtension</span></span>](./Remove-AzVMChefExtension.md)
