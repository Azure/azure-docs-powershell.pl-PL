---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: FFB335D4-AE3E-4788-B6FD-9AFC36F52B61
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/set-azdatalakestoreitemacl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemAcl.md
ms.openlocfilehash: 16663994a245a7429560ccf2ab855a84acc6ae57
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956186"
---
# <span data-ttu-id="2fb4b-101">Set-AzDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="2fb4b-101">Set-AzDataLakeStoreItemAcl</span></span>

## <span data-ttu-id="2fb4b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2fb4b-102">SYNOPSIS</span></span>
<span data-ttu-id="2fb4b-103">Modyfikuje acl pliku lub folderu w sklepie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2fb4b-103">Modifies the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="2fb4b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2fb4b-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreItemAcl [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2fb4b-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="2fb4b-105">DESCRIPTION</span></span>
<span data-ttu-id="2fb4b-106">Polecenie **cmdlet Set-AzDataLakeStoreItemAcl** modyfikuje listę kontroli dostępu (ACL) pliku lub folderu w magazynie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2fb4b-106">The **Set-AzDataLakeStoreItemAcl** cmdlet modifies the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="2fb4b-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2fb4b-107">EXAMPLES</span></span>

### <span data-ttu-id="2fb4b-108">Przykład 1. Ustawianie listy ACL dla pliku i folderu</span><span class="sxs-lookup"><span data-stu-id="2fb4b-108">Example 1: Set the ACL for a file and a folder</span></span>
```
PS C:\>$ACL = Get-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path /
PS C:\> Set-AzDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/MyFiles/Test.txt" -Acl $ACL
```

<span data-ttu-id="2fb4b-109">Pierwsze polecenie pobiera wartość ACL dla katalogu głównego konta ContosoADL, a następnie zapisuje je w $ACL danych.</span><span class="sxs-lookup"><span data-stu-id="2fb4b-109">The first command gets the ACL for the root directory of the ContosoADL account, and then stores it in the $ACL variable.</span></span>
<span data-ttu-id="2fb4b-110">Drugie polecenie ustawia ACL pliku na Test.txt na to w $ACL.</span><span class="sxs-lookup"><span data-stu-id="2fb4b-110">The second command sets the ACL for the file Test.txt to the one in $ACL.</span></span>

### <span data-ttu-id="2fb4b-111">Przykład 2. Ustawianie listy ACL dla folderu cyklicznie</span><span class="sxs-lookup"><span data-stu-id="2fb4b-111">Example 2: Set the ACL for folder recursively</span></span>
```
PS C:\>$ACL = Get-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path /Folder1
PS C:\> Set-AzDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/Folder2" -Acl $ACL -Recurse -Concurrency 128
```

<span data-ttu-id="2fb4b-112">Pierwsze polecenie pobiera wartość ACL folderu katalogu Folder1 konta ContosoADL, a następnie zapisuje je w $ACL zmienną.</span><span class="sxs-lookup"><span data-stu-id="2fb4b-112">The first command gets the ACL for the directory Folder1 of the ContosoADL account, and then stores it in the $ACL variable.</span></span>
<span data-ttu-id="2fb4b-113">Drugie polecenie ustawia cykliczne ustawienie listy ACL na folder folder2 oraz jego podfoldery i pliki na ten w $ACL.</span><span class="sxs-lookup"><span data-stu-id="2fb4b-113">The second command sets the ACL recursively to Folder2 and its sub directories and files to the one in $ACL.</span></span>

## <span data-ttu-id="2fb4b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2fb4b-114">PARAMETERS</span></span>

### <span data-ttu-id="2fb4b-115">— Konto</span><span class="sxs-lookup"><span data-stu-id="2fb4b-115">-Account</span></span>
<span data-ttu-id="2fb4b-116">Określa nazwę konta sklepu Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2fb4b-116">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fb4b-117">-Acl</span><span class="sxs-lookup"><span data-stu-id="2fb4b-117">-Acl</span></span>
<span data-ttu-id="2fb4b-118">Określa wartość ACL dla pliku lub folderu.</span><span class="sxs-lookup"><span data-stu-id="2fb4b-118">Specifies an ACL for a file or a folder.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2fb4b-119">— współbieżność</span><span class="sxs-lookup"><span data-stu-id="2fb4b-119">-Concurrency</span></span>
<span data-ttu-id="2fb4b-120">Liczba plików/katalogów przetwarzanych równolegle.</span><span class="sxs-lookup"><span data-stu-id="2fb4b-120">Number of files/directories processed in parallel.</span></span> <span data-ttu-id="2fb4b-121">Opcjonalnie: zostanie wybrana rozsądna wartość domyślna.</span><span class="sxs-lookup"><span data-stu-id="2fb4b-121">Optional: a reasonable default will be selected.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fb4b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fb4b-122">-DefaultProfile</span></span>
<span data-ttu-id="2fb4b-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2fb4b-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2fb4b-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2fb4b-124">-PassThru</span></span>
<span data-ttu-id="2fb4b-125">Wskazuje, że należy zwrócić wynikowe listy ACL.</span><span class="sxs-lookup"><span data-stu-id="2fb4b-125">Indicates the resulting ACL should be returned.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fb4b-126">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="2fb4b-126">-Path</span></span>
<span data-ttu-id="2fb4b-127">Określa ścieżkę pliku lub folderu do magazynu Data Lake Store, zaczynając od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="2fb4b-127">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fb4b-128">- Rekurencie</span><span class="sxs-lookup"><span data-stu-id="2fb4b-128">-Recurse</span></span>
<span data-ttu-id="2fb4b-129">Wskazuje wartość listy ACL, która ma być ustawiana rekurencyjnie na podkategorie podrzędny i pliki.</span><span class="sxs-lookup"><span data-stu-id="2fb4b-129">Indicates the ACL to be set recursively to the child subdirectories and files</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fb4b-130">-ShowProgress</span><span class="sxs-lookup"><span data-stu-id="2fb4b-130">-ShowProgress</span></span>
<span data-ttu-id="2fb4b-131">Jeśli pomyślnie przekazano, jest pokazywany stan postępu.</span><span class="sxs-lookup"><span data-stu-id="2fb4b-131">If passed then progress status is showed.</span></span> <span data-ttu-id="2fb4b-132">Ma zastosowanie tylko w przypadku powtarzania się zestawu Acl.</span><span class="sxs-lookup"><span data-stu-id="2fb4b-132">Only applicable when recursive Acl set is done.</span></span>

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

### <span data-ttu-id="2fb4b-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2fb4b-133">-Confirm</span></span>
<span data-ttu-id="2fb4b-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2fb4b-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2fb4b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2fb4b-135">-WhatIf</span></span>
<span data-ttu-id="2fb4b-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2fb4b-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2fb4b-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="2fb4b-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2fb4b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fb4b-138">CommonParameters</span></span>
<span data-ttu-id="2fb4b-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fb4b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fb4b-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fb4b-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fb4b-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2fb4b-141">INPUTS</span></span>

### <span data-ttu-id="2fb4b-142">System.String</span><span class="sxs-lookup"><span data-stu-id="2fb4b-142">System.String</span></span>

### <span data-ttu-id="2fb4b-143">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="2fb4b-143">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="2fb4b-144">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span><span class="sxs-lookup"><span data-stu-id="2fb4b-144">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span></span>

### <span data-ttu-id="2fb4b-145">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="2fb4b-145">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="2fb4b-146">System.Int32</span><span class="sxs-lookup"><span data-stu-id="2fb4b-146">System.Int32</span></span>

## <span data-ttu-id="2fb4b-147">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2fb4b-147">OUTPUTS</span></span>

### <span data-ttu-id="2fb4b-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span><span class="sxs-lookup"><span data-stu-id="2fb4b-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span></span>

## <span data-ttu-id="2fb4b-149">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2fb4b-149">NOTES</span></span>

## <span data-ttu-id="2fb4b-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2fb4b-150">RELATED LINKS</span></span>
