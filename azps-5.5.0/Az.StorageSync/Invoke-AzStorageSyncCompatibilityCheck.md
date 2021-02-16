---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/invoke-azstoragesynccompatibilitycheck
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncCompatibilityCheck.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncCompatibilityCheck.md
ms.openlocfilehash: 51882269c342e766a3b714f931486eca437b9e58
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197451"
---
# <span data-ttu-id="cc71d-101">Invoke-AzStorageSyncCompatibilityCheck</span><span class="sxs-lookup"><span data-stu-id="cc71d-101">Invoke-AzStorageSyncCompatibilityCheck</span></span>

## <span data-ttu-id="cc71d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc71d-102">SYNOPSIS</span></span>
<span data-ttu-id="cc71d-103">Sprawdza potencjalne problemy ze zgodnością między systemem a usługą Azure File Sync.</span><span class="sxs-lookup"><span data-stu-id="cc71d-103">Checks for potential compatibility issues between your system and Azure File Sync.</span></span>

## <span data-ttu-id="cc71d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="cc71d-104">SYNTAX</span></span>

### <span data-ttu-id="cc71d-105">PathBased (Default)</span><span class="sxs-lookup"><span data-stu-id="cc71d-105">PathBased (Default)</span></span>
```
Invoke-AzStorageSyncCompatibilityCheck [-Path] <String> [-Credential <PSCredential>] [-SkipSystemChecks]
 [-SkipNamespaceChecks] [<CommonParameters>]
```

### <span data-ttu-id="cc71d-106">ComputerNameBased</span><span class="sxs-lookup"><span data-stu-id="cc71d-106">ComputerNameBased</span></span>
```
Invoke-AzStorageSyncCompatibilityCheck [-Credential <PSCredential>] [-ComputerName] <String>
 [-SkipSystemChecks] [<CommonParameters>]
```

## <span data-ttu-id="cc71d-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="cc71d-107">DESCRIPTION</span></span>
<span data-ttu-id="cc71d-108">Polecenie cmdlet **Invoke-AzStorageSyncCompatibilityCheck** sprawdza, czy nie ma potencjalnych problemów ze zgodnością między systemem a usługą Azure File Sync. Gdy jest to ścieżka lokalna lub zdalna, wykonuje ona zestaw sprawdzania poprawności w przestrzeni nazw systemu i pliku, a następnie zwraca znalezione problemy ze zgodnością.</span><span class="sxs-lookup"><span data-stu-id="cc71d-108">The **Invoke-AzStorageSyncCompatibilityCheck** cmdlet checks for potential compatibility issues between your system and Azure File Sync. Given a local or remote path, it performs a set of validations on the system and file namespace, and then returns any compatibility issues it finds.</span></span>
<span data-ttu-id="cc71d-109">Testy systemu:</span><span class="sxs-lookup"><span data-stu-id="cc71d-109">System checks:</span></span>
- <span data-ttu-id="cc71d-110">Sprawdza przestrzeń nazw plików zgodności systemu operacyjnego:</span><span class="sxs-lookup"><span data-stu-id="cc71d-110">OS compatibility File namespace checks:</span></span>
- <span data-ttu-id="cc71d-111">Nieobsługiwane znaki</span><span class="sxs-lookup"><span data-stu-id="cc71d-111">Unsupported characters</span></span>
- <span data-ttu-id="cc71d-112">Maksymalny rozmiar pliku</span><span class="sxs-lookup"><span data-stu-id="cc71d-112">Maximum file size</span></span>
- <span data-ttu-id="cc71d-113">Maksymalna długość ścieżki</span><span class="sxs-lookup"><span data-stu-id="cc71d-113">Maximum path length</span></span>
- <span data-ttu-id="cc71d-114">Maksymalna długość pliku</span><span class="sxs-lookup"><span data-stu-id="cc71d-114">Maximum file length</span></span>
- <span data-ttu-id="cc71d-115">Maksymalny rozmiar zestawu danych</span><span class="sxs-lookup"><span data-stu-id="cc71d-115">Maximum dataset size</span></span>
- <span data-ttu-id="cc71d-116">Maksymalna głębokość katalogu</span><span class="sxs-lookup"><span data-stu-id="cc71d-116">Maximum directory depth</span></span>

## <span data-ttu-id="cc71d-117">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="cc71d-117">EXAMPLES</span></span>

### <span data-ttu-id="cc71d-118">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cc71d-118">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncCompatibilityCheck C:\DATA
```

<span data-ttu-id="cc71d-119">To polecenie sprawdza zgodność systemu, a także plików i folderów w folderze C:\DATA.</span><span class="sxs-lookup"><span data-stu-id="cc71d-119">This command checks the compatibility of the system and also of files and folders in C:\DATA.</span></span>

### <span data-ttu-id="cc71d-120">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="cc71d-120">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncCompatibilityCheck C:\DATA -SkipSystemChecks
```

