---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/new-AzImportExportDriveListObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExportDriveListObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExportDriveListObject.md
ms.openlocfilehash: 54252b82ecb32d26cf44b3b6f745856b755d60d9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364492"
---
# <span data-ttu-id="a094f-101">New-AzImportExportDriveListObject</span><span class="sxs-lookup"><span data-stu-id="a094f-101">New-AzImportExportDriveListObject</span></span>

## <span data-ttu-id="a094f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a094f-102">SYNOPSIS</span></span>
<span data-ttu-id="a094f-103">Utwórz obiekt DriverList dla ImportExport.</span><span class="sxs-lookup"><span data-stu-id="a094f-103">Create a DriverList Object for ImportExport.</span></span>

## <span data-ttu-id="a094f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a094f-104">SYNTAX</span></span>

```
New-AzImportExportDriveListObject [-BitLockerKey <String>] [-BytesSucceeded <Int64>] [-CopyStatus <String>]
 [-DriveHeaderHash <String>] [-DriveId <String>] [-ErrorLogUri <String>] [-ManifestFile <String>]
 [-ManifestHash <String>] [-ManifestUri <String>] [-PercentComplete <Int32>] [-State <DriveState>]
 [-VerboseLogUri <String>] [<CommonParameters>]
```

## <span data-ttu-id="a094f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a094f-105">DESCRIPTION</span></span>
<span data-ttu-id="a094f-106">Utwórz obiekt DriverList dla ImportExport.</span><span class="sxs-lookup"><span data-stu-id="a094f-106">Create a DriverList Object for ImportExport.</span></span>

## <span data-ttu-id="a094f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a094f-107">EXAMPLES</span></span>

### <span data-ttu-id="a094f-108">Przykład 1. Tworzenie nowego DriveList dla zadania ImportExport</span><span class="sxs-lookup"><span data-stu-id="a094f-108">Example 1: Create a new DriveList for ImportExport job</span></span>
```powershell
PS C:\> New-AzImportExportDriveListObject -DriveId "9CA995BA" -BitLockerKey "238810-662376-448998-450120-652806-203390-606320-483076" -ManifestFile "\\DriveManifest.xml" -ManifestHash "109B21108597EF36D5785F08303F3638"

BitLockerKey                                            BytesSucceeded CopyStatus DriveHeaderHash DriveId  ErrorLogUri ManifestFile        ManifestHash                     ManifestUri PercentComplete State VerboseLogUri  
------------                                            -------------- ---------- --------------- -------  ----------- ------------        ------------                     ----------- --------------- ----- ------- 
238810-662376-448998-450120-652806-203390-606320-483076 0                                         9CA995BA             \\DriveManifest.xml 109B21108597EF36D5785F08303F3638             0
```

<span data-ttu-id="a094f-109">Te polecenia cmdlet tworzą nowe DriveList dla ImportExport.</span><span class="sxs-lookup"><span data-stu-id="a094f-109">These cmdlets create a new DriveList for ImportExport job.</span></span>

## <span data-ttu-id="a094f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a094f-110">PARAMETERS</span></span>

### <span data-ttu-id="a094f-111">-BitLockerKey</span><span class="sxs-lookup"><span data-stu-id="a094f-111">-BitLockerKey</span></span>
<span data-ttu-id="a094f-112">Klucz funkcji BitLocker służący do szyfrowania dysku.</span><span class="sxs-lookup"><span data-stu-id="a094f-112">The BitLocker key used to encrypt the drive.</span></span>

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

### <span data-ttu-id="a094f-113">-BytesSucceeded</span><span class="sxs-lookup"><span data-stu-id="a094f-113">-BytesSucceeded</span></span>
<span data-ttu-id="a094f-114">Pomyślnie przeniesiono bajty dla dysku.</span><span class="sxs-lookup"><span data-stu-id="a094f-114">Bytes successfully transferred for the drive.</span></span>

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

### <span data-ttu-id="a094f-115">-CopyStatus</span><span class="sxs-lookup"><span data-stu-id="a094f-115">-CopyStatus</span></span>
<span data-ttu-id="a094f-116">Szczegółowy stan procesu transferu danych.</span><span class="sxs-lookup"><span data-stu-id="a094f-116">Detailed status about the data transfer process.</span></span>
<span data-ttu-id="a094f-117">To pole nie jest zwracane w odpowiedzi, dopóki dysk nie będzie w stanie przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="a094f-117">This field is not returned in the response until the drive is in the Transferring state.</span></span>

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

