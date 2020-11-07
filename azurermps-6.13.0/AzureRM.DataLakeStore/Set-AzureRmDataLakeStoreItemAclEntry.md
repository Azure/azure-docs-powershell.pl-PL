---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 0671D833-8B3A-4480-A576-92F1A9E8CE92
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemAclEntry.md
ms.openlocfilehash: acf0b53ba6ad03de117e9171ec64d30ee627a927
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543912"
---
# <span data-ttu-id="d9e0d-101">Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="d9e0d-101">Set-AzureRmDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="d9e0d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d9e0d-102">SYNOPSIS</span></span>
<span data-ttu-id="d9e0d-103">Modyfikuje wpis na liście ACL pliku lub folderu w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d9e0d-103">Modifies an entry in the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9e0d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d9e0d-104">SYNTAX</span></span>

### <span data-ttu-id="d9e0d-105">SetByACLObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d9e0d-105">SetByACLObject (Default)</span></span>
```
Set-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9e0d-106">SetSpecificACE</span><span class="sxs-lookup"><span data-stu-id="d9e0d-106">SetSpecificACE</span></span>
```
Set-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-AceType] <AceType> [[-Id] <Guid>] [-Permissions] <Permission> [-Default] [-PassThru] [-Recurse]
 [-Concurrency <Int32>] [-ShowProgress] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d9e0d-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d9e0d-107">DESCRIPTION</span></span>
<span data-ttu-id="d9e0d-108">Polecenie cmdlet **Set-AzureRmDataLakeStoreItemAclEntry** modyfikuje wpis (ACE) na liście kontroli dostępu (ACL) pliku lub folderu w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d9e0d-108">The **Set-AzureRmDataLakeStoreItemAclEntry** cmdlet modifies an entry (ACE) in the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="d9e0d-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d9e0d-109">EXAMPLES</span></span>

### <span data-ttu-id="d9e0d-110">Przykład 1: Modyfikowanie uprawnień ACE</span><span class="sxs-lookup"><span data-stu-id="d9e0d-110">Example 1: Modify permissions for an ACE</span></span>
```
PS C:\>Set-AzureRmDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").ObjectId -Permissions All
```

<span data-ttu-id="d9e0d-111">To polecenie modyfikuje wpis ACE dla Patti, aby mieć wszystkie uprawnienia.</span><span class="sxs-lookup"><span data-stu-id="d9e0d-111">This command modifies the ACE for Patti Fuller to have all permissions.</span></span>

### <span data-ttu-id="d9e0d-112">Przykład 2: Modyfikowanie uprawnień w ramach wpisu ACE rekurencyjnie</span><span class="sxs-lookup"><span data-stu-id="d9e0d-112">Example 2: Modify permissions for an ACE recursively</span></span>
```
PS C:\>Set-AzureRmDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").ObjectId -Permissions All -Recurse -Concurrency 128
```

### <span data-ttu-id="d9e0d-113">Przykład 3: Modyfikowanie uprawnień dla funkcji ACE rekurencyjnie wykorzystującej obiekt ACL</span><span class="sxs-lookup"><span data-stu-id="d9e0d-113">Example 3: Modify permissions for an ACE recursively using Acl object</span></span>
```
PS C:\>$fullAcl="user:userid1:--x,default:user:userid1:--x"
PS C:\>$newFullAcl = $fullAcl.Split("{,}")
PS C:\>Set-AzureRmDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -Acl $newFullAcl -Recurse -Concurrency 128
```

<span data-ttu-id="d9e0d-114">To polecenie cyklicznie modyfikuje wpis ACE dla Patti, aby mieć wszystkie uprawnienia do katalogu głównego oraz wszystkich jego podkatalogów i plików.</span><span class="sxs-lookup"><span data-stu-id="d9e0d-114">This command recursively modifies the ACE for Patti Fuller to have all permissions to root and all its subdirectories and files.</span></span>

## <span data-ttu-id="d9e0d-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d9e0d-115">PARAMETERS</span></span>

### <span data-ttu-id="d9e0d-116">— Konto</span><span class="sxs-lookup"><span data-stu-id="d9e0d-116">-Account</span></span>
<span data-ttu-id="d9e0d-117">Określa nazwę konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d9e0d-117">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="d9e0d-118">-AceType</span><span class="sxs-lookup"><span data-stu-id="d9e0d-118">-AceType</span></span>
<span data-ttu-id="d9e0d-119">Określa typ wpisu ACE do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="d9e0d-119">Specifies the type of ACE to modify.</span></span>
<span data-ttu-id="d9e0d-120">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="d9e0d-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d9e0d-121">Konta</span><span class="sxs-lookup"><span data-stu-id="d9e0d-121">User</span></span> 
- <span data-ttu-id="d9e0d-122">Grupowanie</span><span class="sxs-lookup"><span data-stu-id="d9e0d-122">Group</span></span> 
- <span data-ttu-id="d9e0d-123">Usuń</span><span class="sxs-lookup"><span data-stu-id="d9e0d-123">Mask</span></span> 
- <span data-ttu-id="d9e0d-124">Pozostałe</span><span class="sxs-lookup"><span data-stu-id="d9e0d-124">Other</span></span>

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

