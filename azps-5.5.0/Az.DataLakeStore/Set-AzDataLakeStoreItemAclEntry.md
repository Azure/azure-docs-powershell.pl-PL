---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 0671D833-8B3A-4480-A576-92F1A9E8CE92
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 4f432596e6165989df07187a9383da04f0929a2d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194634"
---
# <span data-ttu-id="93595-101">Set-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="93595-101">Set-AzDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="93595-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93595-102">SYNOPSIS</span></span>
<span data-ttu-id="93595-103">Modyfikuje wpis w liście ACL pliku lub folderu w magazynie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="93595-103">Modifies an entry in the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="93595-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="93595-104">SYNTAX</span></span>

### <span data-ttu-id="93595-105">SetByACLObject (domyślne)</span><span class="sxs-lookup"><span data-stu-id="93595-105">SetByACLObject (Default)</span></span>
```
Set-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93595-106">SetSpecificACE</span><span class="sxs-lookup"><span data-stu-id="93595-106">SetSpecificACE</span></span>
```
Set-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance> [-AceType] <AceType>
 [[-Id] <Guid>] [-Permissions] <Permission> [-Default] [-PassThru] [-Recurse] [-Concurrency <Int32>]
 [-ShowProgress] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93595-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="93595-107">DESCRIPTION</span></span>
<span data-ttu-id="93595-108">Polecenie cmdlet **Set-AzDataLakeStoreItemAclEntry** modyfikuje wpis (ACE) na liście kontroli dostępu pliku lub folderu w magazynie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="93595-108">The **Set-AzDataLakeStoreItemAclEntry** cmdlet modifies an entry (ACE) in the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="93595-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="93595-109">EXAMPLES</span></span>

### <span data-ttu-id="93595-110">Przykład 1. Modyfikowanie uprawnień do wpisów ACE</span><span class="sxs-lookup"><span data-stu-id="93595-110">Example 1: Modify permissions for an ACE</span></span>
```
PS C:\>Set-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId -Permissions All
```

<span data-ttu-id="93595-111">To polecenie modyfikuje wpis ACE dla PattiEgo Fullera, tak aby miał wszystkie uprawnienia.</span><span class="sxs-lookup"><span data-stu-id="93595-111">This command modifies the ACE for Patti Fuller to have all permissions.</span></span>

### <span data-ttu-id="93595-112">Przykład 2. Rekurencyjnie modyfikowanie uprawnień do ace</span><span class="sxs-lookup"><span data-stu-id="93595-112">Example 2: Modify permissions for an ACE recursively</span></span>
```
PS C:\>Set-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId -Permissions All -Recurse -Concurrency 128
```

### <span data-ttu-id="93595-113">Przykład 3. Modyfikowanie uprawnień do obiektu ACE rekurencyjnie przy użyciu obiektu Acl</span><span class="sxs-lookup"><span data-stu-id="93595-113">Example 3: Modify permissions for an ACE recursively using Acl object</span></span>
```
PS C:\>$fullAcl="user:userid1:--x,default:user:userid1:--x"
PS C:\>$newFullAcl = $fullAcl.Split("{,}")
PS C:\>Set-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -Acl $newFullAcl -Recurse -Concurrency 128
```

<span data-ttu-id="93595-114">To polecenie cyklicznie modyfikuje ace for Patti Fuller, aby mieć wszystkie uprawnienia do katalogu głównego oraz wszystkich jego podkategorii i plików.</span><span class="sxs-lookup"><span data-stu-id="93595-114">This command recursively modifies the ACE for Patti Fuller to have all permissions to root and all its subdirectories and files.</span></span>

## <span data-ttu-id="93595-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="93595-115">PARAMETERS</span></span>

