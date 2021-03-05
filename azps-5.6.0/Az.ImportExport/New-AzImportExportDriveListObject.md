---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/powershell/module/az.importexport/new-AzImportExportDriveListObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExportDriveListObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExportDriveListObject.md
ms.openlocfilehash: 4b3907e71dd8d457b1ab38ecd5cdc82b38d7b772
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970826"
---
# <span data-ttu-id="2c621-101">New-AzImportExportDriveListObject</span><span class="sxs-lookup"><span data-stu-id="2c621-101">New-AzImportExportDriveListObject</span></span>

## <span data-ttu-id="2c621-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c621-102">SYNOPSIS</span></span>
<span data-ttu-id="2c621-103">Utwórz obiekt DriverList for ImportExport.</span><span class="sxs-lookup"><span data-stu-id="2c621-103">Create a DriverList Object for ImportExport.</span></span>

## <span data-ttu-id="2c621-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2c621-104">SYNTAX</span></span>

```
New-AzImportExportDriveListObject [-BitLockerKey <String>] [-BytesSucceeded <Int64>] [-CopyStatus <String>]
 [-DriveHeaderHash <String>] [-DriveId <String>] [-ErrorLogUri <String>] [-ManifestFile <String>]
 [-ManifestHash <String>] [-ManifestUri <String>] [-PercentComplete <Int32>] [-State <DriveState>]
 [-VerboseLogUri <String>] [<CommonParameters>]
```

## <span data-ttu-id="2c621-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="2c621-105">DESCRIPTION</span></span>
<span data-ttu-id="2c621-106">Utwórz obiekt DriverList for ImportExport.</span><span class="sxs-lookup"><span data-stu-id="2c621-106">Create a DriverList Object for ImportExport.</span></span>

## <span data-ttu-id="2c621-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2c621-107">EXAMPLES</span></span>

### <span data-ttu-id="2c621-108">Przykład 1. Tworzenie nowego zadania Lista dysków dla zadania ImportExport</span><span class="sxs-lookup"><span data-stu-id="2c621-108">Example 1: Create a new DriveList for ImportExport job</span></span>
```powershell
PS C:\> New-AzImportExportDriveListObject -DriveId "9CA995BA" -BitLockerKey "238810-662376-448998-450120-652806-203390-606320-483076" -ManifestFile "\\DriveManifest.xml" -ManifestHash "109B21108597EF36D5785F08303F3638"

BitLockerKey                                            BytesSucceeded CopyStatus DriveHeaderHash DriveId  ErrorLogUri ManifestFile        ManifestHash                     ManifestUri PercentComplete State VerboseLogUri  
------------                                            -------------- ---------- --------------- -------  ----------- ------------        ------------                     ----------- --------------- ----- ------- 
238810-662376-448998-450120-652806-203390-606320-483076 0                                         9CA995BA             \\DriveManifest.xml 109B21108597EF36D5785F08303F3638             0
```

<span data-ttu-id="2c621-109">Te polecenia cmdlet tworzą nowe zadanie Lista dysków dla zadania ImportExport.</span><span class="sxs-lookup"><span data-stu-id="2c621-109">These cmdlets create a new DriveList for ImportExport job.</span></span>

## <span data-ttu-id="2c621-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2c621-110">PARAMETERS</span></span>

