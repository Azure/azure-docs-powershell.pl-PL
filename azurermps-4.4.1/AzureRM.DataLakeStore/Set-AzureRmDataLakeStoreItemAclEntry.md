---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 0671D833-8B3A-4480-A576-92F1A9E8CE92
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 9646ef98499e56e24ce81c78f6b94dce75ff0078
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553332"
---
# <span data-ttu-id="ab00a-101">Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="ab00a-101">Set-AzureRmDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="ab00a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ab00a-102">SYNOPSIS</span></span>
<span data-ttu-id="ab00a-103">Modyfikuje wpis na liście ACL pliku lub folderu w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ab00a-103">Modifies an entry in the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab00a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ab00a-104">SYNTAX</span></span>

### <span data-ttu-id="ab00a-105">Ustawianie wpisów list ACL przy użyciu obiektu ACL (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="ab00a-105">Set ACL Entries using ACL object (Default)</span></span>
```
Set-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ab00a-106">Ustawianie konkretnego wpisu ACE</span><span class="sxs-lookup"><span data-stu-id="ab00a-106">Set specific ACE</span></span>
```
Set-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-AceType] <AceType> [[-Id] <Guid>] [-Permissions] <Permission> [-Default] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab00a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ab00a-107">DESCRIPTION</span></span>
<span data-ttu-id="ab00a-108">Polecenie cmdlet **Set-AzureRmDataLakeStoreItemAclEntry** modyfikuje wpis (ACE) na liście kontroli dostępu (ACL) pliku lub folderu w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ab00a-108">The **Set-AzureRmDataLakeStoreItemAclEntry** cmdlet modifies an entry (ACE) in the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="ab00a-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ab00a-109">EXAMPLES</span></span>

### <span data-ttu-id="ab00a-110">Przykład 1: Modyfikowanie uprawnień ACE</span><span class="sxs-lookup"><span data-stu-id="ab00a-110">Example 1: Modify permissions for an ACE</span></span>
```
PS C:\>Set-AzureRmDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").ObjectId -Permissions All
```

<span data-ttu-id="ab00a-111">To polecenie modyfikuje wpis ACE dla Patti, aby mieć wszystkie uprawnienia.</span><span class="sxs-lookup"><span data-stu-id="ab00a-111">This command modifies the ACE for Patti Fuller to have all permissions.</span></span>

## <span data-ttu-id="ab00a-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ab00a-112">PARAMETERS</span></span>

### <span data-ttu-id="ab00a-113">— Konto</span><span class="sxs-lookup"><span data-stu-id="ab00a-113">-Account</span></span>
<span data-ttu-id="ab00a-114">Określa nazwę konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ab00a-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="ab00a-115">-AceType</span><span class="sxs-lookup"><span data-stu-id="ab00a-115">-AceType</span></span>
<span data-ttu-id="ab00a-116">Określa typ wpisu ACE do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="ab00a-116">Specifies the type of ACE to modify.</span></span>
<span data-ttu-id="ab00a-117">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="ab00a-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ab00a-118">Konta</span><span class="sxs-lookup"><span data-stu-id="ab00a-118">User</span></span> 
- <span data-ttu-id="ab00a-119">Grupowanie</span><span class="sxs-lookup"><span data-stu-id="ab00a-119">Group</span></span> 
- <span data-ttu-id="ab00a-120">Usuń</span><span class="sxs-lookup"><span data-stu-id="ab00a-120">Mask</span></span> 
- <span data-ttu-id="ab00a-121">Pozostałe</span><span class="sxs-lookup"><span data-stu-id="ab00a-121">Other</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType
Parameter Sets: Set specific ACE
Aliases: 
Accepted values: User, Group, Mask, Other

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab00a-122">-ACL</span><span class="sxs-lookup"><span data-stu-id="ab00a-122">-Acl</span></span>
<span data-ttu-id="ab00a-123">Określa obiekt ACL zawierający wpisy do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="ab00a-123">Specifies the ACL object that contains the entries to modify.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]
Parameter Sets: Set ACL Entries using ACL object
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ab00a-124">-Wartość domyślna</span><span class="sxs-lookup"><span data-stu-id="ab00a-124">-Default</span></span>
<span data-ttu-id="ab00a-125">Wskazuje, że ta operacja modyfikuje domyślny wpis ACE z określonej listy ACL.</span><span class="sxs-lookup"><span data-stu-id="ab00a-125">Indicates that this operation modifies the default ACE from the specified ACL.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Set specific ACE
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab00a-126">-ID</span><span class="sxs-lookup"><span data-stu-id="ab00a-126">-Id</span></span>
<span data-ttu-id="ab00a-127">Określa identyfikator obiektu użytkownika, grupy lub podmiotu zabezpieczeń usługi AzureActive, dla którego należy zmodyfikować wpis ACE.</span><span class="sxs-lookup"><span data-stu-id="ab00a-127">Specifies the object ID of the AzureActive Directory user, group, or service principal for which to modify an ACE.</span></span>

