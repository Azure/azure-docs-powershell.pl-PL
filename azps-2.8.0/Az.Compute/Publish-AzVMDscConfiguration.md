---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: FB9ACBA2-081E-4876-A21A-F5BA11CBEDA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/publish-azvmdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Publish-AzVMDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Publish-AzVMDscConfiguration.md
ms.openlocfilehash: 3db80e92a7bcd61fc62adaafda0bb3887f532202
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706303"
---
# <span data-ttu-id="85f12-101">Publish-AzVMDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="85f12-101">Publish-AzVMDscConfiguration</span></span>

## <span data-ttu-id="85f12-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="85f12-102">SYNOPSIS</span></span>
<span data-ttu-id="85f12-103">Przekazywanie skryptu DSC do magazynu obiektów blob platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="85f12-103">Uploads a DSC script to Azure blob storage.</span></span>

## <span data-ttu-id="85f12-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="85f12-104">SYNTAX</span></span>

### <span data-ttu-id="85f12-105">UploadArchive (domyślny)</span><span class="sxs-lookup"><span data-stu-id="85f12-105">UploadArchive (Default)</span></span>
```
Publish-AzVMDscConfiguration [-ResourceGroupName] <String> [-ConfigurationPath] <String>
 [[-ContainerName] <String>] [-StorageAccountName] <String> [-StorageEndpointSuffix <String>] [-Force]
 [-SkipDependencyDetection] [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85f12-106">Funkcja Zarchiwizuj</span><span class="sxs-lookup"><span data-stu-id="85f12-106">CreateArchive</span></span>
```
Publish-AzVMDscConfiguration [-ConfigurationPath] <String> [[-OutputArchivePath] <String>] [-Force]
 [-SkipDependencyDetection] [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85f12-107">Opis</span><span class="sxs-lookup"><span data-stu-id="85f12-107">DESCRIPTION</span></span>
<span data-ttu-id="85f12-108">Polecenie cmdlet **Publish-AzVMDscConfiguration** umożliwia przekazanie skryptu konfiguracji stanu (DSC) do magazynu obiektów blob platformy Azure, który później można zastosować do maszyn wirtualnych platformy Azure przy użyciu polecenia cmdlet Set-AzVMDscExtension.</span><span class="sxs-lookup"><span data-stu-id="85f12-108">The **Publish-AzVMDscConfiguration** cmdlet uploads a Desired State Configuration (DSC) script to Azure blob storage, which later can be applied to Azure virtual machines using the Set-AzVMDscExtension cmdlet.</span></span>

## <span data-ttu-id="85f12-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="85f12-109">EXAMPLES</span></span>

### <span data-ttu-id="85f12-110">Przykład 1: Tworzenie pakietu zip przekazywanie go do magazynu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="85f12-110">Example 1: Create a .zip package an upload it to Azure storage</span></span>
```
PS C:\> Publish-AzVMDscConfiguration ".\MyConfiguration.ps1"
```

<span data-ttu-id="85f12-111">To polecenie tworzy pakiet ZIP dla danego skryptu i wszystkich modułów zasobów zależnych, a następnie przekazuje go do magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="85f12-111">This command creates a .zip package for the given script and any dependent resource modules and uploads it to Azure storage.</span></span>

### <span data-ttu-id="85f12-112">Przykład 2: Tworzenie pakietu zip i przechowywanie go w pliku lokalnym</span><span class="sxs-lookup"><span data-stu-id="85f12-112">Example 2: Create a .zip package and store it to a local file</span></span>
```
PS C:\> Publish-AzVMDscConfiguration ".\MyConfiguration.ps1" -OutputArchivePath ".\MyConfiguration.ps1.zip"
```

<span data-ttu-id="85f12-113">To polecenie tworzy pakiet ZIP dla danego skryptu i wszystkich modułów zasobów zależnych i zapisuje go w pliku lokalnym o nazwie .\MyConfiguration.ps1.zip.</span><span class="sxs-lookup"><span data-stu-id="85f12-113">This command creates a .zip package for the given script and any dependent resource modules and stores it in the local file that is named .\MyConfiguration.ps1.zip.</span></span>

### <span data-ttu-id="85f12-114">Przykład 3: Dodawanie konfiguracji do archiwum, a następnie przekazywanie go do magazynu</span><span class="sxs-lookup"><span data-stu-id="85f12-114">Example 3: Add configuration to the archive and then upload it to storage</span></span>
```
PS C:\> Publish-AzVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -SkipDependencyDetection
```

<span data-ttu-id="85f12-115">To polecenie dodaje konfigurację o nazwie Sample.ps1 do archiwum konfiguracji w celu przekazania do magazynu platformy Azure i pominięcie modułów zasobów zależnych.</span><span class="sxs-lookup"><span data-stu-id="85f12-115">This command adds configuration named Sample.ps1 to the configuration archive to upload to Azure storage and skips dependent resource modules.</span></span>

### <span data-ttu-id="85f12-116">Przykład 4: Dodawanie danych konfiguracji i konfiguracji do archiwum, a następnie przekazywanie go do magazynu</span><span class="sxs-lookup"><span data-stu-id="85f12-116">Example 4: Add configuration and configuration data to the archive and then upload it to storage</span></span>
```
PS C:\> Publish-AzVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -ConfigurationDataPath "C:\SampleData.psd1"
```

<span data-ttu-id="85f12-117">To polecenie dodaje konfigurację o nazwie Sample.ps1 i dane konfiguracji o nazwie SampleData.psd1 do archiwum konfiguracji w celu przekazania do magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="85f12-117">This command adds configuration named Sample.ps1 and configuration data named SampleData.psd1 to the configuration archive to upload to Azure storage.</span></span>

### <span data-ttu-id="85f12-118">Przykład 5: Dodawanie konfiguracji, danych konfiguracyjnych i dodatkowej zawartości do archiwum, a następnie przekazywanie go do miejsca do magazynowania</span><span class="sxs-lookup"><span data-stu-id="85f12-118">Example 5: Add configuration, configuration data, and additional content to the archive and then upload it to storage</span></span>
```
PS C:\> Publish-AzVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -AdditionalPath @("C:\ContentDir1", "C:\File.txt") -ConfigurationDataPath "C:\SampleData.psd1"
```

<span data-ttu-id="85f12-119">To polecenie umożliwia dodanie konfiguracji o nazwie Sample.ps1, danych konfiguracji SampleData.psd1 oraz dodatkowej zawartości do archiwum konfiguracji w celu przekazania do magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="85f12-119">This command adds configuration named Sample.ps1, configuration data SampleData.psd1, and additional content to configuration archive to upload to Azure storage.</span></span>

## <span data-ttu-id="85f12-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="85f12-120">PARAMETERS</span></span>

### <span data-ttu-id="85f12-121">-AdditionalPath</span><span class="sxs-lookup"><span data-stu-id="85f12-121">-AdditionalPath</span></span>
<span data-ttu-id="85f12-122">Określa ścieżkę pliku lub katalogu, który ma zostać uwzględniony w archiwum konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="85f12-122">Specifies the path of a file or a directory to include in the configuration archive.</span></span>
<span data-ttu-id="85f12-123">Pobieranie zostanie pobrane na maszynie wirtualnej wraz z konfiguracją.</span><span class="sxs-lookup"><span data-stu-id="85f12-123">It gets downloaded to the virtual machine together with the configuration.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85f12-124">-ConfigurationDataPath</span><span class="sxs-lookup"><span data-stu-id="85f12-124">-ConfigurationDataPath</span></span>
<span data-ttu-id="85f12-125">Określa ścieżkę pliku psd1, który określa dane konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="85f12-125">Specifies the path of a .psd1 file that specifies the data for the configuration.</span></span>
<span data-ttu-id="85f12-126">Zostanie ona dodana do archiwum konfiguracji, a następnie przekazana do funkcji konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="85f12-126">This is added to the configuration archive and then passed to the configuration function.</span></span>
<span data-ttu-id="85f12-127">Zostanie zastąpiona ścieżką danych konfiguracyjnych dostarczaną za pośrednictwem polecenia cmdlet Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="85f12-127">It gets overwritten by the configuration data path provided through the Set-AzVMDscExtension cmdlet</span></span>

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

### <span data-ttu-id="85f12-128">-ConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="85f12-128">-ConfigurationPath</span></span>
<span data-ttu-id="85f12-129">Określa ścieżkę pliku zawierającego co najmniej jeden wariant.</span><span class="sxs-lookup"><span data-stu-id="85f12-129">Specifies the path of a file that contains one or more configurations.</span></span>
<span data-ttu-id="85f12-130">Plik może być plikiem skryptu programu Windows PowerShell (. ps1) lub plikiem modułu programu Windows PowerShell (. PSM1).</span><span class="sxs-lookup"><span data-stu-id="85f12-130">The file can be a Windows PowerShell script (.ps1) file or a Windows PowerShell module (.psm1) file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="85f12-131">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="85f12-131">-ContainerName</span></span>
<span data-ttu-id="85f12-132">Określa nazwę kontenera magazynu platformy Azure, do którego jest przekazywana konfiguracja.</span><span class="sxs-lookup"><span data-stu-id="85f12-132">Specifies the name of the Azure storage container the configuration is uploaded to.</span></span>

```yaml
Type: System.String
Parameter Sets: UploadArchive
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85f12-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85f12-133">-DefaultProfile</span></span>
<span data-ttu-id="85f12-134">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="85f12-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85f12-135">-Force</span><span class="sxs-lookup"><span data-stu-id="85f12-135">-Force</span></span>
<span data-ttu-id="85f12-136">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="85f12-136">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="85f12-137">-OutputArchivePath</span><span class="sxs-lookup"><span data-stu-id="85f12-137">-OutputArchivePath</span></span>
<span data-ttu-id="85f12-138">Określa ścieżkę lokalnego pliku. zip, w którym ma zostać napisana archiwum konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="85f12-138">Specifies the path of a local .zip file to write the configuration archive to.</span></span>
<span data-ttu-id="85f12-139">Gdy ten parametr jest wykorzystywany, skrypt konfiguracji nie jest przekazywany do magazynu obiektów blob platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="85f12-139">When this parameter is used, the configuration script is not uploaded to Azure blob storage.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateArchive
Aliases: ConfigurationArchivePath

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85f12-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85f12-140">-ResourceGroupName</span></span>
<span data-ttu-id="85f12-141">Określa nazwę grupy zasobów zawierającej konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="85f12-141">Specifies the name of the resource group that contains the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: UploadArchive
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85f12-142">-SkipDependencyDetection</span><span class="sxs-lookup"><span data-stu-id="85f12-142">-SkipDependencyDetection</span></span>
<span data-ttu-id="85f12-143">Wskazuje, że to polecenie cmdlet wyklucza zależności zasobu DSC z archiwum konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="85f12-143">Indicates that this cmdlet excludes DSC resource dependencies from the configuration archive.</span></span>

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

### <span data-ttu-id="85f12-144">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="85f12-144">-StorageAccountName</span></span>
<span data-ttu-id="85f12-145">Określa nazwę konta usługi Azure Storage, która jest używana do przekazania skryptu konfiguracji do kontenera określonego przez parametr *ContainerName* .</span><span class="sxs-lookup"><span data-stu-id="85f12-145">Specifies the Azure storage account name that is used to upload the configuration script to the container specified by the *ContainerName* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: UploadArchive
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85f12-146">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="85f12-146">-StorageEndpointSuffix</span></span>
<span data-ttu-id="85f12-147">Określa sufiks punktu końcowego magazynu.</span><span class="sxs-lookup"><span data-stu-id="85f12-147">Specifies the suffix for the storage end point.</span></span>

```yaml
Type: System.String
Parameter Sets: UploadArchive
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85f12-148">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="85f12-148">-Confirm</span></span>
<span data-ttu-id="85f12-149">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85f12-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85f12-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85f12-150">-WhatIf</span></span>
<span data-ttu-id="85f12-151">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85f12-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85f12-152">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="85f12-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85f12-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85f12-153">CommonParameters</span></span>
<span data-ttu-id="85f12-154">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85f12-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85f12-155">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="85f12-155">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85f12-156">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="85f12-156">INPUTS</span></span>

### <span data-ttu-id="85f12-157">System. String</span><span class="sxs-lookup"><span data-stu-id="85f12-157">System.String</span></span>

### <span data-ttu-id="85f12-158">System. String []</span><span class="sxs-lookup"><span data-stu-id="85f12-158">System.String[]</span></span>

## <span data-ttu-id="85f12-159">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="85f12-159">OUTPUTS</span></span>

### <span data-ttu-id="85f12-160">System. String</span><span class="sxs-lookup"><span data-stu-id="85f12-160">System.String</span></span>

## <span data-ttu-id="85f12-161">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="85f12-161">NOTES</span></span>

## <span data-ttu-id="85f12-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="85f12-162">RELATED LINKS</span></span>

[<span data-ttu-id="85f12-163">Get-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="85f12-163">Get-AzVMDscExtension</span></span>](./Get-AzVMDscExtension.md)

[<span data-ttu-id="85f12-164">Remove-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="85f12-164">Remove-AzVMDscExtension</span></span>](./Remove-AzVMDscExtension.md)

[<span data-ttu-id="85f12-165">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="85f12-165">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)


