---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/new-AzImportExportDriveListObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExportDriveListObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExportDriveListObject.md
ms.openlocfilehash: 54252b82ecb32d26cf44b3b6f745856b755d60d9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503529"
---
# <span data-ttu-id="80cea-101">New-AzImportExportDriveListObject</span><span class="sxs-lookup"><span data-stu-id="80cea-101">New-AzImportExportDriveListObject</span></span>

## <span data-ttu-id="80cea-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="80cea-102">SYNOPSIS</span></span>
<span data-ttu-id="80cea-103">Utwórz obiekt DriverList dla ImportExport.</span><span class="sxs-lookup"><span data-stu-id="80cea-103">Create a DriverList Object for ImportExport.</span></span>

## <span data-ttu-id="80cea-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="80cea-104">SYNTAX</span></span>

```
New-AzImportExportDriveListObject [-BitLockerKey <String>] [-BytesSucceeded <Int64>] [-CopyStatus <String>]
 [-DriveHeaderHash <String>] [-DriveId <String>] [-ErrorLogUri <String>] [-ManifestFile <String>]
 [-ManifestHash <String>] [-ManifestUri <String>] [-PercentComplete <Int32>] [-State <DriveState>]
 [-VerboseLogUri <String>] [<CommonParameters>]
```

## <span data-ttu-id="80cea-105">Opis</span><span class="sxs-lookup"><span data-stu-id="80cea-105">DESCRIPTION</span></span>
<span data-ttu-id="80cea-106">Utwórz obiekt DriverList dla ImportExport.</span><span class="sxs-lookup"><span data-stu-id="80cea-106">Create a DriverList Object for ImportExport.</span></span>

## <span data-ttu-id="80cea-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="80cea-107">EXAMPLES</span></span>

### <span data-ttu-id="80cea-108">Przykład 1. Tworzenie nowego DriveList dla zadania ImportExport</span><span class="sxs-lookup"><span data-stu-id="80cea-108">Example 1: Create a new DriveList for ImportExport job</span></span>
```powershell
PS C:\> New-AzImportExportDriveListObject -DriveId "9CA995BA" -BitLockerKey "238810-662376-448998-450120-652806-203390-606320-483076" -ManifestFile "\\DriveManifest.xml" -ManifestHash "109B21108597EF36D5785F08303F3638"

BitLockerKey                                            BytesSucceeded CopyStatus DriveHeaderHash DriveId  ErrorLogUri ManifestFile        ManifestHash                     ManifestUri PercentComplete State VerboseLogUri  
------------                                            -------------- ---------- --------------- -------  ----------- ------------        ------------                     ----------- --------------- ----- ------- 
238810-662376-448998-450120-652806-203390-606320-483076 0                                         9CA995BA             \\DriveManifest.xml 109B21108597EF36D5785F08303F3638             0
```

<span data-ttu-id="80cea-109">Te polecenia cmdlet tworzą nowe DriveList dla ImportExport.</span><span class="sxs-lookup"><span data-stu-id="80cea-109">These cmdlets create a new DriveList for ImportExport job.</span></span>

## <span data-ttu-id="80cea-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="80cea-110">PARAMETERS</span></span>

### <span data-ttu-id="80cea-111">-BitLockerKey</span><span class="sxs-lookup"><span data-stu-id="80cea-111">-BitLockerKey</span></span>
<span data-ttu-id="80cea-112">Klucz funkcji BitLocker służący do szyfrowania dysku.</span><span class="sxs-lookup"><span data-stu-id="80cea-112">The BitLocker key used to encrypt the drive.</span></span>

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

### <span data-ttu-id="80cea-113">-BytesSucceeded</span><span class="sxs-lookup"><span data-stu-id="80cea-113">-BytesSucceeded</span></span>
<span data-ttu-id="80cea-114">Pomyślnie przeniesiono bajty dla dysku.</span><span class="sxs-lookup"><span data-stu-id="80cea-114">Bytes successfully transferred for the drive.</span></span>

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

### <span data-ttu-id="80cea-115">-CopyStatus</span><span class="sxs-lookup"><span data-stu-id="80cea-115">-CopyStatus</span></span>
<span data-ttu-id="80cea-116">Szczegółowy stan procesu transferu danych.</span><span class="sxs-lookup"><span data-stu-id="80cea-116">Detailed status about the data transfer process.</span></span>
<span data-ttu-id="80cea-117">To pole nie jest zwracane w odpowiedzi, dopóki dysk nie będzie w stanie przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="80cea-117">This field is not returned in the response until the drive is in the Transferring state.</span></span>

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