<span data-ttu-id="cc71d-121">To polecenie sprawdza zgodność plików i folderów w folderze C:\DATA, ale nie sprawdza zgodności systemu.</span><span class="sxs-lookup"><span data-stu-id="cc71d-121">This command checks the compatibility of files and folders in C:\DATA, but does not perform a system compatibility check.</span></span>

### <span data-ttu-id="cc71d-122">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="cc71d-122">Example 3</span></span>
```powershell
PS C:\> $validation = Invoke-AzStorageSyncCompatibilityCheck C:\DATA
PS C:\> $validation.Results | Select-Object -Property Type, Path, Level, Description, Result | Export-Csv -Path C:\results.csv -Encoding utf8
```

<span data-ttu-id="cc71d-123">To polecenie sprawdza zgodność systemu, a także plików i folderów w folderze C:\DATA, a następnie eksportuje wyniki jako plik CSV do folderu C:\results.</span><span class="sxs-lookup"><span data-stu-id="cc71d-123">This command checks the compatibility of the system and also of files and folders in C:\DATA, and then exports the results as a CSV file to C:\results.</span></span>

## <span data-ttu-id="cc71d-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cc71d-124">PARAMETERS</span></span>

### <span data-ttu-id="cc71d-125">— Nazwa_komputera</span><span class="sxs-lookup"><span data-stu-id="cc71d-125">-ComputerName</span></span>
<span data-ttu-id="cc71d-126">Komputer, na który jest sprawdzana ta kontrola.</span><span class="sxs-lookup"><span data-stu-id="cc71d-126">The computer you are performing this check on.</span></span>

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

### <span data-ttu-id="cc71d-127">- Credential</span><span class="sxs-lookup"><span data-stu-id="cc71d-127">-Credential</span></span>
<span data-ttu-id="cc71d-128">Poświadczenia dla ważnego udziału.</span><span class="sxs-lookup"><span data-stu-id="cc71d-128">Your credentials for the share you are validating.</span></span>

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

### <span data-ttu-id="cc71d-129">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="cc71d-129">-Path</span></span>
<span data-ttu-id="cc71d-130">Ścieżka UNC dla ważnego udziału.</span><span class="sxs-lookup"><span data-stu-id="cc71d-130">The UNC path of the share you are validating.</span></span>

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

### <span data-ttu-id="cc71d-131">-SkipNamespaceChecks</span><span class="sxs-lookup"><span data-stu-id="cc71d-131">-SkipNamespaceChecks</span></span>
<span data-ttu-id="cc71d-132">Ustaw tę flagę, aby pominąć sprawdzanie poprawności przestrzeni nazw plików i wykonać tylko sprawdzanie poprawności systemu.</span><span class="sxs-lookup"><span data-stu-id="cc71d-132">Set this flag to skip file namespace validations and only perform system validations.</span></span>

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

### <span data-ttu-id="cc71d-133">-SkipSystemChecks</span><span class="sxs-lookup"><span data-stu-id="cc71d-133">-SkipSystemChecks</span></span>
<span data-ttu-id="cc71d-134">Ustaw tę flagę, aby pominąć sprawdzanie poprawności systemu i wykonać tylko sprawdzanie poprawności przestrzeni nazw plików.</span><span class="sxs-lookup"><span data-stu-id="cc71d-134">Set this flag to skip system validations and only perform file namespace validations.</span></span>

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

### <span data-ttu-id="cc71d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc71d-135">CommonParameters</span></span>
<span data-ttu-id="cc71d-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc71d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc71d-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc71d-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc71d-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cc71d-138">INPUTS</span></span>

### <span data-ttu-id="cc71d-139">Brak</span><span class="sxs-lookup"><span data-stu-id="cc71d-139">None</span></span>

## <span data-ttu-id="cc71d-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cc71d-140">OUTPUTS</span></span>

### <span data-ttu-id="cc71d-141">Microsoft.Azure.Commands.StorageSync.Evaluation.Models.PSValidationResult</span><span class="sxs-lookup"><span data-stu-id="cc71d-141">Microsoft.Azure.Commands.StorageSync.Evaluation.Models.PSValidationResult</span></span>

## <span data-ttu-id="cc71d-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="cc71d-142">NOTES</span></span>
* <span data-ttu-id="cc71d-143">Słowa kluczowe: azure, Az, arm, resource, management, storagesync, filesync</span><span class="sxs-lookup"><span data-stu-id="cc71d-143">Keywords: azure, Az, arm, resource, management, storagesync, filesync</span></span>

## <span data-ttu-id="cc71d-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cc71d-144">RELATED LINKS</span></span>
