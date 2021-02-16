---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 33E7607E-C2BC-4F46-9038-91AC92041F00
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItemAclEntry.md
ms.openlocfilehash: b6d07dbf390a0835bd28a045e4eea8bcf29e15f9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243882"
---
# <span data-ttu-id="944b6-101">Remove-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="944b6-101">Remove-AzDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="944b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="944b6-102">SYNOPSIS</span></span>
<span data-ttu-id="944b6-103">Usuwa wpis z listy ACL pliku lub folderu w magazynie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="944b6-103">Removes an entry from the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="944b6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="944b6-104">SYNTAX</span></span>

### <span data-ttu-id="944b6-105">RemoveByACLObject (domyślne)</span><span class="sxs-lookup"><span data-stu-id="944b6-105">RemoveByACLObject (Default)</span></span>
```
Remove-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="944b6-106">RemoveSpecificACE</span><span class="sxs-lookup"><span data-stu-id="944b6-106">RemoveSpecificACE</span></span>
```
Remove-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance> [-AceType] <AceType>
 [[-Id] <Guid>] [-Default] [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="944b6-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="944b6-107">DESCRIPTION</span></span>
<span data-ttu-id="944b6-108">Polecenie cmdlet **Remove-AzDataLakeStoreItemAclEntry** usuwa wpis (ACE) z listy kontroli dostępu (ACL) pliku lub folderu w magazynie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="944b6-108">The **Remove-AzDataLakeStoreItemAclEntry** cmdlet removes an entry (ACE) from the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="944b6-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="944b6-109">EXAMPLES</span></span>

### <span data-ttu-id="944b6-110">Przykład 1. Usuwanie wpisu użytkownika</span><span class="sxs-lookup"><span data-stu-id="944b6-110">Example 1: Remove a user entry</span></span>
```
PS C:\>Remove-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId
```

<span data-ttu-id="944b6-111">To polecenie usuwa wpis ACE użytkownika Patti Fuller z konta ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="944b6-111">This command removes the user ACE for Patti Fuller from the ContosoADL account.</span></span>

### <span data-ttu-id="944b6-112">Przykład 2. Ponowne usuwanie wpisu użytkownika</span><span class="sxs-lookup"><span data-stu-id="944b6-112">Example 2: Remove a user entry recursively</span></span>
```
PS C:\>Remove-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId -Recurse -Concurrency 128
```

### <span data-ttu-id="944b6-113">Przykład 3. Usuwanie uprawnień do obiektu ACE rekurencyjnie przy użyciu obiektu Acl</span><span class="sxs-lookup"><span data-stu-id="944b6-113">Example 3: Remove permissions for an ACE recursively using Acl object</span></span>
```
PS C:\>$fullAcl="user:userid1,default:user:userid1
PS C:\>$newFullAcl = $fullAcl.Split("{,}")
PS C:\>Remove-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -Acl $newFullAcl -Recurse -Concurrency 128
```

<span data-ttu-id="944b6-114">To polecenie usuwa wpis ACE użytkownika Patti Fuller z katalogu głównego i rekurencyjnie ze wszystkich jego pod katalogów i plików konta ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="944b6-114">This command removes the user ACE for Patti Fuller from the root and recursively from all it's subdirectories and files for account ContosoADL.</span></span>

## <span data-ttu-id="944b6-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="944b6-115">PARAMETERS</span></span>

### <span data-ttu-id="944b6-116">— Konto</span><span class="sxs-lookup"><span data-stu-id="944b6-116">-Account</span></span>
<span data-ttu-id="944b6-117">Określa nazwę konta w sklepie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="944b6-117">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="944b6-118">-AceType</span><span class="sxs-lookup"><span data-stu-id="944b6-118">-AceType</span></span>
<span data-ttu-id="944b6-119">Określa typ danych ACE do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="944b6-119">Specifies the type of ACE to remove.</span></span>
<span data-ttu-id="944b6-120">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="944b6-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="944b6-121">Użytkownik</span><span class="sxs-lookup"><span data-stu-id="944b6-121">User</span></span>
- <span data-ttu-id="944b6-122">Grupowanie</span><span class="sxs-lookup"><span data-stu-id="944b6-122">Group</span></span>
- <span data-ttu-id="944b6-123">Maskowanie</span><span class="sxs-lookup"><span data-stu-id="944b6-123">Mask</span></span>
- <span data-ttu-id="944b6-124">Inne</span><span class="sxs-lookup"><span data-stu-id="944b6-124">Other</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType
Parameter Sets: RemoveSpecificACE
Aliases:
Accepted values: User, Group, Mask, Other

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="944b6-125">—Acl</span><span class="sxs-lookup"><span data-stu-id="944b6-125">-Acl</span></span>
<span data-ttu-id="944b6-126">Określa obiekt ACL zawierający wpisy do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="944b6-126">Specifies the ACL object that contains the entries to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]
Parameter Sets: RemoveByACLObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="944b6-127">— współbieżność</span><span class="sxs-lookup"><span data-stu-id="944b6-127">-Concurrency</span></span>
<span data-ttu-id="944b6-128">Liczba plików/katalogów przetwarzanych równolegle.</span><span class="sxs-lookup"><span data-stu-id="944b6-128">Number of files/directories processed in parallel.</span></span> <span data-ttu-id="944b6-129">Opcjonalnie: zostanie wybrana rozsądna wartość domyślna</span><span class="sxs-lookup"><span data-stu-id="944b6-129">Optional: a reasonable default will be selected</span></span>

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

