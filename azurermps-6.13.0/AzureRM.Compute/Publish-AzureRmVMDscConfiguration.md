---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: FB9ACBA2-081E-4876-A21A-F5BA11CBEDA2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/publish-azurermvmdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Publish-AzureRmVMDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Publish-AzureRmVMDscConfiguration.md
ms.openlocfilehash: 49dc91288c955de10c3dbcb84da74ffd3d71f140
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524542"
---
# <span data-ttu-id="cf222-101">Publish-AzureRmVMDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="cf222-101">Publish-AzureRmVMDscConfiguration</span></span>

## <span data-ttu-id="cf222-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cf222-102">SYNOPSIS</span></span>
<span data-ttu-id="cf222-103">Przekazywanie skryptu DSC do magazynu obiektów blob platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="cf222-103">Uploads a DSC script to Azure blob storage.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cf222-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cf222-104">SYNTAX</span></span>

### <span data-ttu-id="cf222-105">UploadArchive (domyślny)</span><span class="sxs-lookup"><span data-stu-id="cf222-105">UploadArchive (Default)</span></span>
```
Publish-AzureRmVMDscConfiguration [-ResourceGroupName] <String> [-ConfigurationPath] <String>
 [[-ContainerName] <String>] [-StorageAccountName] <String> [-StorageEndpointSuffix <String>] [-Force]
 [-SkipDependencyDetection] [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf222-106">Funkcja Zarchiwizuj</span><span class="sxs-lookup"><span data-stu-id="cf222-106">CreateArchive</span></span>
```
Publish-AzureRmVMDscConfiguration [-ConfigurationPath] <String> [[-OutputArchivePath] <String>] [-Force]
 [-SkipDependencyDetection] [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf222-107">Opis</span><span class="sxs-lookup"><span data-stu-id="cf222-107">DESCRIPTION</span></span>
<span data-ttu-id="cf222-108">Polecenie cmdlet **Publish-AzureRmVMDscConfiguration** umożliwia przekazanie skryptu konfiguracji stanu (DSC) do magazynu obiektów blob platformy Azure, który później można zastosować do maszyn wirtualnych platformy Azure przy użyciu polecenia cmdlet Set-AzureRmVMDscExtension.</span><span class="sxs-lookup"><span data-stu-id="cf222-108">The **Publish-AzureRmVMDscConfiguration** cmdlet uploads a Desired State Configuration (DSC) script to Azure blob storage, which later can be applied to Azure virtual machines using the Set-AzureRmVMDscExtension cmdlet.</span></span>

## <span data-ttu-id="cf222-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cf222-109">EXAMPLES</span></span>

### <span data-ttu-id="cf222-110">Przykład 1: Tworzenie pakietu zip przekazywanie go do magazynu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="cf222-110">Example 1: Create a .zip package an upload it to Azure storage</span></span>
```
PS C:\> Publish-AzureRmVMDscConfiguration ".\MyConfiguration.ps1"
```

<span data-ttu-id="cf222-111">To polecenie tworzy pakiet ZIP dla danego skryptu i wszystkich modułów zasobów zależnych, a następnie przekazuje go do magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="cf222-111">This command creates a .zip package for the given script and any dependent resource modules and uploads it to Azure storage.</span></span>

### <span data-ttu-id="cf222-112">Przykład 2: Tworzenie pakietu zip i przechowywanie go w pliku lokalnym</span><span class="sxs-lookup"><span data-stu-id="cf222-112">Example 2: Create a .zip package and store it to a local file</span></span>
```
PS C:\> Publish-AzureRmVMDscConfiguration ".\MyConfiguration.ps1" -OutputArchivePath ".\MyConfiguration.ps1.zip"
```

<span data-ttu-id="cf222-113">To polecenie tworzy pakiet ZIP dla danego skryptu i wszystkich modułów zasobów zależnych i zapisuje go w pliku lokalnym o nazwie .\MyConfiguration.ps1.zip.</span><span class="sxs-lookup"><span data-stu-id="cf222-113">This command creates a .zip package for the given script and any dependent resource modules and stores it in the local file that is named .\MyConfiguration.ps1.zip.</span></span>

### <span data-ttu-id="cf222-114">Przykład 3: Dodawanie konfiguracji do archiwum, a następnie przekazywanie go do magazynu</span><span class="sxs-lookup"><span data-stu-id="cf222-114">Example 3: Add configuration to the archive and then upload it to storage</span></span>
```
PS C:\> Publish-AzureRmVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -SkipDependencyDetection
```

<span data-ttu-id="cf222-115">To polecenie dodaje konfigurację o nazwie Sample.ps1 do archiwum konfiguracji w celu przekazania do magazynu platformy Azure i pominięcie modułów zasobów zależnych.</span><span class="sxs-lookup"><span data-stu-id="cf222-115">This command adds configuration named Sample.ps1 to the configuration archive to upload to Azure storage and skips dependent resource modules.</span></span>

### <span data-ttu-id="cf222-116">Przykład 4: Dodawanie danych konfiguracji i konfiguracji do archiwum, a następnie przekazywanie go do magazynu</span><span class="sxs-lookup"><span data-stu-id="cf222-116">Example 4: Add configuration and configuration data to the archive and then upload it to storage</span></span>
```
PS C:\> Publish-AzureRmVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -ConfigurationDataPath "C:\SampleData.psd1"
```

<span data-ttu-id="cf222-117">To polecenie dodaje konfigurację o nazwie Sample.ps1 i dane konfiguracji o nazwie SampleData.psd1 do archiwum konfiguracji w celu przekazania do magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="cf222-117">This command adds configuration named Sample.ps1 and configuration data named SampleData.psd1 to the configuration archive to upload to Azure storage.</span></span>

### <span data-ttu-id="cf222-118">Przykład 5: Dodawanie konfiguracji, danych konfiguracyjnych i dodatkowej zawartości do archiwum, a następnie przekazywanie go do miejsca do magazynowania</span><span class="sxs-lookup"><span data-stu-id="cf222-118">Example 5: Add configuration, configuration data, and additional content to the archive and then upload it to storage</span></span>
```
PS C:\> Publish-AzureRmVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -AdditionalPath @("C:\ContentDir1", "C:\File.txt") -ConfigurationDataPath "C:\SampleData.psd1"
```

<span data-ttu-id="cf222-119">To polecenie umożliwia dodanie konfiguracji o nazwie Sample.ps1, danych konfiguracji SampleData.psd1 oraz dodatkowej zawartości do archiwum konfiguracji w celu przekazania do magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="cf222-119">This command adds configuration named Sample.ps1, configuration data SampleData.psd1, and additional content to configuration archive to upload to Azure storage.</span></span>

## <span data-ttu-id="cf222-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cf222-120">PARAMETERS</span></span>

### <span data-ttu-id="cf222-121">-AdditionalPath</span><span class="sxs-lookup"><span data-stu-id="cf222-121">-AdditionalPath</span></span>
<span data-ttu-id="cf222-122">Określa ścieżkę pliku lub katalogu, który ma zostać uwzględniony w archiwum konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="cf222-122">Specifies the path of a file or a directory to include in the configuration archive.</span></span>
<span data-ttu-id="cf222-123">Pobieranie zostanie pobrane na maszynie wirtualnej wraz z konfiguracją.</span><span class="sxs-lookup"><span data-stu-id="cf222-123">It gets downloaded to the virtual machine together with the configuration.</span></span>

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

### <span data-ttu-id="cf222-124">-ConfigurationDataPath</span><span class="sxs-lookup"><span data-stu-id="cf222-124">-ConfigurationDataPath</span></span>
<span data-ttu-id="cf222-125">Określa ścieżkę pliku psd1, który określa dane konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="cf222-125">Specifies the path of a .psd1 file that specifies the data for the configuration.</span></span>
<span data-ttu-id="cf222-126">Zostanie ona dodana do archiwum konfiguracji, a następnie przekazana do funkcji konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="cf222-126">This is added to the configuration archive and then passed to the configuration function.</span></span>
<span data-ttu-id="cf222-127">Zostanie zastąpiona ścieżką danych konfiguracyjnych dostarczaną za pośrednictwem polecenia cmdlet Set-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="cf222-127">It gets overwritten by the configuration data path provided through the Set-AzureRmVMDscExtension cmdlet</span></span>

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

### <span data-ttu-id="cf222-128">-ConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="cf222-128">-ConfigurationPath</span></span>
<span data-ttu-id="cf222-129">Określa ścieżkę pliku zawierającego co najmniej jeden wariant.</span><span class="sxs-lookup"><span data-stu-id="cf222-129">Specifies the path of a file that contains one or more configurations.</span></span>
<span data-ttu-id="cf222-130">Plik może być plikiem skryptu programu Windows PowerShell (. ps1) lub plikiem modułu programu Windows PowerShell (. PSM1).</span><span class="sxs-lookup"><span data-stu-id="cf222-130">The file can be a Windows PowerShell script (.ps1) file or a Windows PowerShell module (.psm1) file.</span></span>

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

### <span data-ttu-id="cf222-131">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="cf222-131">-ContainerName</span></span>
<span data-ttu-id="cf222-132">Określa nazwę kontenera magazynu platformy Azure, do którego jest przekazywana konfiguracja.</span><span class="sxs-lookup"><span data-stu-id="cf222-132">Specifies the name of the Azure storage container the configuration is uploaded to.</span></span>

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

### <span data-ttu-id="cf222-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf222-133">-DefaultProfile</span></span>
<span data-ttu-id="cf222-134">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cf222-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf222-135">-Force</span><span class="sxs-lookup"><span data-stu-id="cf222-135">-Force</span></span>
<span data-ttu-id="cf222-136">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="cf222-136">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cf222-137">-OutputArchivePath</span><span class="sxs-lookup"><span data-stu-id="cf222-137">-OutputArchivePath</span></span>
<span data-ttu-id="cf222-138">Określa ścieżkę lokalnego pliku. zip, w którym ma zostać napisana archiwum konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="cf222-138">Specifies the path of a local .zip file to write the configuration archive to.</span></span>
<span data-ttu-id="cf222-139">Gdy ten parametr jest wykorzystywany, skrypt konfiguracji nie jest przekazywany do magazynu obiektów blob platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="cf222-139">When this parameter is used, the configuration script is not uploaded to Azure blob storage.</span></span>

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

### <span data-ttu-id="cf222-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf222-140">-ResourceGroupName</span></span>
<span data-ttu-id="cf222-141">Określa nazwę grupy zasobów zawierającej konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="cf222-141">Specifies the name of the resource group that contains the storage account.</span></span>

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

### <span data-ttu-id="cf222-142">-SkipDependencyDetection</span><span class="sxs-lookup"><span data-stu-id="cf222-142">-SkipDependencyDetection</span></span>
<span data-ttu-id="cf222-143">Wskazuje, że to polecenie cmdlet wyklucza zależności zasobu DSC z archiwum konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="cf222-143">Indicates that this cmdlet excludes DSC resource dependencies from the configuration archive.</span></span>

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

### <span data-ttu-id="cf222-144">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="cf222-144">-StorageAccountName</span></span>
<span data-ttu-id="cf222-145">Określa nazwę konta usługi Azure Storage, która jest używana do przekazania skryptu konfiguracji do kontenera określonego przez parametr *ContainerName* .</span><span class="sxs-lookup"><span data-stu-id="cf222-145">Specifies the Azure storage account name that is used to upload the configuration script to the container specified by the *ContainerName* parameter.</span></span>

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

### <span data-ttu-id="cf222-146">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="cf222-146">-StorageEndpointSuffix</span></span>
<span data-ttu-id="cf222-147">Określa sufiks punktu końcowego magazynu.</span><span class="sxs-lookup"><span data-stu-id="cf222-147">Specifies the suffix for the storage end point.</span></span>

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

### <span data-ttu-id="cf222-148">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cf222-148">-Confirm</span></span>
<span data-ttu-id="cf222-149">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf222-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf222-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf222-150">-WhatIf</span></span>
<span data-ttu-id="cf222-151">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf222-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf222-152">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="cf222-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf222-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf222-153">CommonParameters</span></span>
<span data-ttu-id="cf222-154">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf222-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf222-155">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf222-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf222-156">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cf222-156">INPUTS</span></span>

### <span data-ttu-id="cf222-157">System. String</span><span class="sxs-lookup"><span data-stu-id="cf222-157">System.String</span></span>

### <span data-ttu-id="cf222-158">System. String []</span><span class="sxs-lookup"><span data-stu-id="cf222-158">System.String[]</span></span>

## <span data-ttu-id="cf222-159">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cf222-159">OUTPUTS</span></span>

### <span data-ttu-id="cf222-160">System. String</span><span class="sxs-lookup"><span data-stu-id="cf222-160">System.String</span></span>

## <span data-ttu-id="cf222-161">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cf222-161">NOTES</span></span>

## <span data-ttu-id="cf222-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cf222-162">RELATED LINKS</span></span>

[<span data-ttu-id="cf222-163">Get-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="cf222-163">Get-AzureRmVMDscExtension</span></span>](./Get-AzureRmVMDscExtension.md)

[<span data-ttu-id="cf222-164">Remove-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="cf222-164">Remove-AzureRmVMDscExtension</span></span>](./Remove-AzureRmVMDscExtension.md)

[<span data-ttu-id="cf222-165">Set-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="cf222-165">Set-AzureRmVMDscExtension</span></span>](./Set-AzureRmVMDscExtension.md)