### <span data-ttu-id="d9e0d-125">-ACL</span><span class="sxs-lookup"><span data-stu-id="d9e0d-125">-Acl</span></span>
<span data-ttu-id="d9e0d-126">Określa obiekt ACL zawierający wpisy do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="d9e0d-126">Specifies the ACL object that contains the entries to modify.</span></span>

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

### <span data-ttu-id="d9e0d-127">-Concurrency</span><span class="sxs-lookup"><span data-stu-id="d9e0d-127">-Concurrency</span></span>
<span data-ttu-id="d9e0d-128">Liczba plików/katalogów przetworzonych równolegle.</span><span class="sxs-lookup"><span data-stu-id="d9e0d-128">Number of files/directories processed in parallel.</span></span> <span data-ttu-id="d9e0d-129">Opcjonalnie: wybrana zostanie rozsądna wartość domyślna</span><span class="sxs-lookup"><span data-stu-id="d9e0d-129">Optional: a reasonable default will be selected</span></span>

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

### <span data-ttu-id="d9e0d-130">-Wartość domyślna</span><span class="sxs-lookup"><span data-stu-id="d9e0d-130">-Default</span></span>
<span data-ttu-id="d9e0d-131">Wskazuje, że ta operacja modyfikuje domyślny wpis ACE z określonej listy ACL.</span><span class="sxs-lookup"><span data-stu-id="d9e0d-131">Indicates that this operation modifies the default ACE from the specified ACL.</span></span>

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

### <span data-ttu-id="d9e0d-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9e0d-132">-DefaultProfile</span></span>
<span data-ttu-id="d9e0d-133">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d9e0d-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9e0d-134">-ID</span><span class="sxs-lookup"><span data-stu-id="d9e0d-134">-Id</span></span>
<span data-ttu-id="d9e0d-135">Określa identyfikator obiektu użytkownika, grupy lub podmiotu zabezpieczeń usługi AzureActive, dla którego należy zmodyfikować wpis ACE.</span><span class="sxs-lookup"><span data-stu-id="d9e0d-135">Specifies the object ID of the AzureActive Directory user, group, or service principal for which to modify an ACE.</span></span>

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

### <span data-ttu-id="d9e0d-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d9e0d-136">-PassThru</span></span>
<span data-ttu-id="d9e0d-137">Wskazuje, że wynikowa lista ACL powinna być zwracana.</span><span class="sxs-lookup"><span data-stu-id="d9e0d-137">Indicates the resulting ACL should be returned.</span></span>

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

### <span data-ttu-id="d9e0d-138">-Path</span><span class="sxs-lookup"><span data-stu-id="d9e0d-138">-Path</span></span>
<span data-ttu-id="d9e0d-139">Określa ścieżkę elementu, dla którego należy zmodyfikować wpis ACE, rozpoczynając od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="d9e0d-139">Specifies the Data Lake Store path of the item for which to modify an ACE, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="d9e0d-140">-Uprawnienia</span><span class="sxs-lookup"><span data-stu-id="d9e0d-140">-Permissions</span></span>
<span data-ttu-id="d9e0d-141">Określa uprawnienia wpisu ACE.</span><span class="sxs-lookup"><span data-stu-id="d9e0d-141">Specifies the permissions for the ACE.</span></span>
<span data-ttu-id="d9e0d-142">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="d9e0d-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d9e0d-143">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="d9e0d-143">None</span></span>
- <span data-ttu-id="d9e0d-144">Uruchomić</span><span class="sxs-lookup"><span data-stu-id="d9e0d-144">Execute</span></span>
- <span data-ttu-id="d9e0d-145">Wpisywan</span><span class="sxs-lookup"><span data-stu-id="d9e0d-145">Write</span></span>
- <span data-ttu-id="d9e0d-146">WriteExecute</span><span class="sxs-lookup"><span data-stu-id="d9e0d-146">WriteExecute</span></span>
- <span data-ttu-id="d9e0d-147">Czytał</span><span class="sxs-lookup"><span data-stu-id="d9e0d-147">Read</span></span>
- <span data-ttu-id="d9e0d-148">ReadExecute</span><span class="sxs-lookup"><span data-stu-id="d9e0d-148">ReadExecute</span></span>
- <span data-ttu-id="d9e0d-149">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d9e0d-149">ReadWrite</span></span>
- <span data-ttu-id="d9e0d-150">Cały</span><span class="sxs-lookup"><span data-stu-id="d9e0d-150">All</span></span>

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

