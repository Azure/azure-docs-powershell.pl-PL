---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/az.storagesync/invoke-azstoragesynccompatibilitycheck
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncCompatibilityCheck.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncCompatibilityCheck.md
ms.openlocfilehash: b6052172ecca2821b1373d93a8de870969a6b4f7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002209"
---
# <span data-ttu-id="025da-101">Invoke-AzStorageSyncCompatibilityCheck</span><span class="sxs-lookup"><span data-stu-id="025da-101">Invoke-AzStorageSyncCompatibilityCheck</span></span>

## <span data-ttu-id="025da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="025da-102">SYNOPSIS</span></span>
<span data-ttu-id="025da-103">Sprawdza potencjalne problemy ze zgodnością między systemem a usługą Azure File Sync.</span><span class="sxs-lookup"><span data-stu-id="025da-103">Checks for potential compatibility issues between your system and Azure File Sync.</span></span>

## <span data-ttu-id="025da-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="025da-104">SYNTAX</span></span>

### <span data-ttu-id="025da-105">PathBased (Default)</span><span class="sxs-lookup"><span data-stu-id="025da-105">PathBased (Default)</span></span>
```
Invoke-AzStorageSyncCompatibilityCheck [-Path] <String> [-Credential <PSCredential>] [-SkipSystemChecks]
 [-SkipNamespaceChecks] [<CommonParameters>]
```

### <span data-ttu-id="025da-106">ComputerNameBased</span><span class="sxs-lookup"><span data-stu-id="025da-106">ComputerNameBased</span></span>
```
Invoke-AzStorageSyncCompatibilityCheck [-Credential <PSCredential>] [-ComputerName] <String>
 [-SkipSystemChecks] [<CommonParameters>]
```

## <span data-ttu-id="025da-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="025da-107">DESCRIPTION</span></span>
<span data-ttu-id="025da-108">Polecenie **cmdlet Invoke-AzStorageSyncCompatibilityCheck** sprawdza, czy nie ma potencjalnych problemów ze zgodnością między systemem a usługą Azure File Sync. Gdy jest to ścieżka lokalna lub zdalna, wykonuje ona zestaw sprawdzania poprawności w przestrzeni nazw systemu i pliku, a następnie zwraca znalezione problemy ze zgodnością.</span><span class="sxs-lookup"><span data-stu-id="025da-108">The **Invoke-AzStorageSyncCompatibilityCheck** cmdlet checks for potential compatibility issues between your system and Azure File Sync. Given a local or remote path, it performs a set of validations on the system and file namespace, and then returns any compatibility issues it finds.</span></span>
<span data-ttu-id="025da-109">Testy systemu:</span><span class="sxs-lookup"><span data-stu-id="025da-109">System checks:</span></span>
- <span data-ttu-id="025da-110">Sprawdza przestrzeń nazw plików zgodności systemu operacyjnego:</span><span class="sxs-lookup"><span data-stu-id="025da-110">OS compatibility File namespace checks:</span></span>
- <span data-ttu-id="025da-111">Nieobsługiwane znaki</span><span class="sxs-lookup"><span data-stu-id="025da-111">Unsupported characters</span></span>
- <span data-ttu-id="025da-112">Maksymalny rozmiar pliku</span><span class="sxs-lookup"><span data-stu-id="025da-112">Maximum file size</span></span>
- <span data-ttu-id="025da-113">Maksymalna długość ścieżki</span><span class="sxs-lookup"><span data-stu-id="025da-113">Maximum path length</span></span>
- <span data-ttu-id="025da-114">Maksymalna długość pliku</span><span class="sxs-lookup"><span data-stu-id="025da-114">Maximum file length</span></span>
- <span data-ttu-id="025da-115">Maksymalny rozmiar zestawu danych</span><span class="sxs-lookup"><span data-stu-id="025da-115">Maximum dataset size</span></span>
- <span data-ttu-id="025da-116">Maksymalna głębokość katalogu</span><span class="sxs-lookup"><span data-stu-id="025da-116">Maximum directory depth</span></span>

## <span data-ttu-id="025da-117">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="025da-117">EXAMPLES</span></span>

### <span data-ttu-id="025da-118">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="025da-118">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncCompatibilityCheck C:\DATA
```

<span data-ttu-id="025da-119">To polecenie sprawdza zgodność systemu, a także plików i folderów w folderze C:\DATA.</span><span class="sxs-lookup"><span data-stu-id="025da-119">This command checks the compatibility of the system and also of files and folders in C:\DATA.</span></span>

### <span data-ttu-id="025da-120">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="025da-120">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncCompatibilityCheck C:\DATA -SkipSystemChecks
```

