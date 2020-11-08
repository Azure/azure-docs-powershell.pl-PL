---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 956B60BE-D978-4682-BA11-4EE9296B77B4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2d21d1b9609c160bdb2b4b3b8477a4b1b9bea991
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054848"
---
# <span data-ttu-id="e5e5c-101">Publish-AzureVMDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="e5e5c-101">Publish-AzureVMDscConfiguration</span></span>

## <span data-ttu-id="e5e5c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e5e5c-102">SYNOPSIS</span></span>
<span data-ttu-id="e5e5c-103">Umożliwia opublikowanie odpowiedniego skryptu konfiguracji stanu w usłudze Azure Blob Storage.</span><span class="sxs-lookup"><span data-stu-id="e5e5c-103">Publishes a desired state configuration script to Azure blob storage.</span></span>

## <span data-ttu-id="e5e5c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e5e5c-104">SYNTAX</span></span>

### <span data-ttu-id="e5e5c-105">UploadArchive (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e5e5c-105">UploadArchive (Default)</span></span>
```
Publish-AzureVMDscConfiguration [-ConfigurationPath] <String> [-ContainerName <String>] [-Force]
 [-StorageContext <AzureStorageContext>] [-StorageEndpointSuffix <String>] [-SkipDependencyDetection]
 [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>] [-PassThru] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e5e5c-106">Funkcja Zarchiwizuj</span><span class="sxs-lookup"><span data-stu-id="e5e5c-106">CreateArchive</span></span>
```
Publish-AzureVMDscConfiguration [-ConfigurationPath] <String> [-Force] [-ConfigurationArchivePath <String>]
 [-SkipDependencyDetection] [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>] [-PassThru]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5e5c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e5e5c-107">DESCRIPTION</span></span>
<span data-ttu-id="e5e5c-108">Polecenie cmdlet **Publish-AzureVMDscConfiguration** umożliwia opublikowanie żądanego skryptu konfiguracji stanu w magazynie obiektów blob platformy Azure, który później można zastosować do maszyn wirtualnych platformy Azure przy użyciu polecenia cmdlet **Set-AzureVMDscExtension** .</span><span class="sxs-lookup"><span data-stu-id="e5e5c-108">The **Publish-AzureVMDscConfiguration** cmdlet publishes a desired state configuration script to Azure blob storage, which later can be applied to Azure virtual machines using the **Set-AzureVMDscExtension** cmdlet.</span></span>

## <span data-ttu-id="e5e5c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e5e5c-109">EXAMPLES</span></span>

### <span data-ttu-id="e5e5c-110">Przykład 1. publikowanie skryptu konfiguracji stanu do magazynu obiektów BLOB</span><span class="sxs-lookup"><span data-stu-id="e5e5c-110">Example 1: Publish a state configuration script to blob storage</span></span>
```
PS C:\> Publish-AzureVMDscConfiguration .\MyConfiguration.ps1
```

<span data-ttu-id="e5e5c-111">To polecenie tworzy pakiet ZIP dla danego skryptu i wszystkich modułów zasobów zależnych, a następnie przekazuje go do magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e5e5c-111">This command creates a .zip package for the given script and any dependent resource modules and uploads it to Azure storage.</span></span>

### <span data-ttu-id="e5e5c-112">Przykład 2: publikowanie skryptu konfiguracji stanu do pliku lokalnego</span><span class="sxs-lookup"><span data-stu-id="e5e5c-112">Example 2: Publish a state configuration script to a local file</span></span>
```
PS C:\> Publish-AzureVMDscConfiguration .\MyConfiguration.ps1 -ConfigurationArchivePath .\MyConfiguration.ps1.zip
```

<span data-ttu-id="e5e5c-113">To polecenie tworzy pakiet ZIP dla danego skryptu i wszystkich modułów zasobów zależnych i zapisuje go w lokalnym pliku .\MyConfiguration.ps1.zip.</span><span class="sxs-lookup"><span data-stu-id="e5e5c-113">This command creates a .zip package for the given script and any dependent resource modules and stores it in the local file .\MyConfiguration.ps1.zip.</span></span>

## <span data-ttu-id="e5e5c-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e5e5c-114">PARAMETERS</span></span>

### <span data-ttu-id="e5e5c-115">-AdditionalPath</span><span class="sxs-lookup"><span data-stu-id="e5e5c-115">-AdditionalPath</span></span>
<span data-ttu-id="e5e5c-116">Określa tablicę dodatkowych ścieżek.</span><span class="sxs-lookup"><span data-stu-id="e5e5c-116">Specifies an array of additional paths.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5e5c-117">-ConfigurationArchivePath</span><span class="sxs-lookup"><span data-stu-id="e5e5c-117">-ConfigurationArchivePath</span></span>
<span data-ttu-id="e5e5c-118">Określa ścieżkę pliku lokalnego. zip, w którym to polecenie cmdlet zapisuje archiwum konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="e5e5c-118">Specifies the path of a local .zip file that this cmdlet writes the configuration archive.</span></span>
<span data-ttu-id="e5e5c-119">Po zastosowaniu tego parametru skrypt konfiguracji nie zostanie przekazany do magazynu obiektów blob platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e5e5c-119">The configuration script is not uploaded to Azure blob storage if you use this parameter.</span></span>

