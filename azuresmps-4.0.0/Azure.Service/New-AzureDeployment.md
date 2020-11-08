---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2BDB255A-EFB3-4580-BE95-187008DB208C
online version: ''
schema: 2.0.0
ms.openlocfilehash: c21195f6d3ed938844717789f8a0df16f49fbd85
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054895"
---
# <span data-ttu-id="62264-101">New-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="62264-101">New-AzureDeployment</span></span>

## <span data-ttu-id="62264-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="62264-102">SYNOPSIS</span></span>
<span data-ttu-id="62264-103">Tworzy wdrożenie z usługi.</span><span class="sxs-lookup"><span data-stu-id="62264-103">Creates a deployment from a service.</span></span>

## <span data-ttu-id="62264-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="62264-104">SYNTAX</span></span>

```
New-AzureDeployment [-ServiceName] <String> [-Package] <String> [-Configuration] <String> [-Slot] <String>
 [[-Label] <String>] [[-Name] <String>] [-DoNotStart] [-TreatWarningsAsError]
 [-ExtensionConfiguration <ExtensionConfigurationInput[]>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="62264-105">Opis</span><span class="sxs-lookup"><span data-stu-id="62264-105">DESCRIPTION</span></span>
<span data-ttu-id="62264-106">Polecenie cmdlet **New-AzureDeployment** tworzy wdrożenie platformy Azure z usługi obejmującej role w sieci Web i role pracowników.</span><span class="sxs-lookup"><span data-stu-id="62264-106">The **New-AzureDeployment** cmdlet creates an Azure deployment from a service that comprises web roles and worker roles.</span></span>
<span data-ttu-id="62264-107">To polecenie cmdlet tworzy wdrożenie na podstawie pliku pakietu (. cspkg) oraz pliku konfiguracji usługi (cscfg).</span><span class="sxs-lookup"><span data-stu-id="62264-107">This cmdlet creates a deployment based on a package file (.cspkg) and a service configuration file (.cscfg).</span></span>
<span data-ttu-id="62264-108">Określ nazwę, która jest unikatowa w środowisku wdrażania.</span><span class="sxs-lookup"><span data-stu-id="62264-108">Specify a name that is unique within deployment environment.</span></span>

<span data-ttu-id="62264-109">Użyj polecenia cmdlet **New-AzureVM** w celu utworzenia wdrożenia opartego na maszynach wirtualnych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="62264-109">Use the **New-AzureVM** cmdlet to create a deployment based on Azure virtual machines.</span></span>

## <span data-ttu-id="62264-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="62264-110">EXAMPLES</span></span>

### <span data-ttu-id="62264-111">Przykład 1: Tworzenie wdrożenia</span><span class="sxs-lookup"><span data-stu-id="62264-111">Example 1: Create a deployment</span></span>
```
PS C:\> New-AzureDeployment -ServiceName "ContosoService" -Slot "Production" -Package "https://contosostorage.blob.core.windows.net/container06/ContosoPackage.cspkg" -Configuration "C:\packages\ContosoConfiguration.cscfg" -Label "ContosoDeployment"
```

<span data-ttu-id="62264-112">To polecenie tworzy wdrożenie produkcyjne na podstawie pakietu o nazwie ContosoPackage. cspkg i konfiguracji o nazwie ContosoConfiguration. cscfg.</span><span class="sxs-lookup"><span data-stu-id="62264-112">This command creates a production deployment based on a package named ContosoPackage.cspkg and a configuration named ContosoConfiguration.cscfg.</span></span>
<span data-ttu-id="62264-113">Polecenie Określa etykietę wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="62264-113">The command specifies a label for the deployment.</span></span>
<span data-ttu-id="62264-114">Nazwa nie jest określana.</span><span class="sxs-lookup"><span data-stu-id="62264-114">It does not specify a name.</span></span>
<span data-ttu-id="62264-115">To polecenie cmdlet tworzy identyfikator GUID jako nazwę.</span><span class="sxs-lookup"><span data-stu-id="62264-115">This cmdlet creates a GUID as the name.</span></span>

### <span data-ttu-id="62264-116">Przykład 2: Tworzenie wdrożenia na podstawie konfiguracji rozszerzenia</span><span class="sxs-lookup"><span data-stu-id="62264-116">Example 2: Create a deployment based on an extension configuration</span></span>
```
PS C:\> New-AzureDeployment -ServiceName "ContosoService" -Slot "Production" -Package "https://contosostorage.blob.core.windows.net/container06/ContosoPackage.cspkg" -Configuration "C:\packages\ContosoConfiguration.cscfg" -ExtensionConfiguration "C:\packages\ContosoExtensionConfig.cscfg"
```

<span data-ttu-id="62264-117">To polecenie tworzy wdrożenie produkcyjne na podstawie pakietu i konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="62264-117">This command creates a production deployment based on a package and configuration.</span></span>
<span data-ttu-id="62264-118">To polecenie określa konfigurację rozszerzenia o nazwie ContosoExtensionConfig. cscfg.</span><span class="sxs-lookup"><span data-stu-id="62264-118">The command specifies an extension configuration named ContosoExtensionConfig.cscfg.</span></span>
<span data-ttu-id="62264-119">To polecenie cmdlet tworzy identyfikatory GUID jako imię i nazwisko oraz etykietę.</span><span class="sxs-lookup"><span data-stu-id="62264-119">This cmdlet creates GUIDs as the name and the label.</span></span>

## <span data-ttu-id="62264-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="62264-120">PARAMETERS</span></span>

### <span data-ttu-id="62264-121">— Konfiguracja</span><span class="sxs-lookup"><span data-stu-id="62264-121">-Configuration</span></span>
<span data-ttu-id="62264-122">Określa pełną ścieżkę do pliku konfiguracji usługi.</span><span class="sxs-lookup"><span data-stu-id="62264-122">Specifies the full path of a service configuration file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62264-123">-DoNotStart</span><span class="sxs-lookup"><span data-stu-id="62264-123">-DoNotStart</span></span>
<span data-ttu-id="62264-124">Określa, że to polecenie cmdlet nie rozpocznie wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="62264-124">Specifies that this cmdlet does not start the deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62264-125">-ExtensionConfiguration</span><span class="sxs-lookup"><span data-stu-id="62264-125">-ExtensionConfiguration</span></span>
<span data-ttu-id="62264-126">Określa tablicę obiektów konfiguracji rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="62264-126">Specifies an array of extension configuration objects.</span></span>

```yaml
Type: ExtensionConfigurationInput[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62264-127">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="62264-127">-InformationAction</span></span>
<span data-ttu-id="62264-128">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="62264-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="62264-129">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="62264-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="62264-130">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="62264-130">Continue</span></span>
- <span data-ttu-id="62264-131">Ignorować</span><span class="sxs-lookup"><span data-stu-id="62264-131">Ignore</span></span>
- <span data-ttu-id="62264-132">Inquire</span><span class="sxs-lookup"><span data-stu-id="62264-132">Inquire</span></span>
- <span data-ttu-id="62264-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="62264-133">SilentlyContinue</span></span>
- <span data-ttu-id="62264-134">Przestaw</span><span class="sxs-lookup"><span data-stu-id="62264-134">Stop</span></span>
- <span data-ttu-id="62264-135">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="62264-135">Suspend</span></span>

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

### <span data-ttu-id="62264-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="62264-136">-InformationVariable</span></span>
<span data-ttu-id="62264-137">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="62264-137">Specifies an information variable.</span></span>

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

### <span data-ttu-id="62264-138">-Label</span><span class="sxs-lookup"><span data-stu-id="62264-138">-Label</span></span>
<span data-ttu-id="62264-139">Określa nazwę etykiety dla wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="62264-139">Specifies a label name for the deployment.</span></span>
<span data-ttu-id="62264-140">Jeśli nie określisz etykiety, to polecenie cmdlet użyje identyfikatora GUID.</span><span class="sxs-lookup"><span data-stu-id="62264-140">If you do not specify a label, this cmdlet uses a GUID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62264-141">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="62264-141">-Name</span></span>
<span data-ttu-id="62264-142">Określa nazwę wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="62264-142">Specifies a deployment name.</span></span>
<span data-ttu-id="62264-143">Jeśli nie określisz nazwy, to polecenie cmdlet użyje identyfikatora GUID.</span><span class="sxs-lookup"><span data-stu-id="62264-143">If you do not specify a name, this cmdlet uses a GUID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DeploymentName

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62264-144">-Package</span><span class="sxs-lookup"><span data-stu-id="62264-144">-Package</span></span>
<span data-ttu-id="62264-145">Określa ścieżkę lub identyfikator URI pliku cspkg w magazynie w ramach tego samego abonamentu lub projektu.</span><span class="sxs-lookup"><span data-stu-id="62264-145">Specifies the path or URI of a .cspkg file in storage within the same subscription or project.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62264-146">-Profile</span><span class="sxs-lookup"><span data-stu-id="62264-146">-Profile</span></span>
<span data-ttu-id="62264-147">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62264-147">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="62264-148">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="62264-148">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="62264-149">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="62264-149">-ServiceName</span></span>
<span data-ttu-id="62264-150">Określa nazwę usługi Azure dla wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="62264-150">Specifies the name of the Azure service for the deployment.</span></span>

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

### <span data-ttu-id="62264-151">-Slot</span><span class="sxs-lookup"><span data-stu-id="62264-151">-Slot</span></span>
<span data-ttu-id="62264-152">Określa środowisko, w którym to polecenie cmdlet tworzy wdrożenie.</span><span class="sxs-lookup"><span data-stu-id="62264-152">Specifies the environment where this cmdlet creates the deployment.</span></span>
<span data-ttu-id="62264-153">Prawidłowe wartości to: przemieszczanie i produkcja.</span><span class="sxs-lookup"><span data-stu-id="62264-153">Valid values are: Staging and Production.</span></span>
<span data-ttu-id="62264-154">Wartością domyślną jest produkcja.</span><span class="sxs-lookup"><span data-stu-id="62264-154">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62264-155">-TreatWarningsAsError</span><span class="sxs-lookup"><span data-stu-id="62264-155">-TreatWarningsAsError</span></span>
<span data-ttu-id="62264-156">Określa, że komunikaty ostrzegawcze są błędami.</span><span class="sxs-lookup"><span data-stu-id="62264-156">Specifies that warning messages are errors.</span></span>
<span data-ttu-id="62264-157">W przypadku określenia tego parametru komunikat ostrzegawczy powoduje niepowodzenie wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="62264-157">If you specify this parameter, a warning message causes the deployment to fail.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62264-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62264-158">CommonParameters</span></span>
<span data-ttu-id="62264-159">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62264-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62264-160">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62264-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62264-161">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="62264-161">INPUTS</span></span>

## <span data-ttu-id="62264-162">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="62264-162">OUTPUTS</span></span>

## <span data-ttu-id="62264-163">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="62264-163">NOTES</span></span>

## <span data-ttu-id="62264-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="62264-164">RELATED LINKS</span></span>

[<span data-ttu-id="62264-165">Get-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="62264-165">Get-AzureDeployment</span></span>](./Get-AzureDeployment.md)

[<span data-ttu-id="62264-166">Get-AzureDeploymentEvent</span><span class="sxs-lookup"><span data-stu-id="62264-166">Get-AzureDeploymentEvent</span></span>](./Get-AzureDeploymentEvent.md)

[<span data-ttu-id="62264-167">Przenieś — AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="62264-167">Move-AzureDeployment</span></span>](./Move-AzureDeployment.md)

[<span data-ttu-id="62264-168">Nowe — AzureVM</span><span class="sxs-lookup"><span data-stu-id="62264-168">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="62264-169">Remove-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="62264-169">Remove-AzureDeployment</span></span>](./Remove-AzureDeployment.md)

[<span data-ttu-id="62264-170">Set-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="62264-170">Set-AzureDeployment</span></span>](./Set-AzureDeployment.md)