### <span data-ttu-id="d9e0d-151">-Rekursywowanie</span><span class="sxs-lookup"><span data-stu-id="d9e0d-151">-Recurse</span></span>
<span data-ttu-id="d9e0d-152">Wskazuje, że lista ACL ma być modyfikowana rekurencyjnie do podrzędnych podkatalogów i plików</span><span class="sxs-lookup"><span data-stu-id="d9e0d-152">Indicates the ACL to be modified recursively to the child subdirectories and files</span></span>

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

### <span data-ttu-id="d9e0d-153">-ShowProgress</span><span class="sxs-lookup"><span data-stu-id="d9e0d-153">-ShowProgress</span></span>
<span data-ttu-id="d9e0d-154">Jeśli przekazano, stan postępu będzie wyświetlany.</span><span class="sxs-lookup"><span data-stu-id="d9e0d-154">If passed then progress status is showed.</span></span> <span data-ttu-id="d9e0d-155">Dotyczy tylko zmian cyklicznych listy ACL.</span><span class="sxs-lookup"><span data-stu-id="d9e0d-155">Only applicable when recursive Acl modify is done.</span></span>

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

### <span data-ttu-id="d9e0d-156">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d9e0d-156">-Confirm</span></span>
<span data-ttu-id="d9e0d-157">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9e0d-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9e0d-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9e0d-158">-WhatIf</span></span>
<span data-ttu-id="d9e0d-159">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9e0d-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9e0d-160">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d9e0d-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9e0d-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9e0d-161">CommonParameters</span></span>
<span data-ttu-id="d9e0d-162">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9e0d-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9e0d-163">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9e0d-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9e0d-164">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d9e0d-164">INPUTS</span></span>

### <span data-ttu-id="d9e0d-165">System. String</span><span class="sxs-lookup"><span data-stu-id="d9e0d-165">System.String</span></span>

### <span data-ttu-id="d9e0d-166">Microsoft. Azure. Commands. DataLakeStore. models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="d9e0d-166">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="d9e0d-167">Microsoft. Azure. Commands. DataLakeStore. models. DataLakeStoreItemAce []</span><span class="sxs-lookup"><span data-stu-id="d9e0d-167">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span></span>

### <span data-ttu-id="d9e0d-168">Microsoft. Azure. Commands. DataLakeStore. models. DataLakeStoreEnums + AceType</span><span class="sxs-lookup"><span data-stu-id="d9e0d-168">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType</span></span>

### <span data-ttu-id="d9e0d-169">System. GUID</span><span class="sxs-lookup"><span data-stu-id="d9e0d-169">System.Guid</span></span>

### <span data-ttu-id="d9e0d-170">Microsoft. Azure. Commands. DataLakeStore. models. DataLakeStoreEnums + uprawnienie</span><span class="sxs-lookup"><span data-stu-id="d9e0d-170">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Permission</span></span>

### <span data-ttu-id="d9e0d-171">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d9e0d-171">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="d9e0d-172">System. Int32</span><span class="sxs-lookup"><span data-stu-id="d9e0d-172">System.Int32</span></span>

## <span data-ttu-id="d9e0d-173">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d9e0d-173">OUTPUTS</span></span>

### <span data-ttu-id="d9e0d-174">Microsoft. Azure. Commands. DataLakeStore. models. DataLakeStoreItemAce</span><span class="sxs-lookup"><span data-stu-id="d9e0d-174">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span></span>
<span data-ttu-id="d9e0d-175">Jeśli PassThru jest określony, zwróci wynikową listę wpisów listy ACL.</span><span class="sxs-lookup"><span data-stu-id="d9e0d-175">If PassThru is specified, will return the resulting list of ACL entries.</span></span>

## <span data-ttu-id="d9e0d-176">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d9e0d-176">NOTES</span></span>

## <span data-ttu-id="d9e0d-177">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d9e0d-177">RELATED LINKS</span></span>

[<span data-ttu-id="d9e0d-178">Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="d9e0d-178">Remove-AzureRmDataLakeStoreItemAclEntry</span></span>](./Remove-AzureRmDataLakeStoreItemAclEntry.md)

