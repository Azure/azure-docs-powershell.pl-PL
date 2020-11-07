---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: CC306D8C-A5EE-4655-B686-E5A77CCE5042
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMChefExtension.md
ms.openlocfilehash: 25ddfd3fcb7d087db493e87bdd9781b2bbb77040
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716629"
---
# <span data-ttu-id="dc6a4-101">Set-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="dc6a4-101">Set-AzureRmVMChefExtension</span></span>

## <span data-ttu-id="dc6a4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dc6a4-102">SYNOPSIS</span></span>
<span data-ttu-id="dc6a4-103">Dodaje rozszerzenie Kuchmistrz do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="dc6a4-103">Adds a Chef extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc6a4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dc6a4-104">SYNTAX</span></span>

### <span data-ttu-id="dc6a4-105">Linux</span><span class="sxs-lookup"><span data-stu-id="dc6a4-105">Linux</span></span>
```
Set-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-TypeHandlerVersion] <String>]
 -ValidationPem <String> [-ClientRb <String>] [-BootstrapOptions <String>] [-JsonAttribute <String>]
 [-ChefDaemonInterval <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>]
 [-RunList <String>] [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Linux] [[-Location] <String>] [[-Name] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc6a4-106">Microsoft</span><span class="sxs-lookup"><span data-stu-id="dc6a4-106">Windows</span></span>
```
Set-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-TypeHandlerVersion] <String>]
 -ValidationPem <String> [-ClientRb <String>] [-BootstrapOptions <String>] [-JsonAttribute <String>]
 [-ChefDaemonInterval <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>]
 [-RunList <String>] [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Windows] [[-Location] <String>] [[-Name] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc6a4-107">Opis</span><span class="sxs-lookup"><span data-stu-id="dc6a4-107">DESCRIPTION</span></span>
<span data-ttu-id="dc6a4-108">Polecenie cmdlet **Set-AzureVMChefExtension** dodaje rozszerzenie Kuchmistrz do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="dc6a4-108">The **Set-AzureVMChefExtension** cmdlet adds the Chef extension to the virtual machine.</span></span>

## <span data-ttu-id="dc6a4-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dc6a4-109">EXAMPLES</span></span>

### <span data-ttu-id="dc6a4-110">Przykład 1: Dodawanie rozszerzenia Kuchmistrz do maszyny wirtualnej systemu Windows</span><span class="sxs-lookup"><span data-stu-id="dc6a4-110">Example 1: Add a Chef extension to a Windows virtual machine</span></span>
```
PS C:\> Set-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -ValidationPem "C:\my-org-validator.pem" -ClientRb "C:\client.rb" -RunList "Apache" -Daemon "service" -SecretFile "C:\my_encrypted_data_bag_secret" -Windows
```

<span data-ttu-id="dc6a4-111">To polecenie umożliwia dodanie rozszerzenia Kuchmistrz do maszyny wirtualnej systemu Windows o nazwie WindowsVM001.</span><span class="sxs-lookup"><span data-stu-id="dc6a4-111">This command adds a Chef extension to a Windows virtual machine named WindowsVM001.</span></span>
<span data-ttu-id="dc6a4-112">Po uruchomieniu maszyny wirtualnej Kuchmistrz Bootstrap na maszynie wirtualnej w celu uruchomienia programu Apache.</span><span class="sxs-lookup"><span data-stu-id="dc6a4-112">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>

### <span data-ttu-id="dc6a4-113">Przykład 2: Dodawanie rozszerzenia Kuchmistrz do maszyny wirtualnej Linux</span><span class="sxs-lookup"><span data-stu-id="dc6a4-113">Example 2: Add a Chef extension to a Linux virtual machine</span></span>
```
PS C:\> Set-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -ValidationPem "C:\my-org-validator.pem" -ClientRb "C:\client.rb" -RunList "Apache" -Secret "my_secret" -Linux
```

<span data-ttu-id="dc6a4-114">To polecenie umożliwia dodanie rozszerzenia Kuchmistrz do maszyny wirtualnej Linux o nazwie LinuxVM001.</span><span class="sxs-lookup"><span data-stu-id="dc6a4-114">This command adds a Chef extension to a Linux virtual machine named LinuxVM001.</span></span>
<span data-ttu-id="dc6a4-115">Po uruchomieniu maszyny wirtualnej Kuchmistrz Bootstrap na maszynie wirtualnej w celu uruchomienia programu Apache.</span><span class="sxs-lookup"><span data-stu-id="dc6a4-115">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>

### <span data-ttu-id="dc6a4-116">Przykład 3: Dodawanie rozszerzenia Kuchmistrz do maszyny wirtualnej systemu Windows przy użyciu opcji Bootstrap</span><span class="sxs-lookup"><span data-stu-id="dc6a4-116">Example 3: Add a Chef extension to a Windows virtual machine with bootstrap options</span></span>
```
PS C:\> Set-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup003" -VMName "WindowsVM002" -ValidationPem C:\my-org-validator.pem -ClientRb C:\client.rb -BootstrapOptions '{"chef_node_name":"your_node_name","chef_server_url":"https://api.opscode.com/organizations/some-org", "validation_client_name":"some-org-validator"}' -RunList "Apache" -Windows
```

<span data-ttu-id="dc6a4-117">To polecenie powoduje dodanie rozszerzenia Kuchmistrz do maszyny wirtualnej systemu Windows o nazwie WindowsVM002.</span><span class="sxs-lookup"><span data-stu-id="dc6a4-117">This command adds the Chef extension to a Windows virtual machine named WindowsVM002.</span></span>
<span data-ttu-id="dc6a4-118">Po uruchomieniu maszyny wirtualnej Kuchmistrz Bootstrap na maszynie wirtualnej w celu uruchomienia programu Apache.</span><span class="sxs-lookup"><span data-stu-id="dc6a4-118">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>
<span data-ttu-id="dc6a4-119">Po zakończeniu ładowania maszyna wirtualna odwołuje się do BootstrapOptions określonej w formacie JSON.</span><span class="sxs-lookup"><span data-stu-id="dc6a4-119">After bootstrapping, the virtual machine refers to the BootstrapOptions specified in JSON format.</span></span>

## <span data-ttu-id="dc6a4-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dc6a4-120">PARAMETERS</span></span>

### <span data-ttu-id="dc6a4-121">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="dc6a4-121">-AutoUpgradeMinorVersion</span></span>
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc6a4-122">-BootstrapOptions</span><span class="sxs-lookup"><span data-stu-id="dc6a4-122">-BootstrapOptions</span></span>
<span data-ttu-id="dc6a4-123">Określa ustawienia konfiguracji w opcji client_rb.</span><span class="sxs-lookup"><span data-stu-id="dc6a4-123">Specifies configuration settings in the client_rb option.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc6a4-124">-BootstrapVersion</span><span class="sxs-lookup"><span data-stu-id="dc6a4-124">-BootstrapVersion</span></span>
<span data-ttu-id="dc6a4-125">Określa wersję konfiguracji uruchamiania.</span><span class="sxs-lookup"><span data-stu-id="dc6a4-125">Specifies the version of the bootstrap configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc6a4-126">-ChefDaemonInterval</span><span class="sxs-lookup"><span data-stu-id="dc6a4-126">-ChefDaemonInterval</span></span>
<span data-ttu-id="dc6a4-127">Określa częstotliwość (w minutach) uruchamiania usługi Kuchmistrz.</span><span class="sxs-lookup"><span data-stu-id="dc6a4-127">Specifies the frequency (in minutes) at which the chef-service runs.</span></span> <span data-ttu-id="dc6a4-128">Jeśli nie chcesz, aby usługa Kuchmistrz była zainstalowana na platformie Azure VM, ustaw wartość 0 w tym polu.</span><span class="sxs-lookup"><span data-stu-id="dc6a4-128">If in case you don't want the chef-service to be installed on the Azure VM then set value as 0 in this field.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ChefServiceInterval

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc6a4-129">-ChefServerUrl</span><span class="sxs-lookup"><span data-stu-id="dc6a4-129">-ChefServerUrl</span></span>
<span data-ttu-id="dc6a4-130">Określa łącze serwera Kuchmistrz jako adres URL.</span><span class="sxs-lookup"><span data-stu-id="dc6a4-130">Specifies the Chef server link, as a URL.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc6a4-131">-ClientRb</span><span class="sxs-lookup"><span data-stu-id="dc6a4-131">-ClientRb</span></span>
<span data-ttu-id="dc6a4-132">Określa pełną ścieżkę klienta Kuchmistrz.</span><span class="sxs-lookup"><span data-stu-id="dc6a4-132">Specifies the full path of the Chef client.rb.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc6a4-133">-Demon</span><span class="sxs-lookup"><span data-stu-id="dc6a4-133">-Daemon</span></span>
<span data-ttu-id="dc6a4-134">Konfiguruje Kuchmistrz-Client w celu wykonania nienadzorowanej pracy.</span><span class="sxs-lookup"><span data-stu-id="dc6a4-134">Configures the chef-client service for unattended execution.</span></span> <span data-ttu-id="dc6a4-135">Platformą węzłową powinna być system Windows.</span><span class="sxs-lookup"><span data-stu-id="dc6a4-135">The node platform should be Windows.</span></span>
<span data-ttu-id="dc6a4-136">Dozwolone opcje: "Brak", "usługa" i "zadanie".</span><span class="sxs-lookup"><span data-stu-id="dc6a4-136">Allowed options: 'none','service' and 'task'.</span></span>
<span data-ttu-id="dc6a4-137">Brak — obecnie uniemożliwia skonfigurowanie usługi Kuchmistrz-Client jako usługi.</span><span class="sxs-lookup"><span data-stu-id="dc6a4-137">none - Currently prevents the chef-client service from being configured as a service.</span></span>
<span data-ttu-id="dc6a4-138">Usługa — konfiguruje Kuchmistrz-Client do automatycznego uruchamiania w tle jako usługi.</span><span class="sxs-lookup"><span data-stu-id="dc6a4-138">service - Configures the chef-client to run automatically in the background as a service.</span></span>
<span data-ttu-id="dc6a4-139">Task-konfiguruje Kuchmistrz-Client do automatycznego uruchamiania w tle jako zadania secheduled.</span><span class="sxs-lookup"><span data-stu-id="dc6a4-139">task - Configures the chef-client to run automatically in the background as a secheduled task.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: none, service, task

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc6a4-140">-Jsonattribute</span><span class="sxs-lookup"><span data-stu-id="dc6a4-140">-JsonAttribute</span></span>
<span data-ttu-id="dc6a4-141">Ciąg JSON do dodania do pierwszego uruchomienia Kuchmistrz-Client.</span><span class="sxs-lookup"><span data-stu-id="dc6a4-141">A JSON string to be added to the first run of chef-client.</span></span> <span data-ttu-id="dc6a4-142">na przykład-Jsonattribute "{" foo ":" bar "}"</span><span class="sxs-lookup"><span data-stu-id="dc6a4-142">e.g. -JsonAttribute '{"foo" : "bar"}'</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc6a4-143">-Linux</span><span class="sxs-lookup"><span data-stu-id="dc6a4-143">-Linux</span></span>
<span data-ttu-id="dc6a4-144">Wskazuje, że w tym poleceniu cmdlet jest tworzona maszyna wirtualna systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="dc6a4-144">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc6a4-145">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="dc6a4-145">-Location</span></span>
<span data-ttu-id="dc6a4-146">Określa lokalizację maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="dc6a4-146">Specifies the location of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc6a4-147">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="dc6a4-147">-Name</span></span>
<span data-ttu-id="dc6a4-148">Określa nazwę rozszerzenia Kuchmistrz.</span><span class="sxs-lookup"><span data-stu-id="dc6a4-148">Specifies the name of the Chef extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc6a4-149">-Nazwa_organizacji</span><span class="sxs-lookup"><span data-stu-id="dc6a4-149">-OrganizationName</span></span>
<span data-ttu-id="dc6a4-150">Określa nazwę organizacji rozszerzenia Kuchmistrz.</span><span class="sxs-lookup"><span data-stu-id="dc6a4-150">Specifies the organization name of the Chef extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc6a4-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc6a4-151">-ResourceGroupName</span></span>
<span data-ttu-id="dc6a4-152">Określa nazwę grupy zasobów zawierającej maszynę wirtualną.</span><span class="sxs-lookup"><span data-stu-id="dc6a4-152">Specifies the name of the resource group that contains the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc6a4-153">-RunList</span><span class="sxs-lookup"><span data-stu-id="dc6a4-153">-RunList</span></span>
<span data-ttu-id="dc6a4-154">Określa listę uruchamiania węzła Kuchmistrz.</span><span class="sxs-lookup"><span data-stu-id="dc6a4-154">Specifies the Chef node run list.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc6a4-155">-Secret</span><span class="sxs-lookup"><span data-stu-id="dc6a4-155">-Secret</span></span>
<span data-ttu-id="dc6a4-156">Klucz szyfrowania użyty do szyfrowania i odszyfrowywania wartości elementu worka danych.</span><span class="sxs-lookup"><span data-stu-id="dc6a4-156">The encryption key used to encrypt and decrypt the data bag item values.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc6a4-157">-SecretFile</span><span class="sxs-lookup"><span data-stu-id="dc6a4-157">-SecretFile</span></span>
<span data-ttu-id="dc6a4-158">Ścieżka do pliku zawierającego klucz szyfrowania użyty do szyfrowania i odszyfrowywania wartości elementu worka danych.</span><span class="sxs-lookup"><span data-stu-id="dc6a4-158">The path to the file that contains the encryption key used to encrypt and decrypt the data bag item values.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc6a4-159">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="dc6a4-159">-TypeHandlerVersion</span></span>
<span data-ttu-id="dc6a4-160">Określa wersję rozszerzenia, która ma być używana dla tej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="dc6a4-160">Specifies the version of the extension to use for this virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc6a4-161">-ValidationClientName</span><span class="sxs-lookup"><span data-stu-id="dc6a4-161">-ValidationClientName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc6a4-162">-ValidationPem</span><span class="sxs-lookup"><span data-stu-id="dc6a4-162">-ValidationPem</span></span>
<span data-ttu-id="dc6a4-163">Określa ścieżkę pliku modułu sprawdzania poprawności Kuchmistrz.</span><span class="sxs-lookup"><span data-stu-id="dc6a4-163">Specifies the Chef validator .pem file path</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc6a4-164">-VMName</span><span class="sxs-lookup"><span data-stu-id="dc6a4-164">-VMName</span></span>
<span data-ttu-id="dc6a4-165">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="dc6a4-165">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="dc6a4-166">To polecenie cmdlet umożliwia dodanie rozszerzenia Kuchmistrz dla maszyny wirtualnej, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="dc6a4-166">This cmdlet adds the Chef extension for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc6a4-167">-Windows</span><span class="sxs-lookup"><span data-stu-id="dc6a4-167">-Windows</span></span>
<span data-ttu-id="dc6a4-168">Wskazuje, że w tym poleceniu cmdlet jest tworzona maszyna wirtualna systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="dc6a4-168">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc6a4-169">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dc6a4-169">-Confirm</span></span>
<span data-ttu-id="dc6a4-170">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc6a4-170">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc6a4-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc6a4-171">-WhatIf</span></span>
<span data-ttu-id="dc6a4-172">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc6a4-172">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="dc6a4-173">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="dc6a4-173">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc6a4-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc6a4-174">CommonParameters</span></span>
<span data-ttu-id="dc6a4-175">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc6a4-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc6a4-176">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc6a4-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc6a4-177">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dc6a4-177">INPUTS</span></span>

### <span data-ttu-id="dc6a4-178">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="dc6a4-178">None</span></span>
<span data-ttu-id="dc6a4-179">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="dc6a4-179">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="dc6a4-180">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dc6a4-180">OUTPUTS</span></span>

## <span data-ttu-id="dc6a4-181">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dc6a4-181">NOTES</span></span>

## <span data-ttu-id="dc6a4-182">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dc6a4-182">RELATED LINKS</span></span>

[<span data-ttu-id="dc6a4-183">Get-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="dc6a4-183">Get-AzureRmVMChefExtension</span></span>](./Get-AzureRmVMChefExtension.md)

[<span data-ttu-id="dc6a4-184">Remove-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="dc6a4-184">Remove-AzureRmVMChefExtension</span></span>](./Remove-AzureRmVMChefExtension.md)