### <span data-ttu-id="93595-116">— Konto</span><span class="sxs-lookup"><span data-stu-id="93595-116">-Account</span></span>
<span data-ttu-id="93595-117">Określa nazwę konta sklepu Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="93595-117">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="93595-118">-AceType</span><span class="sxs-lookup"><span data-stu-id="93595-118">-AceType</span></span>
<span data-ttu-id="93595-119">Określa typ danych ACE do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="93595-119">Specifies the type of ACE to modify.</span></span>
<span data-ttu-id="93595-120">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="93595-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="93595-121">Użytkownik</span><span class="sxs-lookup"><span data-stu-id="93595-121">User</span></span> 
- <span data-ttu-id="93595-122">Grupowanie</span><span class="sxs-lookup"><span data-stu-id="93595-122">Group</span></span> 
- <span data-ttu-id="93595-123">Maskowanie</span><span class="sxs-lookup"><span data-stu-id="93595-123">Mask</span></span> 
- <span data-ttu-id="93595-124">Inne</span><span class="sxs-lookup"><span data-stu-id="93595-124">Other</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType
Parameter Sets: SetSpecificACE
Aliases:
Accepted values: User, Group, Mask, Other

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93595-125">-Acl</span><span class="sxs-lookup"><span data-stu-id="93595-125">-Acl</span></span>
<span data-ttu-id="93595-126">Określa obiekt ACL zawierający wpisy do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="93595-126">Specifies the ACL object that contains the entries to modify.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]
Parameter Sets: SetByACLObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="93595-127">— współbieżność</span><span class="sxs-lookup"><span data-stu-id="93595-127">-Concurrency</span></span>
<span data-ttu-id="93595-128">Liczba plików/katalogów przetwarzanych równolegle.</span><span class="sxs-lookup"><span data-stu-id="93595-128">Number of files/directories processed in parallel.</span></span> <span data-ttu-id="93595-129">Opcjonalnie: zostanie wybrana rozsądna wartość domyślna</span><span class="sxs-lookup"><span data-stu-id="93595-129">Optional: a reasonable default will be selected</span></span>

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

### <span data-ttu-id="93595-130">— Domyślne</span><span class="sxs-lookup"><span data-stu-id="93595-130">-Default</span></span>
<span data-ttu-id="93595-131">Wskazuje, że ta operacja zmodyfikuje domyślną wartość ace z określonej listy ACL.</span><span class="sxs-lookup"><span data-stu-id="93595-131">Indicates that this operation modifies the default ACE from the specified ACL.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetSpecificACE
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93595-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93595-132">-DefaultProfile</span></span>
<span data-ttu-id="93595-133">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="93595-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93595-134">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="93595-134">-Id</span></span>
<span data-ttu-id="93595-135">Określa identyfikator obiektu użytkownika, grupy lub podmiotu zabezpieczeń usługi AzureActive Directory, dla którego ma być modyfikowany wpis ACE.</span><span class="sxs-lookup"><span data-stu-id="93595-135">Specifies the object ID of the AzureActive Directory user, group, or service principal for which to modify an ACE.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SetSpecificACE
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93595-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="93595-136">-PassThru</span></span>
<span data-ttu-id="93595-137">Wskazuje, że wynikowa acl powinna zostać zwrócona.</span><span class="sxs-lookup"><span data-stu-id="93595-137">Indicates the resulting ACL should be returned.</span></span>

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