### <span data-ttu-id="80cea-118">-DriveHeaderHash</span><span class="sxs-lookup"><span data-stu-id="80cea-118">-DriveHeaderHash</span></span>
<span data-ttu-id="80cea-119">Wartość skrótu nagłówka dysku.</span><span class="sxs-lookup"><span data-stu-id="80cea-119">The drive header hash value.</span></span>

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

### <span data-ttu-id="80cea-120">-DriveId</span><span class="sxs-lookup"><span data-stu-id="80cea-120">-DriveId</span></span>
<span data-ttu-id="80cea-121">Numer seryjny sprzętu dysku bez spacji.</span><span class="sxs-lookup"><span data-stu-id="80cea-121">The drive's hardware serial number, without spaces.</span></span>

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

### <span data-ttu-id="80cea-122">-ErrorLogUri</span><span class="sxs-lookup"><span data-stu-id="80cea-122">-ErrorLogUri</span></span>
<span data-ttu-id="80cea-123">Identyfikator URI wskazujący obiekt BLOB zawierający dziennik błędów operacji transferu danych.</span><span class="sxs-lookup"><span data-stu-id="80cea-123">A URI that points to the blob containing the error log for the data transfer operation.</span></span>

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

### <span data-ttu-id="80cea-124">-ManifestFile</span><span class="sxs-lookup"><span data-stu-id="80cea-124">-ManifestFile</span></span>
<span data-ttu-id="80cea-125">Względna ścieżka pliku manifestu na dysku.</span><span class="sxs-lookup"><span data-stu-id="80cea-125">The relative path of the manifest file on the drive.</span></span>

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

### <span data-ttu-id="80cea-126">-ManifestHash</span><span class="sxs-lookup"><span data-stu-id="80cea-126">-ManifestHash</span></span>
<span data-ttu-id="80cea-127">Zakodowana na Base16 skrót MD5 pliku manifestu na dysku.</span><span class="sxs-lookup"><span data-stu-id="80cea-127">The Base16-encoded MD5 hash of the manifest file on the drive.</span></span>

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

### <span data-ttu-id="80cea-128">-ManifestUri</span><span class="sxs-lookup"><span data-stu-id="80cea-128">-ManifestUri</span></span>
<span data-ttu-id="80cea-129">Identyfikator URI wskazujący obiekt BLOB zawierający plik manifestu dysku.</span><span class="sxs-lookup"><span data-stu-id="80cea-129">A URI that points to the blob containing the drive manifest file.</span></span>

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

### <span data-ttu-id="80cea-130">-PercentComplete</span><span class="sxs-lookup"><span data-stu-id="80cea-130">-PercentComplete</span></span>
<span data-ttu-id="80cea-131">Procent ukończenia dla dysku.</span><span class="sxs-lookup"><span data-stu-id="80cea-131">Percentage completed for the drive.</span></span>

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

### <span data-ttu-id="80cea-132">-State</span><span class="sxs-lookup"><span data-stu-id="80cea-132">-State</span></span>
<span data-ttu-id="80cea-133">Obecny stan stacji.</span><span class="sxs-lookup"><span data-stu-id="80cea-133">The drive's current state.</span></span>

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

### <span data-ttu-id="80cea-134">-VerboseLogUri</span><span class="sxs-lookup"><span data-stu-id="80cea-134">-VerboseLogUri</span></span>
<span data-ttu-id="80cea-135">Identyfikator URI wskazujący obiekt BLOB zawierający pełny dziennik w operacji przesyłania danych.</span><span class="sxs-lookup"><span data-stu-id="80cea-135">A URI that points to the blob containing the verbose log for the data transfer operation.</span></span>

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

### <span data-ttu-id="80cea-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80cea-136">CommonParameters</span></span>
<span data-ttu-id="80cea-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80cea-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80cea-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="80cea-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80cea-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="80cea-139">INPUTS</span></span>

## <span data-ttu-id="80cea-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="80cea-140">OUTPUTS</span></span>

### <span data-ttu-id="80cea-141">Microsoft. Azure. PowerShell. polecenia. ImportExport. models. Api20161101. IDriveStatus</span><span class="sxs-lookup"><span data-stu-id="80cea-141">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IDriveStatus</span></span>

## <span data-ttu-id="80cea-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="80cea-142">NOTES</span></span>

<span data-ttu-id="80cea-143">PISUJE</span><span class="sxs-lookup"><span data-stu-id="80cea-143">ALIASES</span></span>

## <span data-ttu-id="80cea-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="80cea-144">RELATED LINKS</span></span>