```yaml
Type: String
Parameter Sets: CreateArchive
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5e5c-120">-ConfigurationDataPath</span><span class="sxs-lookup"><span data-stu-id="e5e5c-120">-ConfigurationDataPath</span></span>
<span data-ttu-id="e5e5c-121">Określa ścieżkę danych konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="e5e5c-121">Specifies a configuration data path.</span></span>

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

### <span data-ttu-id="e5e5c-122">-ConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="e5e5c-122">-ConfigurationPath</span></span>
<span data-ttu-id="e5e5c-123">Określa ścieżkę pliku zawierającego co najmniej jeden wariant.</span><span class="sxs-lookup"><span data-stu-id="e5e5c-123">Specifies the path of a file that contains one or more configurations.</span></span>
<span data-ttu-id="e5e5c-124">Plik może być skryptem programu Windows PowerShell (plikiem ps1), modułem (plik PSM1) lub archiwum (plikiem zip) zawierającym zestaw modułów programu Windows PowerShell, z każdym modułem w osobnym katalogu.</span><span class="sxs-lookup"><span data-stu-id="e5e5c-124">The file can be a Windows PowerShell script (.ps1 file), module (.psm1 file), or an archive (.zip file) that contains a set of Windows PowerShell modules, with each module in a separate directory.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5e5c-125">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="e5e5c-125">-ContainerName</span></span>
<span data-ttu-id="e5e5c-126">Określa nazwę kontenera magazynu platformy Azure, do którego jest przekazywana konfiguracja.</span><span class="sxs-lookup"><span data-stu-id="e5e5c-126">Specifies the name of the Azure storage container the configuration is uploaded to.</span></span>

```yaml
Type: String
Parameter Sets: UploadArchive
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5e5c-127">-Force</span><span class="sxs-lookup"><span data-stu-id="e5e5c-127">-Force</span></span>
<span data-ttu-id="e5e5c-128">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e5e5c-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e5e5c-129">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="e5e5c-129">-InformationAction</span></span>
<span data-ttu-id="e5e5c-130">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="e5e5c-130">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="e5e5c-131">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="e5e5c-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e5e5c-132">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="e5e5c-132">Continue</span></span>
- <span data-ttu-id="e5e5c-133">Ignorować</span><span class="sxs-lookup"><span data-stu-id="e5e5c-133">Ignore</span></span>
- <span data-ttu-id="e5e5c-134">Inquire</span><span class="sxs-lookup"><span data-stu-id="e5e5c-134">Inquire</span></span>
- <span data-ttu-id="e5e5c-135">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="e5e5c-135">SilentlyContinue</span></span>
- <span data-ttu-id="e5e5c-136">Przestaw</span><span class="sxs-lookup"><span data-stu-id="e5e5c-136">Stop</span></span>
- <span data-ttu-id="e5e5c-137">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="e5e5c-137">Suspend</span></span>

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

### <span data-ttu-id="e5e5c-138">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="e5e5c-138">-InformationVariable</span></span>
<span data-ttu-id="e5e5c-139">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="e5e5c-139">Specifies an information variable.</span></span>

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

### <span data-ttu-id="e5e5c-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e5e5c-140">-PassThru</span></span>
<span data-ttu-id="e5e5c-141">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="e5e5c-141">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e5e5c-142">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="e5e5c-142">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e5e5c-143">-Profile</span><span class="sxs-lookup"><span data-stu-id="e5e5c-143">-Profile</span></span>
<span data-ttu-id="e5e5c-144">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5e5c-144">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e5e5c-145">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="e5e5c-145">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e5e5c-146">-SkipDependencyDetection</span><span class="sxs-lookup"><span data-stu-id="e5e5c-146">-SkipDependencyDetection</span></span>
<span data-ttu-id="e5e5c-147">Wskazuje, że to polecenie cmdlet powoduje pominięcie wykrywania zależności.</span><span class="sxs-lookup"><span data-stu-id="e5e5c-147">Indicates that this cmdlet skips dependency detection.</span></span>

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

### <span data-ttu-id="e5e5c-148">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="e5e5c-148">-StorageContext</span></span>
<span data-ttu-id="e5e5c-149">Określa kontekst usługi Azure Storage, który udostępnia ustawienia zabezpieczeń używane do przekazywania skryptu konfiguracji do kontenera określonego przez parametr *ContainerName* .</span><span class="sxs-lookup"><span data-stu-id="e5e5c-149">Specifies the Azure storage context that provides the security settings used to upload the configuration script to the container specified by the *ContainerName* parameter.</span></span>
<span data-ttu-id="e5e5c-150">Ten kontekst zapewnia dostęp do zapisu w kontenerze.</span><span class="sxs-lookup"><span data-stu-id="e5e5c-150">This context provides write access to the container.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: UploadArchive
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5e5c-151">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="e5e5c-151">-StorageEndpointSuffix</span></span>
<span data-ttu-id="e5e5c-152">Określa sufiks punktu końcowego magazynu, na przykład core.contoso.net</span><span class="sxs-lookup"><span data-stu-id="e5e5c-152">Specifies the suffix for the storage end-point, for instance, core.contoso.net</span></span>

```yaml
Type: String
Parameter Sets: UploadArchive
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5e5c-153">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e5e5c-153">-Confirm</span></span>
<span data-ttu-id="e5e5c-154">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5e5c-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5e5c-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5e5c-155">-WhatIf</span></span>
<span data-ttu-id="e5e5c-156">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5e5c-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5e5c-157">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e5e5c-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5e5c-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5e5c-158">CommonParameters</span></span>
<span data-ttu-id="e5e5c-159">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5e5c-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5e5c-160">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5e5c-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5e5c-161">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e5e5c-161">INPUTS</span></span>

## <span data-ttu-id="e5e5c-162">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e5e5c-162">OUTPUTS</span></span>

## <span data-ttu-id="e5e5c-163">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e5e5c-163">NOTES</span></span>

## <span data-ttu-id="e5e5c-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e5e5c-164">RELATED LINKS</span></span>

[<span data-ttu-id="e5e5c-165">Set-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="e5e5c-165">Set-AzureVMDscExtension</span></span>](./Set-AzureVMDscExtension.md)