### <span data-ttu-id="93595-138">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="93595-138">-Path</span></span>
<span data-ttu-id="93595-139">Określa ścieżkę magazynu usługi Data Lake Store elementu, dla którego ma być modyfikowany wpis ACE, zaczynając od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="93595-139">Specifies the Data Lake Store path of the item for which to modify an ACE, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="93595-140">— Uprawnienia</span><span class="sxs-lookup"><span data-stu-id="93595-140">-Permissions</span></span>
<span data-ttu-id="93595-141">Określa uprawnienia do ace-ace.</span><span class="sxs-lookup"><span data-stu-id="93595-141">Specifies the permissions for the ACE.</span></span>
<span data-ttu-id="93595-142">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="93595-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="93595-143">Brak</span><span class="sxs-lookup"><span data-stu-id="93595-143">None</span></span>
- <span data-ttu-id="93595-144">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="93595-144">Execute</span></span>
- <span data-ttu-id="93595-145">Pisanie</span><span class="sxs-lookup"><span data-stu-id="93595-145">Write</span></span>
- <span data-ttu-id="93595-146">WriteExecute</span><span class="sxs-lookup"><span data-stu-id="93595-146">WriteExecute</span></span>
- <span data-ttu-id="93595-147">Czytanie</span><span class="sxs-lookup"><span data-stu-id="93595-147">Read</span></span>
- <span data-ttu-id="93595-148">ReadExecute</span><span class="sxs-lookup"><span data-stu-id="93595-148">ReadExecute</span></span>
- <span data-ttu-id="93595-149">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="93595-149">ReadWrite</span></span>
- <span data-ttu-id="93595-150">Wszystko</span><span class="sxs-lookup"><span data-stu-id="93595-150">All</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Permission
Parameter Sets: SetSpecificACE
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93595-151">- Rekurencie</span><span class="sxs-lookup"><span data-stu-id="93595-151">-Recurse</span></span>
<span data-ttu-id="93595-152">Wskazuje, że ACL ma być modyfikowane rekurencyjnie do podkategorów i plików podrzędnego.</span><span class="sxs-lookup"><span data-stu-id="93595-152">Indicates the ACL to be modified recursively to the child subdirectories and files</span></span>

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

### <span data-ttu-id="93595-153">-ShowProgress</span><span class="sxs-lookup"><span data-stu-id="93595-153">-ShowProgress</span></span>
<span data-ttu-id="93595-154">Jeśli pomyślnie przekazano, jest pokazywany stan postępu.</span><span class="sxs-lookup"><span data-stu-id="93595-154">If passed then progress status is showed.</span></span> <span data-ttu-id="93595-155">Ma zastosowanie tylko wtedy, gdy jest wykonywana rekurencyjna modyfikacja listy Acl.</span><span class="sxs-lookup"><span data-stu-id="93595-155">Only applicable when recursive Acl modify is done.</span></span>

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

### <span data-ttu-id="93595-156">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="93595-156">-Confirm</span></span>
<span data-ttu-id="93595-157">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="93595-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93595-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93595-158">-WhatIf</span></span>
<span data-ttu-id="93595-159">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93595-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93595-160">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="93595-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93595-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93595-161">CommonParameters</span></span>
<span data-ttu-id="93595-162">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93595-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93595-163">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93595-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93595-164">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="93595-164">INPUTS</span></span>

### <span data-ttu-id="93595-165">System.String</span><span class="sxs-lookup"><span data-stu-id="93595-165">System.String</span></span>

### <span data-ttu-id="93595-166">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="93595-166">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="93595-167">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span><span class="sxs-lookup"><span data-stu-id="93595-167">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span></span>

### <span data-ttu-id="93595-168">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType</span><span class="sxs-lookup"><span data-stu-id="93595-168">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType</span></span>

### <span data-ttu-id="93595-169">System.Guid</span><span class="sxs-lookup"><span data-stu-id="93595-169">System.Guid</span></span>

### <span data-ttu-id="93595-170">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Permission</span><span class="sxs-lookup"><span data-stu-id="93595-170">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Permission</span></span>

### <span data-ttu-id="93595-171">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="93595-171">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="93595-172">System.Int32</span><span class="sxs-lookup"><span data-stu-id="93595-172">System.Int32</span></span>

## <span data-ttu-id="93595-173">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="93595-173">OUTPUTS</span></span>

### <span data-ttu-id="93595-174">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span><span class="sxs-lookup"><span data-stu-id="93595-174">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span></span>

## <span data-ttu-id="93595-175">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="93595-175">NOTES</span></span>

## <span data-ttu-id="93595-176">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="93595-176">RELATED LINKS</span></span>

[<span data-ttu-id="93595-177">Remove-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="93595-177">Remove-AzDataLakeStoreItemAclEntry</span></span>](./Remove-AzDataLakeStoreItemAclEntry.md)


