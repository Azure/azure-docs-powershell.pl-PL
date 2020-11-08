---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7F51F534-6C64-4983-A08F-4732A39C2E7C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 52c62f3d29b4cd2c87fd5606ca013eb03958fb62
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055030"
---
# <span data-ttu-id="d449d-101">Set-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="d449d-101">Set-AzureDeployment</span></span>

## <span data-ttu-id="d449d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d449d-102">SYNOPSIS</span></span>
<span data-ttu-id="d449d-103">Modyfikuje stan, ustawienia konfiguracji lub tryb uaktualniania wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="d449d-103">Modifies the status, configuration settings, or upgrade mode of a deployment.</span></span>

## <span data-ttu-id="d449d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d449d-104">SYNTAX</span></span>

### <span data-ttu-id="d449d-105">Aktualizowanie</span><span class="sxs-lookup"><span data-stu-id="d449d-105">Upgrade</span></span>
```
Set-AzureDeployment [-Upgrade] [-ServiceName] <String> [-Package] <String> [-Configuration] <String>
 [-Slot] <String> [[-Mode] <String>] [[-Label] <String>] [[-RoleName] <String>] [-Force]
 [[-ExtensionConfiguration] <ExtensionConfigurationInput[]>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="d449d-106">Konfiguracji</span><span class="sxs-lookup"><span data-stu-id="d449d-106">Config</span></span>
```
Set-AzureDeployment [-Config] [-ServiceName] <String> [-Configuration] <String> [-Slot] <String>
 [[-ExtensionConfiguration] <ExtensionConfigurationInput[]>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="d449d-107">Stan</span><span class="sxs-lookup"><span data-stu-id="d449d-107">Status</span></span>
```
Set-AzureDeployment [-Status] [-ServiceName] <String> [-Slot] <String> [-NewStatus] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="d449d-108">Opis</span><span class="sxs-lookup"><span data-stu-id="d449d-108">DESCRIPTION</span></span>
<span data-ttu-id="d449d-109">Polecenie cmdlet **Set-AzureDeployment** modyfikuje stan, ustawienia konfiguracji lub tryb uaktualniania wdrożenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d449d-109">The **Set-AzureDeployment** cmdlet modifies the status, configuration settings, or upgrade mode of an Azure deployment.</span></span>
<span data-ttu-id="d449d-110">Stan wdrożenia możesz zmienić na uruchomiony lub zawieszony.</span><span class="sxs-lookup"><span data-stu-id="d449d-110">You can change the status of the deployment to either Running or Suspended.</span></span>
<span data-ttu-id="d449d-111">Możesz zmienić plik cscfg dla wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="d449d-111">You can change the .cscfg file for the deployment.</span></span>
<span data-ttu-id="d449d-112">Możesz ustawić tryb uaktualniania i pliki konfiguracji aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="d449d-112">You can set the upgrade mode and update configuration files.</span></span>
<span data-ttu-id="d449d-113">Użyj polecenia cmdlet **Set-AzureWalkUpgradeDomain** w celu zainicjowania uaktualnienia.</span><span class="sxs-lookup"><span data-stu-id="d449d-113">Use the **Set-AzureWalkUpgradeDomain** cmdlet to initiate an upgrade.</span></span>

## <span data-ttu-id="d449d-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d449d-114">EXAMPLES</span></span>

### <span data-ttu-id="d449d-115">Przykład 1. Zmienianie stanu wdrożenia</span><span class="sxs-lookup"><span data-stu-id="d449d-115">Example 1: Change the status of a deployment</span></span>
```
PS C:\> Set-AzureDeployment -Status -ServiceName "ContosoService" -Slot "Production" -NewStatus "Running"
```

<span data-ttu-id="d449d-116">To polecenie ustawia stan wdrożenia usługi o nazwie ContosoService w środowisku produkcyjnym w celu uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="d449d-116">This command sets the status of the deployment for the service named ContosoService in the production environment to Running.</span></span>

### <span data-ttu-id="d449d-117">Przykład 2: Przypisywanie innego pliku konfiguracji do wdrożenia</span><span class="sxs-lookup"><span data-stu-id="d449d-117">Example 2: Assign a different configuration file to a deployment</span></span>
```
PS C:\> Set-AzureDeployment -Config -ServiceName "ContosoService" -Slot "Staging" -Configuration "C:\Temp\MyServiceConfig.Cloud.csfg"
```

<span data-ttu-id="d449d-118">To polecenie przypisuje inny plik konfiguracji dla wdrożenia usługi o nazwie ContosoService w środowisku przemieszczania.</span><span class="sxs-lookup"><span data-stu-id="d449d-118">This command assigns a different configuration file for the deployment for the service named ContosoService in the staging environment.</span></span>

### <span data-ttu-id="d449d-119">Przykład 3: Ustawianie trybu uaktualnienia Auto</span><span class="sxs-lookup"><span data-stu-id="d449d-119">Example 3: Set the upgrade mode to Auto</span></span>
```
PS C:\> Set-AzureDeployment -Upgrade -ServiceName "ContosoService" -Mode Auto -Package "C:\packages\ContosoApp.cspkg" -Configuration "C:\Config\ContosoServiceConfig.Cloud.csfg"
```

<span data-ttu-id="d449d-120">To polecenie ustawia tryb uaktualniania na Auto i określa pakiet uaktualniający oraz nowy plik konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="d449d-120">This command sets the upgrade mode to Auto, and specifies an upgrade package and a new configuration file.</span></span>

### <span data-ttu-id="d449d-121">Przykład 4: Instalowanie konfiguracji rozszerzenia w usłudze</span><span class="sxs-lookup"><span data-stu-id="d449d-121">Example 4: Install extension configuration in a service</span></span>
```
PS C:\> Set-AzureDeployment -Config -ServiceName "ContosoService" -Mode "Automatic" -Package "https://contosostorage.blob.core.windows.net/container06/ContosoPackage.cspkg" -Configuration "C:\packages\ContosoConfiguration.cscfg" -Slot "Production" -ExtensionConfiguration "C:\packages\ContosoExtensionConfig.cscfg"
```

<span data-ttu-id="d449d-122">To polecenie powoduje zainstalowanie konfiguracji rozszerzenia w określonej usłudze chmury i zastosowanie jej do ról.</span><span class="sxs-lookup"><span data-stu-id="d449d-122">This command installs the extension configuration in the specified Cloud Service and applies them on roles.</span></span>

## <span data-ttu-id="d449d-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d449d-123">PARAMETERS</span></span>

### <span data-ttu-id="d449d-124">-Config</span><span class="sxs-lookup"><span data-stu-id="d449d-124">-Config</span></span>
<span data-ttu-id="d449d-125">Określa, że to polecenie cmdlet modyfikuje konfigurację wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="d449d-125">Specifies that this cmdlet modifies the configuration of the deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Config
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d449d-126">— Konfiguracja</span><span class="sxs-lookup"><span data-stu-id="d449d-126">-Configuration</span></span>
<span data-ttu-id="d449d-127">Określa pełną ścieżkę do pliku konfiguracji cscfg.</span><span class="sxs-lookup"><span data-stu-id="d449d-127">Specifies the full path of a .cscfg configuration file.</span></span>
<span data-ttu-id="d449d-128">Możesz określić plik konfiguracji w celu przeprowadzenia uaktualnienia lub zmiany konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="d449d-128">You can specify a configuration file for an upgrade or configuration change.</span></span>

```yaml
Type: String
Parameter Sets: Upgrade, Config
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d449d-129">-ExtensionConfiguration</span><span class="sxs-lookup"><span data-stu-id="d449d-129">-ExtensionConfiguration</span></span>
<span data-ttu-id="d449d-130">Określa tablicę obiektów konfiguracji rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="d449d-130">Specifies an array of extension configuration objects.</span></span>

```yaml
Type: ExtensionConfigurationInput[]
Parameter Sets: Upgrade, Config
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d449d-131">-Force</span><span class="sxs-lookup"><span data-stu-id="d449d-131">-Force</span></span>
<span data-ttu-id="d449d-132">Wskazuje, że polecenie cmdlet przeprowadza wymuszone uaktualnienie.</span><span class="sxs-lookup"><span data-stu-id="d449d-132">Indicates that cmdlet performs a forced upgrade.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Upgrade
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d449d-133">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="d449d-133">-InformationAction</span></span>
<span data-ttu-id="d449d-134">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="d449d-134">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="d449d-135">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="d449d-135">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d449d-136">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="d449d-136">Continue</span></span>
- <span data-ttu-id="d449d-137">Ignorować</span><span class="sxs-lookup"><span data-stu-id="d449d-137">Ignore</span></span>
- <span data-ttu-id="d449d-138">Inquire</span><span class="sxs-lookup"><span data-stu-id="d449d-138">Inquire</span></span>
- <span data-ttu-id="d449d-139">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="d449d-139">SilentlyContinue</span></span>
- <span data-ttu-id="d449d-140">Przestaw</span><span class="sxs-lookup"><span data-stu-id="d449d-140">Stop</span></span>
- <span data-ttu-id="d449d-141">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="d449d-141">Suspend</span></span>

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

### <span data-ttu-id="d449d-142">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="d449d-142">-InformationVariable</span></span>
<span data-ttu-id="d449d-143">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="d449d-143">Specifies an information variable.</span></span>

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

### <span data-ttu-id="d449d-144">-Label</span><span class="sxs-lookup"><span data-stu-id="d449d-144">-Label</span></span>
<span data-ttu-id="d449d-145">Określa etykietę uaktualnionego wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="d449d-145">Specifies a label for the upgraded deployment.</span></span>

```yaml
Type: String
Parameter Sets: Upgrade
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d449d-146">-Mode (tryb)</span><span class="sxs-lookup"><span data-stu-id="d449d-146">-Mode</span></span>
<span data-ttu-id="d449d-147">Określa tryb uaktualniania.</span><span class="sxs-lookup"><span data-stu-id="d449d-147">Specifies the mode of upgrade.</span></span>
<span data-ttu-id="d449d-148">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="d449d-148">Valid values are:</span></span> 

- <span data-ttu-id="d449d-149">Automatycznie</span><span class="sxs-lookup"><span data-stu-id="d449d-149">Auto</span></span> 
- <span data-ttu-id="d449d-150">Ręcznie</span><span class="sxs-lookup"><span data-stu-id="d449d-150">Manual</span></span> 
- <span data-ttu-id="d449d-151">Jednoczesn</span><span class="sxs-lookup"><span data-stu-id="d449d-151">Simultaneous</span></span>

```yaml
Type: String
Parameter Sets: Upgrade
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d449d-152">-NewStatus</span><span class="sxs-lookup"><span data-stu-id="d449d-152">-NewStatus</span></span>
<span data-ttu-id="d449d-153">Określa stan docelowy wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="d449d-153">Specifies the target status for the deployment.</span></span>
<span data-ttu-id="d449d-154">Prawidłowe wartości to: uruchomione i zawieszone.</span><span class="sxs-lookup"><span data-stu-id="d449d-154">Valid values are: Running and Suspended.</span></span>

```yaml
Type: String
Parameter Sets: Status
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d449d-155">-Package</span><span class="sxs-lookup"><span data-stu-id="d449d-155">-Package</span></span>
<span data-ttu-id="d449d-156">Określa pełną ścieżkę do pliku pakietu uaktualniającego.</span><span class="sxs-lookup"><span data-stu-id="d449d-156">Specifies the full path of an upgrade package file.</span></span>

```yaml
Type: String
Parameter Sets: Upgrade
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d449d-157">-Profile</span><span class="sxs-lookup"><span data-stu-id="d449d-157">-Profile</span></span>
<span data-ttu-id="d449d-158">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d449d-158">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d449d-159">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="d449d-159">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d449d-160">-Rolename</span><span class="sxs-lookup"><span data-stu-id="d449d-160">-RoleName</span></span>
<span data-ttu-id="d449d-161">Określa nazwę roli do uaktualnienia.</span><span class="sxs-lookup"><span data-stu-id="d449d-161">Specifies the name of the role to upgrade.</span></span>

```yaml
Type: String
Parameter Sets: Upgrade
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d449d-162">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="d449d-162">-ServiceName</span></span>
<span data-ttu-id="d449d-163">Określa nazwę usługi platformy Azure wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="d449d-163">Specifies the name of the Azure service of the deployment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d449d-164">-Slot</span><span class="sxs-lookup"><span data-stu-id="d449d-164">-Slot</span></span>
<span data-ttu-id="d449d-165">Określa środowisko wdrożenia, które ma zostać zmodyfikowane.</span><span class="sxs-lookup"><span data-stu-id="d449d-165">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="d449d-166">Prawidłowe wartości: produkcja i przemieszczanie.</span><span class="sxs-lookup"><span data-stu-id="d449d-166">Valid values are: Production and Staging.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d449d-167">-Status</span><span class="sxs-lookup"><span data-stu-id="d449d-167">-Status</span></span>
<span data-ttu-id="d449d-168">Określa, że to polecenie cmdlet zmieni stan wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="d449d-168">Specifies that this cmdlet changes the status of the deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Status
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d449d-169">— Uaktualnienie</span><span class="sxs-lookup"><span data-stu-id="d449d-169">-Upgrade</span></span>
<span data-ttu-id="d449d-170">Określa, że to polecenie cmdlet uaktualni wdrożenie.</span><span class="sxs-lookup"><span data-stu-id="d449d-170">Specifies that this cmdlet upgrades the deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Upgrade
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d449d-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d449d-171">CommonParameters</span></span>
<span data-ttu-id="d449d-172">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d449d-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d449d-173">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d449d-173">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d449d-174">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d449d-174">INPUTS</span></span>

## <span data-ttu-id="d449d-175">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d449d-175">OUTPUTS</span></span>

## <span data-ttu-id="d449d-176">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d449d-176">NOTES</span></span>

## <span data-ttu-id="d449d-177">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d449d-177">RELATED LINKS</span></span>

[<span data-ttu-id="d449d-178">Get-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="d449d-178">Get-AzureDeployment</span></span>](./Get-AzureDeployment.md)

[<span data-ttu-id="d449d-179">Get-AzureDeploymentEvent</span><span class="sxs-lookup"><span data-stu-id="d449d-179">Get-AzureDeploymentEvent</span></span>](./Get-AzureDeploymentEvent.md)

[<span data-ttu-id="d449d-180">Przenieś — AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="d449d-180">Move-AzureDeployment</span></span>](./Move-AzureDeployment.md)

[<span data-ttu-id="d449d-181">Nowe — AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="d449d-181">New-AzureDeployment</span></span>](./New-AzureDeployment.md)

[<span data-ttu-id="d449d-182">Remove-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="d449d-182">Remove-AzureDeployment</span></span>](./Remove-AzureDeployment.md)

[<span data-ttu-id="d449d-183">Set-AzureWalkUpgradeDomain</span><span class="sxs-lookup"><span data-stu-id="d449d-183">Set-AzureWalkUpgradeDomain</span></span>](./Set-AzureWalkUpgradeDomain.md)


