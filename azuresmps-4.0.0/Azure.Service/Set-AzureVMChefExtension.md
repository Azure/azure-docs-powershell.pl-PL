---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 021D4624-AE78-4FBE-B1DE-A8A84DF1FC90
online version: ''
schema: 2.0.0
ms.openlocfilehash: 52c3a26887e42884025234ba5f1a7330c258e903
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055011"
---
# <span data-ttu-id="23bcb-101">Set-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="23bcb-101">Set-AzureVMChefExtension</span></span>

## <span data-ttu-id="23bcb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="23bcb-102">SYNOPSIS</span></span>
<span data-ttu-id="23bcb-103">Dodaje rozszerzenie Kuchmistrz do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="23bcb-103">Adds the Chef extension to the virtual machine.</span></span>

## <span data-ttu-id="23bcb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="23bcb-104">SYNTAX</span></span>

### <span data-ttu-id="23bcb-105">Windows (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="23bcb-105">Windows (Default)</span></span>
```
Set-AzureVMChefExtension [-Version <String>] -ValidationPem <String> [-ClientRb <String>]
 [-BootstrapOptions <String>] [-RunList <String>] [-JsonAttribute <String>] [-ChefDaemonInterval <String>]
 [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>] [-Windows]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="23bcb-106">Linux</span><span class="sxs-lookup"><span data-stu-id="23bcb-106">Linux</span></span>
```
Set-AzureVMChefExtension [-Version <String>] -ValidationPem <String> [-ClientRb <String>]
 [-BootstrapOptions <String>] [-RunList <String>] [-JsonAttribute <String>] [-ChefDaemonInterval <String>]
 [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>] [-Linux]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="23bcb-107">Opis</span><span class="sxs-lookup"><span data-stu-id="23bcb-107">DESCRIPTION</span></span>
<span data-ttu-id="23bcb-108">Polecenie cmdlet **Set-AzureVMChefExtension** dodaje rozszerzenie Kuchmistrz do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="23bcb-108">The **Set-AzureVMChefExtension** cmdlet adds the Chef extension to the virtual machine.</span></span>

## <span data-ttu-id="23bcb-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="23bcb-109">EXAMPLES</span></span>

### <span data-ttu-id="23bcb-110">Przykład 1: Dodawanie rozszerzenia Kuchmistrz do maszyny wirtualnej systemu Windows</span><span class="sxs-lookup"><span data-stu-id="23bcb-110">Example 1: Add a Chef extension to a Windows virtual machine</span></span>
```
PS C:\> Set-AzureVMChefExtension -VM $VM -ValidationPem "C:\\myorg-validator.pem" -ClientRb "C:\\client.rb" -RunList "Apache" -Windows;
```

<span data-ttu-id="23bcb-111">To polecenie umożliwia dodanie rozszerzenia Kuchmistrz do maszyny wirtualnej systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="23bcb-111">This command adds a Chef extension to a Windows virtual machine.</span></span>
<span data-ttu-id="23bcb-112">Po odebraniu maszyny wirtualnej jest ona uruchamiana z systemem Kuchmistrz i działa na nim program Apache.</span><span class="sxs-lookup"><span data-stu-id="23bcb-112">When the virtual machine comes up, it is bootstrapped with Chef and runs Apache on it.</span></span>

### <span data-ttu-id="23bcb-113">Przykład 2: Dodawanie rozszerzenia Kuchmistrz do maszyny wirtualnej systemu Windows z załadowaniem</span><span class="sxs-lookup"><span data-stu-id="23bcb-113">Example 2: Add a Chef extension to a Windows virtual machine with bootstrapping</span></span>
```
PS C:\> Set-AzureVMChefExtension -VM $VM -ValidationPem "C:\\myorg-validator.pem" -BootstrapOptions '{"chef_node_name":"your_node_name","chef_server_url":"https://api.opscode.com/organizations/some-org", "validation_client_name":"some-org-validator"}' -RunList "Apache" -Windows;
```

<span data-ttu-id="23bcb-114">To polecenie powoduje dodanie rozszerzenia Kuchmistrz do maszyny wirtualnej systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="23bcb-114">This command adds the Chef extension to a Windows virtual machine.</span></span>
<span data-ttu-id="23bcb-115">Po uruchomieniu maszyny wirtualnej jest ona inicjowana przy użyciu Kuchmistrz i działa na nim program Apache.</span><span class="sxs-lookup"><span data-stu-id="23bcb-115">When the virtual machine launches, it is bootstrapped with Chef and runs Apache on it.</span></span>
<span data-ttu-id="23bcb-116">Po zakończeniu ładowania maszyna wirtualna odwołuje się do *BootstrapOptions* określonej w formacie JSON.</span><span class="sxs-lookup"><span data-stu-id="23bcb-116">After bootstrapping, the virtual machine refers to the *BootstrapOptions* specified in JSON format.</span></span>