### <span data-ttu-id="a094f-118">-DriveHeaderHash</span><span class="sxs-lookup"><span data-stu-id="a094f-118">-DriveHeaderHash</span></span>
<span data-ttu-id="a094f-119">Wartość skrótu nagłówka dysku.</span><span class="sxs-lookup"><span data-stu-id="a094f-119">The drive header hash value.</span></span>

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

### <span data-ttu-id="a094f-120">-DriveId</span><span class="sxs-lookup"><span data-stu-id="a094f-120">-DriveId</span></span>
<span data-ttu-id="a094f-121">Numer seryjny sprzętu dysku bez spacji.</span><span class="sxs-lookup"><span data-stu-id="a094f-121">The drive's hardware serial number, without spaces.</span></span>

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

### <span data-ttu-id="a094f-122">-ErrorLogUri</span><span class="sxs-lookup"><span data-stu-id="a094f-122">-ErrorLogUri</span></span>
<span data-ttu-id="a094f-123">Identyfikator URI wskazujący obiekt BLOB zawierający dziennik błędów operacji transferu danych.</span><span class="sxs-lookup"><span data-stu-id="a094f-123">A URI that points to the blob containing the error log for the data transfer operation.</span></span>

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

### <span data-ttu-id="a094f-124">-ManifestFile</span><span class="sxs-lookup"><span data-stu-id="a094f-124">-ManifestFile</span></span>
<span data-ttu-id="a094f-125">Względna ścieżka pliku manifestu na dysku.</span><span class="sxs-lookup"><span data-stu-id="a094f-125">The relative path of the manifest file on the drive.</span></span>

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

### <span data-ttu-id="a094f-126">-ManifestHash</span><span class="sxs-lookup"><span data-stu-id="a094f-126">-ManifestHash</span></span>
<span data-ttu-id="a094f-127">Zakodowana na Base16 skrót MD5 pliku manifestu na dysku.</span><span class="sxs-lookup"><span data-stu-id="a094f-127">The Base16-encoded MD5 hash of the manifest file on the drive.</span></span>

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

### <span data-ttu-id="a094f-128">-ManifestUri</span><span class="sxs-lookup"><span data-stu-id="a094f-128">-ManifestUri</span></span>
<span data-ttu-id="a094f-129">Identyfikator URI wskazujący obiekt BLOB zawierający plik manifestu dysku.</span><span class="sxs-lookup"><span data-stu-id="a094f-129">A URI that points to the blob containing the drive manifest file.</span></span>

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

### <span data-ttu-id="a094f-130">-PercentComplete</span><span class="sxs-lookup"><span data-stu-id="a094f-130">-PercentComplete</span></span>
<span data-ttu-id="a094f-131">Procent ukończenia dla dysku.</span><span class="sxs-lookup"><span data-stu-id="a094f-131">Percentage completed for the drive.</span></span>

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

### <span data-ttu-id="a094f-132">-State</span><span class="sxs-lookup"><span data-stu-id="a094f-132">-State</span></span>
<span data-ttu-id="a094f-133">Obecny stan stacji.</span><span class="sxs-lookup"><span data-stu-id="a094f-133">The drive's current state.</span></span>

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

### <span data-ttu-id="a094f-134">-VerboseLogUri</span><span class="sxs-lookup"><span data-stu-id="a094f-134">-VerboseLogUri</span></span>
<span data-ttu-id="a094f-135">Identyfikator URI wskazujący obiekt BLOB zawierający pełny dziennik w operacji przesyłania danych.</span><span class="sxs-lookup"><span data-stu-id="a094f-135">A URI that points to the blob containing the verbose log for the data transfer operation.</span></span>

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

### <span data-ttu-id="a094f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a094f-136">CommonParameters</span></span>
<span data-ttu-id="a094f-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a094f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a094f-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a094f-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a094f-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a094f-139">INPUTS</span></span>

## <span data-ttu-id="a094f-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a094f-140">OUTPUTS</span></span>

### <span data-ttu-id="a094f-141">Microsoft. Azure. PowerShell. polecenia. ImportExport. models. Api20161101. IDriveStatus</span><span class="sxs-lookup"><span data-stu-id="a094f-141">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IDriveStatus</span></span>

## <span data-ttu-id="a094f-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a094f-142">NOTES</span></span>

<span data-ttu-id="a094f-143">PISUJE</span><span class="sxs-lookup"><span data-stu-id="a094f-143">ALIASES</span></span>

## <span data-ttu-id="a094f-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a094f-144">RELATED LINKS</span></span>