### <span data-ttu-id="944b6-130">— Domyślne</span><span class="sxs-lookup"><span data-stu-id="944b6-130">-Default</span></span>
<span data-ttu-id="944b6-131">Wskazuje, że ta operacja usuwa domyślny wpis ace z określonej listy ACL.</span><span class="sxs-lookup"><span data-stu-id="944b6-131">Indicates that this operation removes the default ACE from the specified ACL.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RemoveSpecificACE
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="944b6-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="944b6-132">-DefaultProfile</span></span>
<span data-ttu-id="944b6-133">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="944b6-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="944b6-134">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="944b6-134">-Id</span></span>
<span data-ttu-id="944b6-135">Określa identyfikator obiektu użytkownika, grupy lub podmiotu zabezpieczeń usługi AzureActive Directory, dla którego ma być usuwany wpis ACE.</span><span class="sxs-lookup"><span data-stu-id="944b6-135">Specifies the object ID of the AzureActive Directory user, group, or service principal for which to remove an ACE.</span></span>

```yaml
Type: System.Guid
Parameter Sets: RemoveSpecificACE
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="944b6-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="944b6-136">-PassThru</span></span>
<span data-ttu-id="944b6-137">Wskazuje, że powinna zostać zwrócona odpowiedź logiczna wskazująca wynik operacji usuwania.</span><span class="sxs-lookup"><span data-stu-id="944b6-137">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="944b6-138">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="944b6-138">-Path</span></span>
<span data-ttu-id="944b6-139">Określa ścieżkę magazynu Data Lake Store elementu, z którego ma być usuwany wpis ACE, zaczynając od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="944b6-139">Specifies the Data Lake Store path of the item from which to remove an ACE, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="944b6-140">- Rekurencie</span><span class="sxs-lookup"><span data-stu-id="944b6-140">-Recurse</span></span>
<span data-ttu-id="944b6-141">Wskazuje, że listy ACL mają być usuwane rekurencyjnie do podkategorów i plików podrzędnego.</span><span class="sxs-lookup"><span data-stu-id="944b6-141">Indicates the ACL to be removed recursively to the child subdirectories and files</span></span>

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

### <span data-ttu-id="944b6-142">-ShowProgress</span><span class="sxs-lookup"><span data-stu-id="944b6-142">-ShowProgress</span></span>
<span data-ttu-id="944b6-143">Jeśli pomyślnie przekazano, jest pokazywany stan postępu.</span><span class="sxs-lookup"><span data-stu-id="944b6-143">If passed then progress status is showed.</span></span> <span data-ttu-id="944b6-144">Ma zastosowanie tylko w przypadku usuwania listy cyklicznej.</span><span class="sxs-lookup"><span data-stu-id="944b6-144">Only applicable when recursive Acl remove is done.</span></span>

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

### <span data-ttu-id="944b6-145">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="944b6-145">-Confirm</span></span>
<span data-ttu-id="944b6-146">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="944b6-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="944b6-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="944b6-147">-WhatIf</span></span>
<span data-ttu-id="944b6-148">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="944b6-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="944b6-149">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="944b6-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="944b6-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="944b6-150">CommonParameters</span></span>
<span data-ttu-id="944b6-151">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="944b6-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="944b6-152">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="944b6-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="944b6-153">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="944b6-153">INPUTS</span></span>

### <span data-ttu-id="944b6-154">System.String</span><span class="sxs-lookup"><span data-stu-id="944b6-154">System.String</span></span>

### <span data-ttu-id="944b6-155">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="944b6-155">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="944b6-156">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span><span class="sxs-lookup"><span data-stu-id="944b6-156">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span></span>

### <span data-ttu-id="944b6-157">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType</span><span class="sxs-lookup"><span data-stu-id="944b6-157">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType</span></span>

### <span data-ttu-id="944b6-158">System.Guid</span><span class="sxs-lookup"><span data-stu-id="944b6-158">System.Guid</span></span>

### <span data-ttu-id="944b6-159">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="944b6-159">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="944b6-160">System.Int32</span><span class="sxs-lookup"><span data-stu-id="944b6-160">System.Int32</span></span>

## <span data-ttu-id="944b6-161">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="944b6-161">OUTPUTS</span></span>

### <span data-ttu-id="944b6-162">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="944b6-162">System.Boolean</span></span>

## <span data-ttu-id="944b6-163">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="944b6-163">NOTES</span></span>

## <span data-ttu-id="944b6-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="944b6-164">RELATED LINKS</span></span>

[<span data-ttu-id="944b6-165">Set-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="944b6-165">Set-AzDataLakeStoreItemAclEntry</span></span>](./Set-AzDataLakeStoreItemAclEntry.md)


