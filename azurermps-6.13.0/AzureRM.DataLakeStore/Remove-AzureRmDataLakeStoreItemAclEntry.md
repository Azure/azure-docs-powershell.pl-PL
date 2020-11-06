---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 33E7607E-C2BC-4F46-9038-91AC92041F00
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/remove-azurermdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 154c57c6a403fce574a785aaf60d95a7936907b9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524445"
---
# <span data-ttu-id="d3f35-101">Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="d3f35-101">Remove-AzureRmDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="d3f35-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d3f35-102">SYNOPSIS</span></span>
<span data-ttu-id="d3f35-103">Usuwa wpis z listy ACL pliku lub folderu w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d3f35-103">Removes an entry from the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d3f35-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d3f35-104">SYNTAX</span></span>

### <span data-ttu-id="d3f35-105">RemoveByACLObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d3f35-105">RemoveByACLObject (Default)</span></span>
```
Remove-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3f35-106">RemoveSpecificACE</span><span class="sxs-lookup"><span data-stu-id="d3f35-106">RemoveSpecificACE</span></span>
```
Remove-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-AceType] <AceType> [[-Id] <Guid>] [-Default] [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3f35-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d3f35-107">DESCRIPTION</span></span>
<span data-ttu-id="d3f35-108">Polecenie cmdlet **Remove-AzureRmDataLakeStoreItemAclEntry** usuwa wpis (ACE) z listy kontroli dostępu (ACL) pliku lub folderu w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d3f35-108">The **Remove-AzureRmDataLakeStoreItemAclEntry** cmdlet removes an entry (ACE) from the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="d3f35-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d3f35-109">EXAMPLES</span></span>

### <span data-ttu-id="d3f35-110">Przykład 1. Usuń wpis użytkownika</span><span class="sxs-lookup"><span data-stu-id="d3f35-110">Example 1: Remove a user entry</span></span>
```
PS C:\>Remove-AzureRmDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").ObjectId
```

<span data-ttu-id="d3f35-111">To polecenie usuwa wpis ACE użytkownika dla Patti z konta ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="d3f35-111">This command removes the user ACE for Patti Fuller from the ContosoADL account.</span></span>

### <span data-ttu-id="d3f35-112">Przykład 2: cykliczne Usuwanie wpisu użytkownika</span><span class="sxs-lookup"><span data-stu-id="d3f35-112">Example 2: Remove a user entry recursively</span></span>
```
PS C:\>Remove-AzureRmDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").ObjectId -Recurse -Concurrency 128
```

### <span data-ttu-id="d3f35-113">Przykład 3: usuwanie uprawnień do cyklicznego wpisu ACE przy użyciu obiektu ACL</span><span class="sxs-lookup"><span data-stu-id="d3f35-113">Example 3: Remove permissions for an ACE recursively using Acl object</span></span>
```
PS C:\>$fullAcl="user:userid1,default:user:userid1
PS C:\>$newFullAcl = $fullAcl.Split("{,}")
PS C:\>Remove-AzureRmDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -Acl $newFullAcl -Recurse -Concurrency 128
```

<span data-ttu-id="d3f35-114">To polecenie usuwa wpis ACE użytkownika dla Patti z katalogu głównego i rekursywnie ze wszystkich podkatalogów i plików konta ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="d3f35-114">This command removes the user ACE for Patti Fuller from the root and recursively from all it's subdirectories and files for account ContosoADL.</span></span>

## <span data-ttu-id="d3f35-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d3f35-115">PARAMETERS</span></span>

### <span data-ttu-id="d3f35-116">— Konto</span><span class="sxs-lookup"><span data-stu-id="d3f35-116">-Account</span></span>
<span data-ttu-id="d3f35-117">Określa nazwę konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d3f35-117">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="d3f35-118">-AceType</span><span class="sxs-lookup"><span data-stu-id="d3f35-118">-AceType</span></span>
<span data-ttu-id="d3f35-119">Określa typ wpisu ACE do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="d3f35-119">Specifies the type of ACE to remove.</span></span>
<span data-ttu-id="d3f35-120">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="d3f35-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d3f35-121">Konta</span><span class="sxs-lookup"><span data-stu-id="d3f35-121">User</span></span>
- <span data-ttu-id="d3f35-122">Grupowanie</span><span class="sxs-lookup"><span data-stu-id="d3f35-122">Group</span></span>
- <span data-ttu-id="d3f35-123">Usuń</span><span class="sxs-lookup"><span data-stu-id="d3f35-123">Mask</span></span>
- <span data-ttu-id="d3f35-124">Pozostałe</span><span class="sxs-lookup"><span data-stu-id="d3f35-124">Other</span></span>

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

### <span data-ttu-id="d3f35-125">-ACL</span><span class="sxs-lookup"><span data-stu-id="d3f35-125">-Acl</span></span>
<span data-ttu-id="d3f35-126">Określa obiekt ACL zawierający wpisy, które mają zostać usunięte.</span><span class="sxs-lookup"><span data-stu-id="d3f35-126">Specifies the ACL object that contains the entries to be removed.</span></span>

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

### <span data-ttu-id="d3f35-127">-Concurrency</span><span class="sxs-lookup"><span data-stu-id="d3f35-127">-Concurrency</span></span>
<span data-ttu-id="d3f35-128">Liczba plików/katalogów przetworzonych równolegle.</span><span class="sxs-lookup"><span data-stu-id="d3f35-128">Number of files/directories processed in parallel.</span></span> <span data-ttu-id="d3f35-129">Opcjonalnie: wybrana zostanie rozsądna wartość domyślna</span><span class="sxs-lookup"><span data-stu-id="d3f35-129">Optional: a reasonable default will be selected</span></span>

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

### <span data-ttu-id="d3f35-130">-Wartość domyślna</span><span class="sxs-lookup"><span data-stu-id="d3f35-130">-Default</span></span>
<span data-ttu-id="d3f35-131">Wskazuje, że ta operacja powoduje usunięcie domyślnego wpisu ACE z określonej listy ACL.</span><span class="sxs-lookup"><span data-stu-id="d3f35-131">Indicates that this operation removes the default ACE from the specified ACL.</span></span>

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

### <span data-ttu-id="d3f35-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3f35-132">-DefaultProfile</span></span>
<span data-ttu-id="d3f35-133">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d3f35-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3f35-134">-ID</span><span class="sxs-lookup"><span data-stu-id="d3f35-134">-Id</span></span>
<span data-ttu-id="d3f35-135">Określa identyfikator obiektu użytkownika katalogu AzureActive, grupę lub podmiot zabezpieczeń usługi, dla którego ma zostać usunięty wpis ACE.</span><span class="sxs-lookup"><span data-stu-id="d3f35-135">Specifies the object ID of the AzureActive Directory user, group, or service principal for which to remove an ACE.</span></span>

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

### <span data-ttu-id="d3f35-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d3f35-136">-PassThru</span></span>
<span data-ttu-id="d3f35-137">Wskazuje, że należy zwrócić odpowiedź logiczną wskazującą wynik operacji usuwania.</span><span class="sxs-lookup"><span data-stu-id="d3f35-137">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="d3f35-138">-Path</span><span class="sxs-lookup"><span data-stu-id="d3f35-138">-Path</span></span>
<span data-ttu-id="d3f35-139">Określa ścieżkę do usługi Data Lake Store, z której ma zostać usunięty wpis ACE, począwszy od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="d3f35-139">Specifies the Data Lake Store path of the item from which to remove an ACE, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="d3f35-140">-Rekursywowanie</span><span class="sxs-lookup"><span data-stu-id="d3f35-140">-Recurse</span></span>
<span data-ttu-id="d3f35-141">Wskazuje, że lista ACL ma być usuwana rekurencyjnie do podrzędnych podkatalogów i plików</span><span class="sxs-lookup"><span data-stu-id="d3f35-141">Indicates the ACL to be removed recursively to the child subdirectories and files</span></span>

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

### <span data-ttu-id="d3f35-142">-ShowProgress</span><span class="sxs-lookup"><span data-stu-id="d3f35-142">-ShowProgress</span></span>
<span data-ttu-id="d3f35-143">Jeśli przekazano, stan postępu będzie wyświetlany.</span><span class="sxs-lookup"><span data-stu-id="d3f35-143">If passed then progress status is showed.</span></span> <span data-ttu-id="d3f35-144">Dotyczy tylko usuwania cyklicznego listy ACL.</span><span class="sxs-lookup"><span data-stu-id="d3f35-144">Only applicable when recursive Acl remove is done.</span></span>

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

### <span data-ttu-id="d3f35-145">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d3f35-145">-Confirm</span></span>
<span data-ttu-id="d3f35-146">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3f35-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3f35-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3f35-147">-WhatIf</span></span>
<span data-ttu-id="d3f35-148">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3f35-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3f35-149">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d3f35-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3f35-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3f35-150">CommonParameters</span></span>
<span data-ttu-id="d3f35-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3f35-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3f35-152">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3f35-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3f35-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d3f35-153">INPUTS</span></span>

### <span data-ttu-id="d3f35-154">System. String</span><span class="sxs-lookup"><span data-stu-id="d3f35-154">System.String</span></span>

### <span data-ttu-id="d3f35-155">Microsoft. Azure. Commands. DataLakeStore. models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="d3f35-155">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="d3f35-156">Microsoft. Azure. Commands. DataLakeStore. models. DataLakeStoreItemAce []</span><span class="sxs-lookup"><span data-stu-id="d3f35-156">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span></span>

### <span data-ttu-id="d3f35-157">Microsoft. Azure. Commands. DataLakeStore. models. DataLakeStoreEnums + AceType</span><span class="sxs-lookup"><span data-stu-id="d3f35-157">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType</span></span>

### <span data-ttu-id="d3f35-158">System. GUID</span><span class="sxs-lookup"><span data-stu-id="d3f35-158">System.Guid</span></span>

### <span data-ttu-id="d3f35-159">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d3f35-159">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="d3f35-160">System. Int32</span><span class="sxs-lookup"><span data-stu-id="d3f35-160">System.Int32</span></span>

## <span data-ttu-id="d3f35-161">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d3f35-161">OUTPUTS</span></span>

### <span data-ttu-id="d3f35-162">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d3f35-162">System.Boolean</span></span>

## <span data-ttu-id="d3f35-163">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d3f35-163">NOTES</span></span>

## <span data-ttu-id="d3f35-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d3f35-164">RELATED LINKS</span></span>

[<span data-ttu-id="d3f35-165">Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="d3f35-165">Set-AzureRmDataLakeStoreItemAclEntry</span></span>](./Set-AzureRmDataLakeStoreItemAclEntry.md)