### <span data-ttu-id="2c621-111">-BitLockerKey</span><span class="sxs-lookup"><span data-stu-id="2c621-111">-BitLockerKey</span></span>
<span data-ttu-id="2c621-112">Klawisz BitLocker używany do szyfrowania dysku.</span><span class="sxs-lookup"><span data-stu-id="2c621-112">The BitLocker key used to encrypt the drive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c621-113">-BytesSucceed</span><span class="sxs-lookup"><span data-stu-id="2c621-113">-BytesSucceeded</span></span>
<span data-ttu-id="2c621-114">Bajty zostały pomyślnie przeniesione dla dysku.</span><span class="sxs-lookup"><span data-stu-id="2c621-114">Bytes successfully transferred for the drive.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c621-115">- CopyStatus</span><span class="sxs-lookup"><span data-stu-id="2c621-115">-CopyStatus</span></span>
<span data-ttu-id="2c621-116">Szczegółowy stan procesu transferu danych.</span><span class="sxs-lookup"><span data-stu-id="2c621-116">Detailed status about the data transfer process.</span></span>
<span data-ttu-id="2c621-117">To pole nie jest zwracane w odpowiedzi, dopóki dysk nie znajduje się w stanie Przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="2c621-117">This field is not returned in the response until the drive is in the Transferring state.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c621-118">-DriveHeaderHash</span><span class="sxs-lookup"><span data-stu-id="2c621-118">-DriveHeaderHash</span></span>
<span data-ttu-id="2c621-119">Wartość skrótu nagłówka dysku.</span><span class="sxs-lookup"><span data-stu-id="2c621-119">The drive header hash value.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c621-120">— DriveId</span><span class="sxs-lookup"><span data-stu-id="2c621-120">-DriveId</span></span>
<span data-ttu-id="2c621-121">Numer seryjny sprzętu dysku bez spacji.</span><span class="sxs-lookup"><span data-stu-id="2c621-121">The drive's hardware serial number, without spaces.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c621-122">-ErrorLogUri</span><span class="sxs-lookup"><span data-stu-id="2c621-122">-ErrorLogUri</span></span>
<span data-ttu-id="2c621-123">A URI that points to the blob containing the error log for the data transfer operation.</span><span class="sxs-lookup"><span data-stu-id="2c621-123">A URI that points to the blob containing the error log for the data transfer operation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c621-124">-ManifestFile</span><span class="sxs-lookup"><span data-stu-id="2c621-124">-ManifestFile</span></span>
<span data-ttu-id="2c621-125">Względna ścieżka pliku manifestu na dysku.</span><span class="sxs-lookup"><span data-stu-id="2c621-125">The relative path of the manifest file on the drive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c621-126">-ManifestHash</span><span class="sxs-lookup"><span data-stu-id="2c621-126">-ManifestHash</span></span>
<span data-ttu-id="2c621-127">Skrót MD5 zakodowany w bazie danych Base16 pliku manifestu na dysku.</span><span class="sxs-lookup"><span data-stu-id="2c621-127">The Base16-encoded MD5 hash of the manifest file on the drive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c621-128">-ManifestUri</span><span class="sxs-lookup"><span data-stu-id="2c621-128">-ManifestUri</span></span>
<span data-ttu-id="2c621-129">A URI that points to the blob containing the drive manifest file.</span><span class="sxs-lookup"><span data-stu-id="2c621-129">A URI that points to the blob containing the drive manifest file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c621-130">-PercentComplete</span><span class="sxs-lookup"><span data-stu-id="2c621-130">-PercentComplete</span></span>
<span data-ttu-id="2c621-131">Procent ukończenia dysku.</span><span class="sxs-lookup"><span data-stu-id="2c621-131">Percentage completed for the drive.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c621-132">— województwo</span><span class="sxs-lookup"><span data-stu-id="2c621-132">-State</span></span>
<span data-ttu-id="2c621-133">Bieżący stan dysku.</span><span class="sxs-lookup"><span data-stu-id="2c621-133">The drive's current state.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Support.DriveState
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c621-134">-VerboseLogUri</span><span class="sxs-lookup"><span data-stu-id="2c621-134">-VerboseLogUri</span></span>
<span data-ttu-id="2c621-135">A URI that points to the blob containing the verbose log for the data transfer operation.</span><span class="sxs-lookup"><span data-stu-id="2c621-135">A URI that points to the blob containing the verbose log for the data transfer operation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c621-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c621-136">CommonParameters</span></span>
<span data-ttu-id="2c621-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c621-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c621-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2c621-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c621-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2c621-139">INPUTS</span></span>

## <span data-ttu-id="2c621-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2c621-140">OUTPUTS</span></span>

### <span data-ttu-id="2c621-141">Microsoft.Azure.PowerShell.cmdlet.ImportExport.Models.Api20161101.IDriveStatus</span><span class="sxs-lookup"><span data-stu-id="2c621-141">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IDriveStatus</span></span>

## <span data-ttu-id="2c621-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2c621-142">NOTES</span></span>

<span data-ttu-id="2c621-143">ALIASY</span><span class="sxs-lookup"><span data-stu-id="2c621-143">ALIASES</span></span>

## <span data-ttu-id="2c621-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2c621-144">RELATED LINKS</span></span>