### <span data-ttu-id="23bcb-117">Przykład 3: Dodawanie rozszerzenia Kuchmistrz do maszyny wirtualnej systemu Windows i instalowanie oprogramowania Apache i GIT</span><span class="sxs-lookup"><span data-stu-id="23bcb-117">Example 3: Add a Chef extension to a Windows virtual machine and install Apache and GIT</span></span>
```
PS C:\> Set-AzureVMChefExtension -VM $VM -ValidationPem "C:\\myorg-validator.pem" -ChefServerUrl "http://ipaddress:port" -ValidationClientName "MyOrg-Validator" -RunList "apache, git" -Windows;
```

<span data-ttu-id="23bcb-118">To polecenie powoduje dodanie rozszerzenia Kuchmistrz do maszyny wirtualnej systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="23bcb-118">This command adds the Chef extension to a Windows virtual machine.</span></span>
<span data-ttu-id="23bcb-119">Po uruchomieniu maszyny wirtualnej jest ona inicjowana z usługą Kuchmistrz i jest instalowana aplikacja Apache i GIT.</span><span class="sxs-lookup"><span data-stu-id="23bcb-119">When the virtual machine launches, it is bootstrapped with Chef and have Apache and GIT installed.</span></span>
<span data-ttu-id="23bcb-120">Jeśli nie podasz klienta. RB, musisz podać adres URL serwera Kuchmistrz i nazwę klienta weryfikacji.</span><span class="sxs-lookup"><span data-stu-id="23bcb-120">If you do not provide the client.rb, you need to provide the Chef server URL and validation client name.</span></span>

### <span data-ttu-id="23bcb-121">Przykład 4: Dodawanie rozszerzenia Kuchmistrz do maszyny wirtualnej Linux</span><span class="sxs-lookup"><span data-stu-id="23bcb-121">Example 4: Add a Chef extension to a Linux virtual machine</span></span>
```
PS C:\> Set-AzureVMChefExtension -VM $VM -ValidationPem "C:\\myorg-validator.pem" -ChefServerUrl "http://ipaddress:port" -OrganizationName "MyOrg" -Linux;
```

<span data-ttu-id="23bcb-122">To polecenie dodaje rozszerzenie Kuchmistrz do maszyny wirtualnej Linux.</span><span class="sxs-lookup"><span data-stu-id="23bcb-122">This command adds the Chef extension to a Linux virtual machine.</span></span>
<span data-ttu-id="23bcb-123">Po uruchomieniu maszyny wirtualnej jest ona inicjowana przy użyciu Kuchmistrz.</span><span class="sxs-lookup"><span data-stu-id="23bcb-123">When the virtual machine launches, it is bootstrapped with Chef.</span></span>
<span data-ttu-id="23bcb-124">Jeśli nie podasz klienta. RB, musisz podać adres URL i organizację serwera Kuchmistrz.</span><span class="sxs-lookup"><span data-stu-id="23bcb-124">If you do not provide the client.rb, you need to provide the Chef server URL and organization.</span></span>

## <span data-ttu-id="23bcb-125">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="23bcb-125">PARAMETERS</span></span>

### <span data-ttu-id="23bcb-126">-BootstrapOptions</span><span class="sxs-lookup"><span data-stu-id="23bcb-126">-BootstrapOptions</span></span>
<span data-ttu-id="23bcb-127">Określa opcje uruchamiania w formacie notacji kodu JavaScript (kod JSON).</span><span class="sxs-lookup"><span data-stu-id="23bcb-127">Specifies bootstrap options in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="23bcb-128">-BootstrapVersion</span><span class="sxs-lookup"><span data-stu-id="23bcb-128">-BootstrapVersion</span></span>
<span data-ttu-id="23bcb-129">Określa wersję klienta Kuchmistrz, która jest instalowana wraz z rozszerzeniem.</span><span class="sxs-lookup"><span data-stu-id="23bcb-129">Specifies the version of the Chef client that is installed together with the extension.</span></span>

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

### <span data-ttu-id="23bcb-130">-ChefDaemonInterval</span><span class="sxs-lookup"><span data-stu-id="23bcb-130">-ChefDaemonInterval</span></span>
<span data-ttu-id="23bcb-131">Określa częstotliwość (w minutach) uruchamiania usługi Kuchmistrz.</span><span class="sxs-lookup"><span data-stu-id="23bcb-131">Specifies the frequency (in minutes) at which the chef-service runs.</span></span> <span data-ttu-id="23bcb-132">Jeśli nie chcesz, aby usługa Kuchmistrz była zainstalowana na platformie Azure VM, ustaw wartość 0 w tym polu.</span><span class="sxs-lookup"><span data-stu-id="23bcb-132">If in case you don't want the chef-service to be installed on the Azure VM then set value as 0 in this field.</span></span>

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

