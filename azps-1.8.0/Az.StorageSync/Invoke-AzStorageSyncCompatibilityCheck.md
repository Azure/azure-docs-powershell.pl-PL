---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/invoke-azstoragesynccompatibilitycheck
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncCompatibilityCheck.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncCompatibilityCheck.md
ms.openlocfilehash: 16348feffd1f3befbb28c3e3ed73a54c2ae234ae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707462"
---
# <span data-ttu-id="7e92e-101">Invoke-AzStorageSyncCompatibilityCheck</span><span class="sxs-lookup"><span data-stu-id="7e92e-101">Invoke-AzStorageSyncCompatibilityCheck</span></span>

## <span data-ttu-id="7e92e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7e92e-102">SYNOPSIS</span></span>
<span data-ttu-id="7e92e-103">Sprawdza potencjalne problemy ze zgodnością między systemem a synchronizacją plików platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7e92e-103">Checks for potential compatibility issues between your system and Azure File Sync.</span></span>

## <span data-ttu-id="7e92e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7e92e-104">SYNTAX</span></span>

### <span data-ttu-id="7e92e-105">PathBased (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7e92e-105">PathBased (Default)</span></span>
```
Invoke-AzStorageSyncCompatibilityCheck [-Path] <String> [-Credential <PSCredential>] [-SkipSystemChecks]
 [-SkipNamespaceChecks] [<CommonParameters>]
```

### <span data-ttu-id="7e92e-106">ComputerNameBased</span><span class="sxs-lookup"><span data-stu-id="7e92e-106">ComputerNameBased</span></span>
```
Invoke-AzStorageSyncCompatibilityCheck [-Credential <PSCredential>] [-ComputerName] <String>
 [-SkipSystemChecks] [<CommonParameters>]
```

## <span data-ttu-id="7e92e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="7e92e-107">DESCRIPTION</span></span>
<span data-ttu-id="7e92e-108">Polecenie cmdlet **Invoke-AzStorageSyncCompatibilityCheck** sprawdza potencjalne problemy ze zgodnością między systemem a synchronizacją plików platformy Azure. W przypadku ścieżki lokalnej lub zdalnej jest ona zbiorem funkcji sprawdzania poprawności w systemie i obszarze nazw plików, a następnie zwraca wszystkie znalezione problemy ze zgodnością.</span><span class="sxs-lookup"><span data-stu-id="7e92e-108">The **Invoke-AzStorageSyncCompatibilityCheck** cmdlet checks for potential compatibility issues between your system and Azure File Sync. Given a local or remote path, it performs a set of validations on the system and file namespace, and then returns any compatibility issues it finds.</span></span>
<span data-ttu-id="7e92e-109">Testy systemowe:</span><span class="sxs-lookup"><span data-stu-id="7e92e-109">System checks:</span></span>
- <span data-ttu-id="7e92e-110">Obszar nazw plików zgodności systemu operacyjnego:</span><span class="sxs-lookup"><span data-stu-id="7e92e-110">OS compatibility File namespace checks:</span></span>
- <span data-ttu-id="7e92e-111">Nieobsługiwane znaki</span><span class="sxs-lookup"><span data-stu-id="7e92e-111">Unsupported characters</span></span>
- <span data-ttu-id="7e92e-112">Maksymalny rozmiar pliku</span><span class="sxs-lookup"><span data-stu-id="7e92e-112">Maximum file size</span></span>
- <span data-ttu-id="7e92e-113">Maksymalna długość ścieżki</span><span class="sxs-lookup"><span data-stu-id="7e92e-113">Maximum path length</span></span>
- <span data-ttu-id="7e92e-114">Maksymalna długość pliku</span><span class="sxs-lookup"><span data-stu-id="7e92e-114">Maximum file length</span></span>
- <span data-ttu-id="7e92e-115">Maksymalny rozmiar zestawu danych</span><span class="sxs-lookup"><span data-stu-id="7e92e-115">Maximum dataset size</span></span>
- <span data-ttu-id="7e92e-116">Maksymalna głębokość katalogów</span><span class="sxs-lookup"><span data-stu-id="7e92e-116">Maximum directory depth</span></span>

## <span data-ttu-id="7e92e-117">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7e92e-117">EXAMPLES</span></span>

### <span data-ttu-id="7e92e-118">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7e92e-118">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncCompatibilityCheck C:\DATA
```

<span data-ttu-id="7e92e-119">To polecenie sprawdza zgodność systemu, a także plików i folderów w programie C:\DATA.</span><span class="sxs-lookup"><span data-stu-id="7e92e-119">This command checks the compatibility of the system and also of files and folders in C:\DATA.</span></span>

### <span data-ttu-id="7e92e-120">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="7e92e-120">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncCompatibilityCheck C:\DATA -SkipSystemChecks
```

