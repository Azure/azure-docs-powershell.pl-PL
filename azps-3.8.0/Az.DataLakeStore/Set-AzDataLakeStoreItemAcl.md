---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: FFB335D4-AE3E-4788-B6FD-9AFC36F52B61
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreitemacl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemAcl.md
ms.openlocfilehash: 8b3412acd7513718c8c34e3fc8bb10c5e33f11a8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94054000"
---
# <span data-ttu-id="52e8f-101">Set-AzDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="52e8f-101">Set-AzDataLakeStoreItemAcl</span></span>

## <span data-ttu-id="52e8f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="52e8f-102">SYNOPSIS</span></span>
<span data-ttu-id="52e8f-103">Modyfikuje listę ACL plików lub folderów w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="52e8f-103">Modifies the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="52e8f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="52e8f-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreItemAcl [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52e8f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="52e8f-105">DESCRIPTION</span></span>
<span data-ttu-id="52e8f-106">Polecenie cmdlet **Set-AzDataLakeStoreItemAcl** modyfikuje listę kontroli dostępu (ACL) pliku lub folderu w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="52e8f-106">The **Set-AzDataLakeStoreItemAcl** cmdlet modifies the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="52e8f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="52e8f-107">EXAMPLES</span></span>

### <span data-ttu-id="52e8f-108">Przykład 1. Ustawianie listy ACL dla pliku i folderu</span><span class="sxs-lookup"><span data-stu-id="52e8f-108">Example 1: Set the ACL for a file and a folder</span></span>
```
PS C:\>$ACL = Get-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path /
PS C:\> Set-AzDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/MyFiles/Test.txt" -Acl $ACL
```

<span data-ttu-id="52e8f-109">Pierwsze polecenie pobiera listę ACL katalogu głównego konta usługi ContosoADL, a następnie zapisuje je w zmiennej $ACL.</span><span class="sxs-lookup"><span data-stu-id="52e8f-109">The first command gets the ACL for the root directory of the ContosoADL account, and then stores it in the $ACL variable.</span></span>
<span data-ttu-id="52e8f-110">Drugie polecenie ustawia listę ACL dla pliku Test.txt z tą $ACL.</span><span class="sxs-lookup"><span data-stu-id="52e8f-110">The second command sets the ACL for the file Test.txt to the one in $ACL.</span></span>

### <span data-ttu-id="52e8f-111">Przykład 2: ustawianie listy ACL folderu rekursywnie</span><span class="sxs-lookup"><span data-stu-id="52e8f-111">Example 2: Set the ACL for folder recursively</span></span>
```
PS C:\>$ACL = Get-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path /Folder1
PS C:\> Set-AzDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/Folder2" -Acl $ACL -Recurse -Concurrency 128
```

<span data-ttu-id="52e8f-112">Pierwsze polecenie pobiera listę ACL dla katalogu Folder1 konta ContosoADL, a następnie zapisuje je w zmiennej $ACL.</span><span class="sxs-lookup"><span data-stu-id="52e8f-112">The first command gets the ACL for the directory Folder1 of the ContosoADL account, and then stores it in the $ACL variable.</span></span>
<span data-ttu-id="52e8f-113">Drugie polecenie ustawia listę ACL rekursywnie na Folder2 oraz jej podkatalogi i pliki w $ACL.</span><span class="sxs-lookup"><span data-stu-id="52e8f-113">The second command sets the ACL recursively to Folder2 and its sub directories and files to the one in $ACL.</span></span>

## <span data-ttu-id="52e8f-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="52e8f-114">PARAMETERS</span></span>

### <span data-ttu-id="52e8f-115">— Konto</span><span class="sxs-lookup"><span data-stu-id="52e8f-115">-Account</span></span>
<span data-ttu-id="52e8f-116">Określa nazwę konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="52e8f-116">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="52e8f-117">-ACL</span><span class="sxs-lookup"><span data-stu-id="52e8f-117">-Acl</span></span>
<span data-ttu-id="52e8f-118">Określa listę ACL dla pliku lub folderu.</span><span class="sxs-lookup"><span data-stu-id="52e8f-118">Specifies an ACL for a file or a folder.</span></span>

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

### <span data-ttu-id="52e8f-119">-Concurrency</span><span class="sxs-lookup"><span data-stu-id="52e8f-119">-Concurrency</span></span>
<span data-ttu-id="52e8f-120">Liczba plików/katalogów przetworzonych równolegle.</span><span class="sxs-lookup"><span data-stu-id="52e8f-120">Number of files/directories processed in parallel.</span></span> <span data-ttu-id="52e8f-121">Opcjonalnie: wybrana zostanie rozsądna wartość domyślna.</span><span class="sxs-lookup"><span data-stu-id="52e8f-121">Optional: a reasonable default will be selected.</span></span>

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

### <span data-ttu-id="52e8f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52e8f-122">-DefaultProfile</span></span>
<span data-ttu-id="52e8f-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="52e8f-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52e8f-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="52e8f-124">-PassThru</span></span>
<span data-ttu-id="52e8f-125">Wskazuje, że wynikowa lista ACL powinna być zwracana.</span><span class="sxs-lookup"><span data-stu-id="52e8f-125">Indicates the resulting ACL should be returned.</span></span>

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

### <span data-ttu-id="52e8f-126">-Path</span><span class="sxs-lookup"><span data-stu-id="52e8f-126">-Path</span></span>
<span data-ttu-id="52e8f-127">Określa ścieżkę pliku lub folderu w usłudze Data Lake Store, rozpoczynając od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="52e8f-127">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="52e8f-128">-Rekursywowanie</span><span class="sxs-lookup"><span data-stu-id="52e8f-128">-Recurse</span></span>
<span data-ttu-id="52e8f-129">Wskazuje listę ACL, która ma być ustawiana cyklicznie w podkatalogach podrzędnych i plikach.</span><span class="sxs-lookup"><span data-stu-id="52e8f-129">Indicates the ACL to be set recursively to the child subdirectories and files</span></span>

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

### <span data-ttu-id="52e8f-130">-ShowProgress</span><span class="sxs-lookup"><span data-stu-id="52e8f-130">-ShowProgress</span></span>
<span data-ttu-id="52e8f-131">Jeśli przekazano, stan postępu będzie wyświetlany.</span><span class="sxs-lookup"><span data-stu-id="52e8f-131">If passed then progress status is showed.</span></span> <span data-ttu-id="52e8f-132">Obowiązuje tylko w przypadku ustawienia cyklicznego zestawu ACL.</span><span class="sxs-lookup"><span data-stu-id="52e8f-132">Only applicable when recursive Acl set is done.</span></span>

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

### <span data-ttu-id="52e8f-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="52e8f-133">-Confirm</span></span>
<span data-ttu-id="52e8f-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52e8f-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52e8f-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52e8f-135">-WhatIf</span></span>
<span data-ttu-id="52e8f-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52e8f-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52e8f-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="52e8f-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52e8f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52e8f-138">CommonParameters</span></span>
<span data-ttu-id="52e8f-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52e8f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52e8f-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52e8f-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52e8f-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="52e8f-141">INPUTS</span></span>

### <span data-ttu-id="52e8f-142">System. String</span><span class="sxs-lookup"><span data-stu-id="52e8f-142">System.String</span></span>

### <span data-ttu-id="52e8f-143">Microsoft. Azure. Commands. DataLakeStore. models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="52e8f-143">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="52e8f-144">Microsoft. Azure. Commands. DataLakeStore. models. DataLakeStoreItemAce []</span><span class="sxs-lookup"><span data-stu-id="52e8f-144">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span></span>

### <span data-ttu-id="52e8f-145">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="52e8f-145">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="52e8f-146">System. Int32</span><span class="sxs-lookup"><span data-stu-id="52e8f-146">System.Int32</span></span>

## <span data-ttu-id="52e8f-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="52e8f-147">OUTPUTS</span></span>

### <span data-ttu-id="52e8f-148">Microsoft. Azure. Commands. DataLakeStore. models. DataLakeStoreItemAce</span><span class="sxs-lookup"><span data-stu-id="52e8f-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span></span>

## <span data-ttu-id="52e8f-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="52e8f-149">NOTES</span></span>

## <span data-ttu-id="52e8f-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="52e8f-150">RELATED LINKS</span></span>