### <span data-ttu-id="23bcb-133">-ChefServerUrl</span><span class="sxs-lookup"><span data-stu-id="23bcb-133">-ChefServerUrl</span></span>
<span data-ttu-id="23bcb-134">Określa adres URL serwera Kuchmistrz.</span><span class="sxs-lookup"><span data-stu-id="23bcb-134">Specifies the URL of the Chef server.</span></span>

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

### <span data-ttu-id="23bcb-135">-ClientRb</span><span class="sxs-lookup"><span data-stu-id="23bcb-135">-ClientRb</span></span>
<span data-ttu-id="23bcb-136">Określa pełną ścieżkę klienta Kuchmistrz.</span><span class="sxs-lookup"><span data-stu-id="23bcb-136">Specifies the full path of the Chef client.rb.</span></span>

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

### <span data-ttu-id="23bcb-137">-Demon</span><span class="sxs-lookup"><span data-stu-id="23bcb-137">-Daemon</span></span>
<span data-ttu-id="23bcb-138">Konfiguruje Kuchmistrz-Client w celu wykonania nienadzorowanej pracy.</span><span class="sxs-lookup"><span data-stu-id="23bcb-138">Configures the chef-client service for unattended execution.</span></span> <span data-ttu-id="23bcb-139">Platformą węzłową powinna być system Windows.</span><span class="sxs-lookup"><span data-stu-id="23bcb-139">The node platform should be Windows.</span></span>
<span data-ttu-id="23bcb-140">Dozwolone opcje: "Brak", "usługa" i "zadanie".</span><span class="sxs-lookup"><span data-stu-id="23bcb-140">Allowed options: 'none','service' and 'task'.</span></span>
<span data-ttu-id="23bcb-141">Brak — obecnie uniemożliwia skonfigurowanie usługi Kuchmistrz-Client jako usługi.</span><span class="sxs-lookup"><span data-stu-id="23bcb-141">none - Currently prevents the chef-client service from being configured as a service.</span></span>
<span data-ttu-id="23bcb-142">Usługa — konfiguruje Kuchmistrz-Client do automatycznego uruchamiania w tle jako usługi.</span><span class="sxs-lookup"><span data-stu-id="23bcb-142">service - Configures the chef-client to run automatically in the background as a service.</span></span>
<span data-ttu-id="23bcb-143">Task-konfiguruje Kuchmistrz-Client do automatycznego uruchamiania w tle jako zadania secheduled.</span><span class="sxs-lookup"><span data-stu-id="23bcb-143">task - Configures the chef-client to run automatically in the background as a secheduled task.</span></span>

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

### <span data-ttu-id="23bcb-144">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="23bcb-144">-InformationAction</span></span>
<span data-ttu-id="23bcb-145">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="23bcb-145">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="23bcb-146">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="23bcb-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="23bcb-147">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="23bcb-147">Continue</span></span>
- <span data-ttu-id="23bcb-148">Ignorować</span><span class="sxs-lookup"><span data-stu-id="23bcb-148">Ignore</span></span>
- <span data-ttu-id="23bcb-149">Inquire</span><span class="sxs-lookup"><span data-stu-id="23bcb-149">Inquire</span></span>
- <span data-ttu-id="23bcb-150">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="23bcb-150">SilentlyContinue</span></span>
- <span data-ttu-id="23bcb-151">Przestaw</span><span class="sxs-lookup"><span data-stu-id="23bcb-151">Stop</span></span>
- <span data-ttu-id="23bcb-152">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="23bcb-152">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23bcb-153">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="23bcb-153">-InformationVariable</span></span>
<span data-ttu-id="23bcb-154">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="23bcb-154">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23bcb-155">-Jsonattribute</span><span class="sxs-lookup"><span data-stu-id="23bcb-155">-JsonAttribute</span></span>
<span data-ttu-id="23bcb-156">Ciąg JSON do dodania do pierwszego uruchomienia Kuchmistrz-Client.</span><span class="sxs-lookup"><span data-stu-id="23bcb-156">A JSON string to be added to the first run of chef-client.</span></span> <span data-ttu-id="23bcb-157">na przykład-Jsonattribute "{" foo ":" bar "}"</span><span class="sxs-lookup"><span data-stu-id="23bcb-157">e.g. -JsonAttribute '{"foo" : "bar"}'</span></span>

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

### <span data-ttu-id="23bcb-158">-Linux</span><span class="sxs-lookup"><span data-stu-id="23bcb-158">-Linux</span></span>
<span data-ttu-id="23bcb-159">Wskazuje, że to polecenie cmdlet tworzy maszynę wirtualną opartą na systemie Linux.</span><span class="sxs-lookup"><span data-stu-id="23bcb-159">Indicates that this cmdlet creates a Linux based virtual machine.</span></span>

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