<span data-ttu-id="7e92e-121">To polecenie sprawdza zgodność plików i folderów w programie C:\DATA, ale nie sprawdza zgodności systemu.</span><span class="sxs-lookup"><span data-stu-id="7e92e-121">This command checks the compatibility of files and folders in C:\DATA, but does not perform a system compatibility check.</span></span>

### <span data-ttu-id="7e92e-122">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="7e92e-122">Example 3</span></span>
```powershell
PS C:\> $validation = Invoke-AzStorageSyncCompatibilityCheck C:\DATA
PS C:\> $validation.Results | Select-Object -Property Type, Path, Level, Description, Result | Export-Csv -Path C:\results.csv -Encoding utf8
```

<span data-ttu-id="7e92e-123">To polecenie sprawdza zgodność systemu, a także plików i folderów w programie C:\DATA, a następnie eksportuje wyniki w postaci pliku CSV do C:\results.</span><span class="sxs-lookup"><span data-stu-id="7e92e-123">This command checks the compatibility of the system and also of files and folders in C:\DATA, and then exports the results as a CSV file to C:\results.</span></span>

## <span data-ttu-id="7e92e-124">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7e92e-124">PARAMETERS</span></span>

### <span data-ttu-id="7e92e-125">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="7e92e-125">-ComputerName</span></span>
<span data-ttu-id="7e92e-126">Komputer, na którym wykonywana jest ta kontrola.</span><span class="sxs-lookup"><span data-stu-id="7e92e-126">The computer you are performing this check on.</span></span>

```yaml
Type: String
Parameter Sets: ComputerNameBased
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e92e-127">— Poświadczenie</span><span class="sxs-lookup"><span data-stu-id="7e92e-127">-Credential</span></span>
<span data-ttu-id="7e92e-128">Twoje poświadczenia dla udziału, którego dotyczy Walidacja.</span><span class="sxs-lookup"><span data-stu-id="7e92e-128">Your credentials for the share you are validating.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e92e-129">-Path</span><span class="sxs-lookup"><span data-stu-id="7e92e-129">-Path</span></span>
<span data-ttu-id="7e92e-130">Ścieżka UNC udziału, którego dotyczy Walidacja.</span><span class="sxs-lookup"><span data-stu-id="7e92e-130">The UNC path of the share you are validating.</span></span>

```yaml
Type: String
Parameter Sets: PathBased
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e92e-131">-SkipNamespaceChecks</span><span class="sxs-lookup"><span data-stu-id="7e92e-131">-SkipNamespaceChecks</span></span>
<span data-ttu-id="7e92e-132">Ustaw tę flagę, aby pominąć sprawdzanie nazw plików i wykonywać tylko sprawdzanie poprawności systemu.</span><span class="sxs-lookup"><span data-stu-id="7e92e-132">Set this flag to skip file namespace validations and only perform system validations.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: PathBased
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e92e-133">-SkipSystemChecks</span><span class="sxs-lookup"><span data-stu-id="7e92e-133">-SkipSystemChecks</span></span>
<span data-ttu-id="7e92e-134">Ustaw tę flagę, aby pominąć sprawdzanie poprawności systemu i wykonać tylko sprawdzanie poprawności nazw plików.</span><span class="sxs-lookup"><span data-stu-id="7e92e-134">Set this flag to skip system validations and only perform file namespace validations.</span></span>

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

### <span data-ttu-id="7e92e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e92e-135">CommonParameters</span></span>
<span data-ttu-id="7e92e-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e92e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e92e-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e92e-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e92e-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7e92e-138">INPUTS</span></span>

### <span data-ttu-id="7e92e-139">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="7e92e-139">None</span></span>

## <span data-ttu-id="7e92e-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7e92e-140">OUTPUTS</span></span>

### <span data-ttu-id="7e92e-141">Microsoft. Azure. Commands. StorageSync. Evaluation. MODELES. PSValidationResult</span><span class="sxs-lookup"><span data-stu-id="7e92e-141">Microsoft.Azure.Commands.StorageSync.Evaluation.Models.PSValidationResult</span></span>

## <span data-ttu-id="7e92e-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7e92e-142">NOTES</span></span>
* <span data-ttu-id="7e92e-143">Słowa kluczowe: Azure, AZ, ARM, Resource, Management, storagesync, FileSync</span><span class="sxs-lookup"><span data-stu-id="7e92e-143">Keywords: azure, Az, arm, resource, management, storagesync, filesync</span></span>

## <span data-ttu-id="7e92e-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7e92e-144">RELATED LINKS</span></span>
