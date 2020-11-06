---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: AzureRM.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storagesync/invoke-azurermstoragesynccompatibilitycheck
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StorageSync/Commands.StorageSync/help/Invoke-AzureRmStorageSyncCompatibilityCheck.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StorageSync/Commands.StorageSync/help/Invoke-AzureRmStorageSyncCompatibilityCheck.md
ms.openlocfilehash: 73e0f00fe184a5462141b060717ca64567d4a67e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547280"
---
# <span data-ttu-id="00d04-101">Invoke-AzureRmStorageSyncCompatibilityCheck</span><span class="sxs-lookup"><span data-stu-id="00d04-101">Invoke-AzureRmStorageSyncCompatibilityCheck</span></span>

## <span data-ttu-id="00d04-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="00d04-102">SYNOPSIS</span></span>
<span data-ttu-id="00d04-103">Sprawdza potencjalne problemy ze zgodnością między systemem a synchronizacją plików platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="00d04-103">Checks for potential compatibility issues between your system and Azure File Sync.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="00d04-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="00d04-104">SYNTAX</span></span>

### <span data-ttu-id="00d04-105">PathBased (domyślny)</span><span class="sxs-lookup"><span data-stu-id="00d04-105">PathBased (Default)</span></span>
```
Invoke-AzureRmStorageSyncCompatibilityCheck [-Path] <String> [-Credential <PSCredential>] [-SkipSystemChecks]
 [-SkipNamespaceChecks] [-Quiet] [<CommonParameters>]
```

### <span data-ttu-id="00d04-106">ComputerNameBased</span><span class="sxs-lookup"><span data-stu-id="00d04-106">ComputerNameBased</span></span>
```
Invoke-AzureRmStorageSyncCompatibilityCheck [-Credential <PSCredential>] [-ComputerName] <String>
 [-SkipSystemChecks] [-Quiet] [<CommonParameters>]
```

## <span data-ttu-id="00d04-107">Opis</span><span class="sxs-lookup"><span data-stu-id="00d04-107">DESCRIPTION</span></span>
<span data-ttu-id="00d04-108">Polecenie cmdlet **Invoke-AzureRmStorageSyncCompatibilityCheck** sprawdza potencjalne problemy ze zgodnością między systemem a synchronizacją plików platformy Azure. W przypadku ścieżki lokalnej lub zdalnej jest ona zbiorem funkcji sprawdzania poprawności w systemie i obszarze nazw plików, a następnie zwraca wszystkie znalezione problemy ze zgodnością.</span><span class="sxs-lookup"><span data-stu-id="00d04-108">The **Invoke-AzureRmStorageSyncCompatibilityCheck** cmdlet checks for potential compatibility issues between your system and Azure File Sync. Given a local or remote path, it performs a set of validations on the system and file namespace, and then returns any compatibility issues it finds.</span></span>
<span data-ttu-id="00d04-109">Testy systemowe:</span><span class="sxs-lookup"><span data-stu-id="00d04-109">System checks:</span></span>
- <span data-ttu-id="00d04-110">Obszar nazw plików zgodności systemu operacyjnego:</span><span class="sxs-lookup"><span data-stu-id="00d04-110">OS compatibility File namespace checks:</span></span>
- <span data-ttu-id="00d04-111">Nieobsługiwane znaki</span><span class="sxs-lookup"><span data-stu-id="00d04-111">Unsupported characters</span></span>
- <span data-ttu-id="00d04-112">Maksymalny rozmiar pliku</span><span class="sxs-lookup"><span data-stu-id="00d04-112">Maximum file size</span></span>
- <span data-ttu-id="00d04-113">Maksymalna długość ścieżki</span><span class="sxs-lookup"><span data-stu-id="00d04-113">Maximum path length</span></span>
- <span data-ttu-id="00d04-114">Maksymalna długość pliku</span><span class="sxs-lookup"><span data-stu-id="00d04-114">Maximum file length</span></span>
- <span data-ttu-id="00d04-115">Maksymalny rozmiar zestawu danych</span><span class="sxs-lookup"><span data-stu-id="00d04-115">Maximum dataset size</span></span>
- <span data-ttu-id="00d04-116">Maksymalna głębokość katalogów</span><span class="sxs-lookup"><span data-stu-id="00d04-116">Maximum directory depth</span></span>

## <span data-ttu-id="00d04-117">Przykłady</span><span class="sxs-lookup"><span data-stu-id="00d04-117">EXAMPLES</span></span>

### <span data-ttu-id="00d04-118">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="00d04-118">Example 1</span></span>
```powershell
PS C:\> Invoke-AzureRmStorageSyncCompatibilityCheck C:\DATA
```

<span data-ttu-id="00d04-119">To polecenie sprawdza zgodność systemu, a także plików i folderów w programie C:\DATA.</span><span class="sxs-lookup"><span data-stu-id="00d04-119">This command checks the compatibility of the system and also of files and folders in C:\DATA.</span></span>