```yaml
Type: System.Guid
Parameter Sets: Set specific ACE
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab00a-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ab00a-128">-PassThru</span></span>
<span data-ttu-id="ab00a-129">Wskazuje, że wynikowa lista ACL powinna być zwracana.</span><span class="sxs-lookup"><span data-stu-id="ab00a-129">Indicates the resulting ACL should be returned.</span></span>

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

### <span data-ttu-id="ab00a-130">-Path</span><span class="sxs-lookup"><span data-stu-id="ab00a-130">-Path</span></span>
<span data-ttu-id="ab00a-131">Określa ścieżkę elementu, dla którego należy zmodyfikować wpis ACE, rozpoczynając od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="ab00a-131">Specifies the Data Lake Store path of the item for which to modify an ACE, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="ab00a-132">-Uprawnienia</span><span class="sxs-lookup"><span data-stu-id="ab00a-132">-Permissions</span></span>
<span data-ttu-id="ab00a-133">Określa uprawnienia wpisu ACE.</span><span class="sxs-lookup"><span data-stu-id="ab00a-133">Specifies the permissions for the ACE.</span></span>
<span data-ttu-id="ab00a-134">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="ab00a-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ab00a-135">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="ab00a-135">None</span></span>
- <span data-ttu-id="ab00a-136">Uruchomić</span><span class="sxs-lookup"><span data-stu-id="ab00a-136">Execute</span></span>
- <span data-ttu-id="ab00a-137">Wpisywan</span><span class="sxs-lookup"><span data-stu-id="ab00a-137">Write</span></span>
- <span data-ttu-id="ab00a-138">WriteExecute</span><span class="sxs-lookup"><span data-stu-id="ab00a-138">WriteExecute</span></span>
- <span data-ttu-id="ab00a-139">Czytał</span><span class="sxs-lookup"><span data-stu-id="ab00a-139">Read</span></span>
- <span data-ttu-id="ab00a-140">ReadExecute</span><span class="sxs-lookup"><span data-stu-id="ab00a-140">ReadExecute</span></span>
- <span data-ttu-id="ab00a-141">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ab00a-141">ReadWrite</span></span>
- <span data-ttu-id="ab00a-142">Cały</span><span class="sxs-lookup"><span data-stu-id="ab00a-142">All</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Permission
Parameter Sets: Set specific ACE
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab00a-143">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ab00a-143">-Confirm</span></span>
<span data-ttu-id="ab00a-144">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab00a-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab00a-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab00a-145">-WhatIf</span></span>
<span data-ttu-id="ab00a-146">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab00a-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab00a-147">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ab00a-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab00a-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab00a-148">-DefaultProfile</span></span>
<span data-ttu-id="ab00a-149">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ab00a-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab00a-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab00a-150">CommonParameters</span></span>
<span data-ttu-id="ab00a-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab00a-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab00a-152">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab00a-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab00a-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ab00a-153">INPUTS</span></span>

### <span data-ttu-id="ab00a-154">DataLakeStoreItemAce[]</span><span class="sxs-lookup"><span data-stu-id="ab00a-154">DataLakeStoreItemAce[]</span></span>
<span data-ttu-id="ab00a-155">Parametr "ACL" przyjmuje wartość typu "DataLakeStoreItemAce []" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="ab00a-155">Parameter 'Acl' accepts value of type 'DataLakeStoreItemAce[]' from the pipeline</span></span>

## <span data-ttu-id="ab00a-156">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ab00a-156">OUTPUTS</span></span>

### <span data-ttu-id="ab00a-157">IEnumerable<DataLakeStoreItemAce></span><span class="sxs-lookup"><span data-stu-id="ab00a-157">IEnumerable<DataLakeStoreItemAce></span></span>
<span data-ttu-id="ab00a-158">Jeśli PassThru jest określony, zwróci wynikową listę wpisów listy ACL.</span><span class="sxs-lookup"><span data-stu-id="ab00a-158">If PassThru is specified, will return the resulting list of ACL entries.</span></span>

## <span data-ttu-id="ab00a-159">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ab00a-159">NOTES</span></span>

## <span data-ttu-id="ab00a-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ab00a-160">RELATED LINKS</span></span>

[<span data-ttu-id="ab00a-161">Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="ab00a-161">Remove-AzureRmDataLakeStoreItemAclEntry</span></span>](./Remove-AzureRmDataLakeStoreItemAclEntry.md)