### <span data-ttu-id="23bcb-160">-Nazwa_organizacji</span><span class="sxs-lookup"><span data-stu-id="23bcb-160">-OrganizationName</span></span>
<span data-ttu-id="23bcb-161">Określa nazwę organizacji rozszerzenia Kuchmistrz.</span><span class="sxs-lookup"><span data-stu-id="23bcb-161">Specifies the organization name of the Chef extension.</span></span>

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

### <span data-ttu-id="23bcb-162">-Profile</span><span class="sxs-lookup"><span data-stu-id="23bcb-162">-Profile</span></span>
<span data-ttu-id="23bcb-163">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23bcb-163">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="23bcb-164">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="23bcb-164">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23bcb-165">-RunList</span><span class="sxs-lookup"><span data-stu-id="23bcb-165">-RunList</span></span>
<span data-ttu-id="23bcb-166">Określa listę uruchamiania węzła Kuchmistrz.</span><span class="sxs-lookup"><span data-stu-id="23bcb-166">Specifies the Chef node run list.</span></span>

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

### <span data-ttu-id="23bcb-167">-Secret</span><span class="sxs-lookup"><span data-stu-id="23bcb-167">-Secret</span></span>
<span data-ttu-id="23bcb-168">Klucz szyfrowania użyty do szyfrowania i odszyfrowywania wartości elementu worka danych.</span><span class="sxs-lookup"><span data-stu-id="23bcb-168">The encryption key used to encrypt and decrypt the data bag item values.</span></span>

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

### <span data-ttu-id="23bcb-169">-SecretFile</span><span class="sxs-lookup"><span data-stu-id="23bcb-169">-SecretFile</span></span>
<span data-ttu-id="23bcb-170">Ścieżka do pliku zawierającego klucz szyfrowania użyty do szyfrowania i odszyfrowywania wartości elementu worka danych.</span><span class="sxs-lookup"><span data-stu-id="23bcb-170">The path to the file that contains the encryption key used to encrypt and decrypt the data bag item values.</span></span>

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

### <span data-ttu-id="23bcb-171">-ValidationClientName</span><span class="sxs-lookup"><span data-stu-id="23bcb-171">-ValidationClientName</span></span>
<span data-ttu-id="23bcb-172">Określa nazwę klienta weryfikacji.</span><span class="sxs-lookup"><span data-stu-id="23bcb-172">Specifies the name of the validation client.</span></span>

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

### <span data-ttu-id="23bcb-173">-ValidationPem</span><span class="sxs-lookup"><span data-stu-id="23bcb-173">-ValidationPem</span></span>
<span data-ttu-id="23bcb-174">Określa ścieżkę pliku modułu sprawdzania poprawności Kuchmistrz.</span><span class="sxs-lookup"><span data-stu-id="23bcb-174">Specifies the Chef validator .pem file path.</span></span>

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

### <span data-ttu-id="23bcb-175">-Version</span><span class="sxs-lookup"><span data-stu-id="23bcb-175">-Version</span></span>
<span data-ttu-id="23bcb-176">Określa numer wersji rozszerzenia Kuchmistrz.</span><span class="sxs-lookup"><span data-stu-id="23bcb-176">Specifies the version number of the Chef extension.</span></span>

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

### <span data-ttu-id="23bcb-177">-VM</span><span class="sxs-lookup"><span data-stu-id="23bcb-177">-VM</span></span>
<span data-ttu-id="23bcb-178">Określa trwały obiekt maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="23bcb-178">Specifies the persistent virtual machine object.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23bcb-179">-Windows</span><span class="sxs-lookup"><span data-stu-id="23bcb-179">-Windows</span></span>
<span data-ttu-id="23bcb-180">Wskazuje, że w tym poleceniu cmdlet jest tworzona maszyna wirtualna systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="23bcb-180">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

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

### <span data-ttu-id="23bcb-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23bcb-181">CommonParameters</span></span>
<span data-ttu-id="23bcb-182">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23bcb-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23bcb-183">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23bcb-183">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23bcb-184">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="23bcb-184">INPUTS</span></span>

## <span data-ttu-id="23bcb-185">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="23bcb-185">OUTPUTS</span></span>

## <span data-ttu-id="23bcb-186">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="23bcb-186">NOTES</span></span>

## <span data-ttu-id="23bcb-187">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="23bcb-187">RELATED LINKS</span></span>

[<span data-ttu-id="23bcb-188">Get-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="23bcb-188">Get-AzureVMChefExtension</span></span>](./Get-AzureVMChefExtension.md)

[<span data-ttu-id="23bcb-189">Remove-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="23bcb-189">Remove-AzureVMChefExtension</span></span>](./Remove-AzureVMChefExtension.md)