### <span data-ttu-id="00d04-120">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="00d04-120">Example 2</span></span>
```powershell
PS C:\> Invoke-AzureRmStorageSyncCompatibilityCheck C:\DATA -SkipSystemChecks
```

<span data-ttu-id="00d04-121">To polecenie sprawdza zgodność plików i folderów w programie C:\DATA, ale nie sprawdza zgodności systemu.</span><span class="sxs-lookup"><span data-stu-id="00d04-121">This command checks the compatibility of files and folders in C:\DATA, but does not perform a system compatibility check.</span></span>

### <span data-ttu-id="00d04-122">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="00d04-122">Example 3</span></span>
```powershell
PS C:\> $errors = Invoke-AzureRmStorageSyncCompatibilityCheck C:\DATA
PS C:\> $errors | Select-Object -Property Type, Path, Level, Description, Result | Export-Csv -Path C:\results
```

<span data-ttu-id="00d04-123">To polecenie sprawdza zgodność systemu, a także plików i folderów w programie C:\DATA, a następnie eksportuje wyniki w postaci pliku CSV do C:\results.</span><span class="sxs-lookup"><span data-stu-id="00d04-123">This command checks the compatibility of the system and also of files and folders in C:\DATA, and then exports the results as a CSV file to C:\results.</span></span>

## <span data-ttu-id="00d04-124">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="00d04-124">PARAMETERS</span></span>

### <span data-ttu-id="00d04-125">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="00d04-125">-ComputerName</span></span>
<span data-ttu-id="00d04-126">Komputer, na którym wykonywana jest ta kontrola.</span><span class="sxs-lookup"><span data-stu-id="00d04-126">The computer you are performing this check on.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputerNameBased
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00d04-127">— Poświadczenie</span><span class="sxs-lookup"><span data-stu-id="00d04-127">-Credential</span></span>
<span data-ttu-id="00d04-128">Twoje poświadczenia dla udziału, którego dotyczy Walidacja.</span><span class="sxs-lookup"><span data-stu-id="00d04-128">Your credentials for the share you are validating.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00d04-129">-Path</span><span class="sxs-lookup"><span data-stu-id="00d04-129">-Path</span></span>
<span data-ttu-id="00d04-130">Ścieżka UNC udziału, którego dotyczy Walidacja.</span><span class="sxs-lookup"><span data-stu-id="00d04-130">The UNC path of the share you are validating.</span></span>

```yaml
Type: System.String
Parameter Sets: PathBased
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00d04-131">-Quiet</span><span class="sxs-lookup"><span data-stu-id="00d04-131">-Quiet</span></span>
<span data-ttu-id="00d04-132">Pomijanie zapisywania raportu wyjściowego na konsoli.</span><span class="sxs-lookup"><span data-stu-id="00d04-132">Suppresses writing output report to console.</span></span>

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

### <span data-ttu-id="00d04-133">-SkipNamespaceChecks</span><span class="sxs-lookup"><span data-stu-id="00d04-133">-SkipNamespaceChecks</span></span>
<span data-ttu-id="00d04-134">Ustaw tę flagę, aby pominąć sprawdzanie nazw plików i wykonywać tylko sprawdzanie poprawności systemu.</span><span class="sxs-lookup"><span data-stu-id="00d04-134">Set this flag to skip file namespace validations and only perform system validations.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PathBased
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00d04-135">-SkipSystemChecks</span><span class="sxs-lookup"><span data-stu-id="00d04-135">-SkipSystemChecks</span></span>
<span data-ttu-id="00d04-136">Ustaw tę flagę, aby pominąć sprawdzanie poprawności systemu i wykonać tylko sprawdzanie poprawności nazw plików.</span><span class="sxs-lookup"><span data-stu-id="00d04-136">Set this flag to skip system validations and only perform file namespace validations.</span></span>

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

### <span data-ttu-id="00d04-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00d04-137">CommonParameters</span></span>
<span data-ttu-id="00d04-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00d04-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00d04-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00d04-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00d04-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="00d04-140">INPUTS</span></span>

### <span data-ttu-id="00d04-141">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="00d04-141">None</span></span>

## <span data-ttu-id="00d04-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="00d04-142">OUTPUTS</span></span>

### <span data-ttu-id="00d04-143">Microsoft. Azure. Commands. StorageSync. Evaluation. MODELES. PSValidationResult</span><span class="sxs-lookup"><span data-stu-id="00d04-143">Microsoft.Azure.Commands.StorageSync.Evaluation.Models.PSValidationResult</span></span>

## <span data-ttu-id="00d04-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="00d04-144">NOTES</span></span>
* <span data-ttu-id="00d04-145">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, storagesync, FileSync</span><span class="sxs-lookup"><span data-stu-id="00d04-145">Keywords: azure, azurerm, arm, resource, management, storagesync, filesync</span></span>

## <span data-ttu-id="00d04-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="00d04-146">RELATED LINKS</span></span>
