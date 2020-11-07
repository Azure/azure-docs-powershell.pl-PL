---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 33E7607E-C2BC-4F46-9038-91AC92041F00
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 7cc09813f03e5424b7d44b7a56810167ca5affba
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710022"
---
# <span data-ttu-id="09753-101">Remove-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="09753-101">Remove-AzDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="09753-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="09753-102">SYNOPSIS</span></span>
<span data-ttu-id="09753-103">Usuwa wpis z listy ACL pliku lub folderu w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="09753-103">Removes an entry from the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="09753-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="09753-104">SYNTAX</span></span>

### <span data-ttu-id="09753-105">RemoveByACLObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="09753-105">RemoveByACLObject (Default)</span></span>
```
Remove-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09753-106">RemoveSpecificACE</span><span class="sxs-lookup"><span data-stu-id="09753-106">RemoveSpecificACE</span></span>
```
Remove-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance> [-AceType] <AceType>
 [[-Id] <Guid>] [-Default] [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09753-107">Opis</span><span class="sxs-lookup"><span data-stu-id="09753-107">DESCRIPTION</span></span>
<span data-ttu-id="09753-108">Polecenie cmdlet **Remove-AzDataLakeStoreItemAclEntry** usuwa wpis (ACE) z listy kontroli dostępu (ACL) pliku lub folderu w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="09753-108">The **Remove-AzDataLakeStoreItemAclEntry** cmdlet removes an entry (ACE) from the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="09753-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="09753-109">EXAMPLES</span></span>

### <span data-ttu-id="09753-110">Przykład 1. Usuń wpis użytkownika</span><span class="sxs-lookup"><span data-stu-id="09753-110">Example 1: Remove a user entry</span></span>
```
PS C:\>Remove-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId
```

<span data-ttu-id="09753-111">To polecenie usuwa wpis ACE użytkownika dla Patti z konta ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="09753-111">This command removes the user ACE for Patti Fuller from the ContosoADL account.</span></span>

### <span data-ttu-id="09753-112">Przykład 2: cykliczne Usuwanie wpisu użytkownika</span><span class="sxs-lookup"><span data-stu-id="09753-112">Example 2: Remove a user entry recursively</span></span>
```
PS C:\>Remove-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId -Recurse -Concurrency 128
```

### <span data-ttu-id="09753-113">Przykład 3: usuwanie uprawnień do cyklicznego wpisu ACE przy użyciu obiektu ACL</span><span class="sxs-lookup"><span data-stu-id="09753-113">Example 3: Remove permissions for an ACE recursively using Acl object</span></span>
```
PS C:\>$fullAcl="user:userid1,default:user:userid1
PS C:\>$newFullAcl = $fullAcl.Split("{,}")
PS C:\>Remove-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -Acl $newFullAcl -Recurse -Concurrency 128
```

<span data-ttu-id="09753-114">To polecenie usuwa wpis ACE użytkownika dla Patti z katalogu głównego i rekursywnie ze wszystkich podkatalogów i plików konta ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="09753-114">This command removes the user ACE for Patti Fuller from the root and recursively from all it's subdirectories and files for account ContosoADL.</span></span>

## <span data-ttu-id="09753-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="09753-115">PARAMETERS</span></span>

### <span data-ttu-id="09753-116">— Konto</span><span class="sxs-lookup"><span data-stu-id="09753-116">-Account</span></span>
<span data-ttu-id="09753-117">Określa nazwę konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="09753-117">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="09753-118">-AceType</span><span class="sxs-lookup"><span data-stu-id="09753-118">-AceType</span></span>
<span data-ttu-id="09753-119">Określa typ wpisu ACE do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="09753-119">Specifies the type of ACE to remove.</span></span>
<span data-ttu-id="09753-120">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="09753-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="09753-121">Konta</span><span class="sxs-lookup"><span data-stu-id="09753-121">User</span></span>
- <span data-ttu-id="09753-122">Grupowanie</span><span class="sxs-lookup"><span data-stu-id="09753-122">Group</span></span>
- <span data-ttu-id="09753-123">Usuń</span><span class="sxs-lookup"><span data-stu-id="09753-123">Mask</span></span>
- <span data-ttu-id="09753-124">Pozostałe</span><span class="sxs-lookup"><span data-stu-id="09753-124">Other</span></span>

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

### <span data-ttu-id="09753-125">-ACL</span><span class="sxs-lookup"><span data-stu-id="09753-125">-Acl</span></span>
<span data-ttu-id="09753-126">Określa obiekt ACL zawierający wpisy, które mają zostać usunięte.</span><span class="sxs-lookup"><span data-stu-id="09753-126">Specifies the ACL object that contains the entries to be removed.</span></span>

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

### <span data-ttu-id="09753-127">-Concurrency</span><span class="sxs-lookup"><span data-stu-id="09753-127">-Concurrency</span></span>
<span data-ttu-id="09753-128">Liczba plików/katalogów przetworzonych równolegle.</span><span class="sxs-lookup"><span data-stu-id="09753-128">Number of files/directories processed in parallel.</span></span> <span data-ttu-id="09753-129">Opcjonalnie: wybrana zostanie rozsądna wartość domyślna</span><span class="sxs-lookup"><span data-stu-id="09753-129">Optional: a reasonable default will be selected</span></span>

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

### <span data-ttu-id="09753-130">-Wartość domyślna</span><span class="sxs-lookup"><span data-stu-id="09753-130">-Default</span></span>
<span data-ttu-id="09753-131">Wskazuje, że ta operacja powoduje usunięcie domyślnego wpisu ACE z określonej listy ACL.</span><span class="sxs-lookup"><span data-stu-id="09753-131">Indicates that this operation removes the default ACE from the specified ACL.</span></span>

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

### <span data-ttu-id="09753-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09753-132">-DefaultProfile</span></span>
<span data-ttu-id="09753-133">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="09753-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09753-134">-ID</span><span class="sxs-lookup"><span data-stu-id="09753-134">-Id</span></span>
<span data-ttu-id="09753-135">Określa identyfikator obiektu użytkownika katalogu AzureActive, grupę lub podmiot zabezpieczeń usługi, dla którego ma zostać usunięty wpis ACE.</span><span class="sxs-lookup"><span data-stu-id="09753-135">Specifies the object ID of the AzureActive Directory user, group, or service principal for which to remove an ACE.</span></span>

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

### <span data-ttu-id="09753-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="09753-136">-PassThru</span></span>
<span data-ttu-id="09753-137">Wskazuje, że należy zwrócić odpowiedź logiczną wskazującą wynik operacji usuwania.</span><span class="sxs-lookup"><span data-stu-id="09753-137">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="09753-138">-Path</span><span class="sxs-lookup"><span data-stu-id="09753-138">-Path</span></span>
<span data-ttu-id="09753-139">Określa ścieżkę do usługi Data Lake Store, z której ma zostać usunięty wpis ACE, począwszy od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="09753-139">Specifies the Data Lake Store path of the item from which to remove an ACE, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="09753-140">-Rekursywowanie</span><span class="sxs-lookup"><span data-stu-id="09753-140">-Recurse</span></span>
<span data-ttu-id="09753-141">Wskazuje, że lista ACL ma być usuwana rekurencyjnie do podrzędnych podkatalogów i plików</span><span class="sxs-lookup"><span data-stu-id="09753-141">Indicates the ACL to be removed recursively to the child subdirectories and files</span></span>

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

### <span data-ttu-id="09753-142">-ShowProgress</span><span class="sxs-lookup"><span data-stu-id="09753-142">-ShowProgress</span></span>
<span data-ttu-id="09753-143">Jeśli przekazano, stan postępu będzie wyświetlany.</span><span class="sxs-lookup"><span data-stu-id="09753-143">If passed then progress status is showed.</span></span> <span data-ttu-id="09753-144">Dotyczy tylko usuwania cyklicznego listy ACL.</span><span class="sxs-lookup"><span data-stu-id="09753-144">Only applicable when recursive Acl remove is done.</span></span>

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

### <span data-ttu-id="09753-145">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="09753-145">-Confirm</span></span>
<span data-ttu-id="09753-146">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09753-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09753-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09753-147">-WhatIf</span></span>
<span data-ttu-id="09753-148">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09753-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09753-149">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="09753-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09753-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09753-150">CommonParameters</span></span>
<span data-ttu-id="09753-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09753-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09753-152">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09753-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09753-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="09753-153">INPUTS</span></span>

### <span data-ttu-id="09753-154">System. String</span><span class="sxs-lookup"><span data-stu-id="09753-154">System.String</span></span>

### <span data-ttu-id="09753-155">Microsoft. Azure. Commands. DataLakeStore. models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="09753-155">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="09753-156">Microsoft. Azure. Commands. DataLakeStore. models. DataLakeStoreItemAce []</span><span class="sxs-lookup"><span data-stu-id="09753-156">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span></span>

### <span data-ttu-id="09753-157">Microsoft. Azure. Commands. DataLakeStore. models. DataLakeStoreEnums + AceType</span><span class="sxs-lookup"><span data-stu-id="09753-157">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType</span></span>

### <span data-ttu-id="09753-158">System. GUID</span><span class="sxs-lookup"><span data-stu-id="09753-158">System.Guid</span></span>

### <span data-ttu-id="09753-159">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="09753-159">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="09753-160">System. Int32</span><span class="sxs-lookup"><span data-stu-id="09753-160">System.Int32</span></span>

## <span data-ttu-id="09753-161">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="09753-161">OUTPUTS</span></span>

### <span data-ttu-id="09753-162">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="09753-162">System.Boolean</span></span>

## <span data-ttu-id="09753-163">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="09753-163">NOTES</span></span>

## <span data-ttu-id="09753-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="09753-164">RELATED LINKS</span></span>

[<span data-ttu-id="09753-165">Set-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="09753-165">Set-AzDataLakeStoreItemAclEntry</span></span>](./Set-AzDataLakeStoreItemAclEntry.md)