<span data-ttu-id="025da-121">To polecenie sprawdza zgodność plików i folderów w folderze C:\DATA, ale nie sprawdza zgodności systemu.</span><span class="sxs-lookup"><span data-stu-id="025da-121">This command checks the compatibility of files and folders in C:\DATA, but does not perform a system compatibility check.</span></span>

### <span data-ttu-id="025da-122">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="025da-122">Example 3</span></span>
```powershell
PS C:\> $validation = Invoke-AzStorageSyncCompatibilityCheck C:\DATA
PS C:\> $validation.Results | Select-Object -Property Type, Path, Level, Description, Result | Export-Csv -Path C:\results.csv -Encoding utf8
```

<span data-ttu-id="025da-123">To polecenie sprawdza zgodność systemu, a także plików i folderów w folderze C:\DATA, a następnie eksportuje wyniki jako plik CSV do folderu C:\results.</span><span class="sxs-lookup"><span data-stu-id="025da-123">This command checks the compatibility of the system and also of files and folders in C:\DATA, and then exports the results as a CSV file to C:\results.</span></span>

## <span data-ttu-id="025da-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="025da-124">PARAMETERS</span></span>

### <span data-ttu-id="025da-125">— Nazwa_komputera</span><span class="sxs-lookup"><span data-stu-id="025da-125">-ComputerName</span></span>
<span data-ttu-id="025da-126">Komputer, na który jest sprawdzana ta kontrola.</span><span class="sxs-lookup"><span data-stu-id="025da-126">The computer you are performing this check on.</span></span>

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

### <span data-ttu-id="025da-127">- Credential</span><span class="sxs-lookup"><span data-stu-id="025da-127">-Credential</span></span>
<span data-ttu-id="025da-128">Poświadczenia dla ważnego udziału.</span><span class="sxs-lookup"><span data-stu-id="025da-128">Your credentials for the share you are validating.</span></span>

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

### <span data-ttu-id="025da-129">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="025da-129">-Path</span></span>
<span data-ttu-id="025da-130">Ścieżka UNC dla ważnego udziału.</span><span class="sxs-lookup"><span data-stu-id="025da-130">The UNC path of the share you are validating.</span></span>

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

### <span data-ttu-id="025da-131">-SkipNamespaceChecks</span><span class="sxs-lookup"><span data-stu-id="025da-131">-SkipNamespaceChecks</span></span>
<span data-ttu-id="025da-132">Ustaw tę flagę, aby pominąć sprawdzanie poprawności przestrzeni nazw plików i wykonać tylko sprawdzanie poprawności systemu.</span><span class="sxs-lookup"><span data-stu-id="025da-132">Set this flag to skip file namespace validations and only perform system validations.</span></span>

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

### <span data-ttu-id="025da-133">-SkipSystemChecks</span><span class="sxs-lookup"><span data-stu-id="025da-133">-SkipSystemChecks</span></span>
<span data-ttu-id="025da-134">Ustaw tę flagę, aby pominąć sprawdzanie poprawności systemu i wykonać tylko sprawdzanie poprawności przestrzeni nazw plików.</span><span class="sxs-lookup"><span data-stu-id="025da-134">Set this flag to skip system validations and only perform file namespace validations.</span></span>

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

### <span data-ttu-id="025da-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="025da-135">CommonParameters</span></span>
<span data-ttu-id="025da-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="025da-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="025da-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="025da-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="025da-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="025da-138">INPUTS</span></span>

### <span data-ttu-id="025da-139">Brak</span><span class="sxs-lookup"><span data-stu-id="025da-139">None</span></span>

## <span data-ttu-id="025da-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="025da-140">OUTPUTS</span></span>

### <span data-ttu-id="025da-141">Microsoft.Azure.Commands.StorageSync.Evaluation.Models.PSValidationResult</span><span class="sxs-lookup"><span data-stu-id="025da-141">Microsoft.Azure.Commands.StorageSync.Evaluation.Models.PSValidationResult</span></span>

## <span data-ttu-id="025da-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="025da-142">NOTES</span></span>
* <span data-ttu-id="025da-143">Słowa kluczowe: azure, Az, arm, resource, management, storagesync, filesync</span><span class="sxs-lookup"><span data-stu-id="025da-143">Keywords: azure, Az, arm, resource, management, storagesync, filesync</span></span>

## <span data-ttu-id="025da-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="025da-144">RELATED LINKS</span></span>
